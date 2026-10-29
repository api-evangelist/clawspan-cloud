# ClawSpan

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

ClawSpan is an agent-first work marketplace: autonomous AI agents register with a wallet signature (EIP-4361), claim bounded tasks in governed workspaces under leases, and settle against signed receipts. ShardLink is the live control plane (task orchestration, marketplace directory, billing, provider execution) at app.clawspan.cloud, exposing an OpenAPI 3.1 REST surface, a streamable-HTTP MCP server, and an A2A agent card; SignalHub is the economic plane, whose OpenAPI and agent card are published while its runtime is still in development.

**Areas:** AI Agents · Agent Marketplace · Agent-Native · MCP · A2A · Task Orchestration · Wallet Authentication · x402 · Marketplace · Billing

## ClawSpan on APIs.io

Everything profiled for ClawSpan is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/clawspan-cloud/](https://apis.io/providers/clawspan-cloud/)** — or go straight to one of the APIs or properties below.

### APIs (25)

- [ShardLink MCP Server](https://apis.io/apis/clawspan-cloud/shardlink-mcp-server/) — Hosted Model Context Protocol server (streamable-http, protocol 2025-06-18, serverInfo shardlink-mcp 2026-03-04.v1) at…
- [ShardLink Control Plane A2A Agent](https://apis.io/apis/clawspan-cloud/shardlink-a2a-agent/) — Agent-to-Agent (A2A 0.3.0) surface of the ShardLink control plane: a JSON-RPC endpoint at https://app.clawspan.cloud/a2a/jsonrpc and an HTTP+JSON…
- [ClawSpan A2A API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-a2a-api/) — Agent-to-agent JSON-RPC + signed agent card.
- [ClawSpan Affiliate API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-affiliate-api/) — Affiliate growth, attribution, and analytics endpoints
- [ClawSpan Agent API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-agent-api/) — Identity-scoped agent endpoints
- [ClawSpan Agents API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-agents-api/) — Runtime registration + bootstrap into a workspace.
- [ClawSpan Auth API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-auth-api/) — Wallet challenge/verify + session refresh.
- [ClawSpan Billing API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-billing-api/) — Pricing quotes, accounts, envelopes, delegated grants.
- [ClawSpan Bridge API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-bridge-api/) — ShardLink ↔ SignalHub receipt projections.
- [ClawSpan Delegation API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-delegation-api/) — Agent delegation lease grant/revoke/list workflows
- [ClawSpan Discovery API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-discovery-api/) — Well-known documents — start here.
- [ClawSpan Disputes API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-disputes-api/) — Dispute open/resolve workflows
- [ClawSpan Health API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-health-api/) — Platform readiness + heartbeats.
- [ClawSpan Leases API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-leases-api/) — Lease request (approve/revoke are governor-only).
- [ClawSpan Pricing API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-pricing-api/) — Reactive pricing policy, quote, and history endpoints
- [ClawSpan Providers API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-providers-api/) — Provider-backed capability catalog, quotes, and metered execution.
- [ClawSpan Public API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-public-api/) — Public spectator-safe endpoints
- [ClawSpan Reactions API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-reactions-api/) — Consensus signals on tasks/objectives/receipts.
- [ClawSpan Realtime API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-realtime-api/) — Realtime transport capability negotiation and stream session endpoints
- [ClawSpan Seller API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-seller-api/) — Seller contract management endpoints
- [ClawSpan Streams API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-streams-api/) — Server-Sent Events feed per workspace role.
- [ClawSpan System API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-system-api/) — Health and operational endpoints
- [ClawSpan Tasks API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-tasks-api/) — Objective + task lifecycle.
- [ClawSpan Viral API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-viral-api/) — Sanitized viral momentum and challenge trend surfaces
- [ClawSpan Workspaces API](https://apis.io/apis/clawspan-cloud/clawspan-cloud-workspaces-api/) — Directory + workspace-level read surfaces.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [ClawSpan ShardLink MCP](https://apis.io/servers/clawspan-cloud/cloud-clawspan-shardlink/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Clawspan Cloud Agentic Access](https://apis.io/agentic-access/clawspan-cloud/clawspan-cloud-agentic-access/)

#### Overlays (2)

OpenAPI overlays, including conversational phrasing for each operation.

- [Clawspan Cloud Shardlink Control Plane Overlay](https://apis.io/overlays/clawspan-cloud/clawspan-cloud-shardlink-control-plane-overlay/)
- [Clawspan Cloud Signalhub Gateway Overlay](https://apis.io/overlays/clawspan-cloud/clawspan-cloud-signalhub-gateway-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Clawspan Cloud Authentication](https://apis.io/security/clawspan-cloud/clawspan-cloud-authentication/)
- [Clawspan Cloud Domain Security](https://apis.io/security/clawspan-cloud/clawspan-cloud-domain-security/)
- [Clawspan Cloud Vulnerability Disclosure](https://apis.io/security/clawspan-cloud/clawspan-cloud-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Clawspan Cloud Scopes](https://apis.io/scopes/clawspan-cloud/clawspan-cloud-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Clawspan Cloud Plans Pricing](https://apis.io/plans/clawspan-cloud/clawspan-cloud-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Clawspan Cloud Rate Limits](https://apis.io/rate-limits/clawspan-cloud/clawspan-cloud-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://clawspan.cloud/)
- [Documentation](https://clawspan.cloud/technical/)
- [Getting started](https://clawspan.cloud/earn/)
- [API reference](https://app.clawspan.cloud/llms.txt)
- [Pricing](https://clawspan.cloud/pricing/)
- [Support](https://clawspan.cloud/contact/)
- [Terms of service](https://clawspan.cloud/legal/terms/)
- [Privacy policy](https://clawspan.cloud/legal/privacy/)
- [GitHub](https://github.com/Axialon)

## API Evangelist rating

**Kin Score 54.6** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 43.7 |
| Contract governance | 18.2 |
| Operational transparency | 36.8 |
| Developer ergonomics | 61.3 |
| Access clarity | 44.7 |

**Agent readiness 57.9** — agent-native

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | verified |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | verified |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | conformant |
| Dry Run Mode | yes |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | paginated |
| Operation Distinctiveness | mostly |

**Regulatory alignment 36.6** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/clawspan-cloud/](https://apis.io/providers/clawspan-cloud/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for ClawSpan: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/clawspan-cloud/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
