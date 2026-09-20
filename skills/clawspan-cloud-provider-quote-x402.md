---
name: clawspan-cloud-provider-quote-x402
description: Price a metered provider capability, fund it with a spend envelope or the x402 402/X-PAYMENT handshake, execute it under a lease, and list executions.
api: ShardLink Control Plane API
base_url: https://app.clawspan.cloud
generated: '2026-09-19'
method: generated
source: openapi/clawspan-cloud-shardlink-control-plane-openapi.yml + https://app.clawspan.cloud/v1/capabilities/graph (providerExecution) + https://app.clawspan.cloud/.well-known/roaming-agent.json
operations:
  - getProviderCatalog
  - createProviderQuote
  - createBillingAccount
  - createSpendEnvelope
  - executeProviderQuote
  - listProviderExecutions
---

# Buy a metered capability through a provider quote

ShardLink resells metered third-party capabilities inside a workspace - `inference` (openai-metered, 20 USD
cents/unit), `browser` (browserbase-metered, 59), `search` (exa-metered, 11), `storage` (s3-metered, 6) and
`notifications` (resend-metered, 4) per the capability graph on 2026-09-19. Every one is `quoteRequired`,
`fundingRequired` and `settlementLinked`. Execution needs an **agent** actor with an **active lease** and must be
the quote's owner.

## Steps

1. **Catalog** - `getProviderCatalog` (`GET /v1/workspaces/{slug}/providers/catalog`) for the capabilities the
   workspace allows and their unit prices in `usdCents`.
2. **Quote** - `createProviderQuote` (`POST /v1/workspaces/{slug}/providers/quotes`, `Idempotency-Key` required).
   The `201` carries a `quoteId`. Nothing is charged yet.
3. **Fund** - choose one:
   - **Envelope**: `createBillingAccount` (`POST /v1/workspaces/{slug}/billing/accounts`) once, then
     `createSpendEnvelope` (`POST .../billing/accounts/{accountId}/envelopes`) referencing a
     `fundingInstrumentId`; pass the resulting `envelopeId` in the execute body.
   - **x402**: send execute with no envelope; the first call answers `402` with a `PAYMENT-REQUIRED` header and a
     `PaymentRequirementEnvelope` (`quoteId`, `paymentId`); settle it with your wallet and retry with an
     `X-PAYMENT` header. Per the preflight, x402 status was `contract_scaffolded` on 2026-09-19 - expect the
     envelope path to be the one that works today.
4. **Execute** - `executeProviderQuote` (`POST /v1/workspaces/{slug}/providers/quotes/{quoteId}/execute`,
   `Idempotency-Key` required). `201` returns the execution with its settlement link.
5. **Audit** - `listProviderExecutions` (`GET /v1/workspaces/{slug}/providers/executions`).

## Errors to plan for

| code | status | meaning |
|---|---|---|
| `payment_required` | 402 | x402 challenge (see step 3) |
| `no_active_lease` | 403 | request a lease first |
| `forbidden` | 403 | not the quote owner, or the capability is suspended for the workspace |
| `idempotency_mismatch` | 409 | same key, different body - use a fresh key |

There is no refund or cancel operation on an executed quote; the only reversible objects on this surface are the
funding controls - `revokeDelegatedSpendGrant` and the MCP-only `workspaces.billing.envelopes.revoke` - and no
reversal window is published for either.
