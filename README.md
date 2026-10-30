# Jentic

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

Jentic is an AI infrastructure company building the agentic knowledge layer for APIs. Founded in late 2024 and backed by $4.5M in pre-seed funding, Jentic enables enterprises to confidently manage, scale, and govern AI agent initiatives in a unified platform built on open standards. The platform provides secure execution, managed authentication, unified permissions, and observability for AI agents accessing 1,500+ public APIs and 2,000+ agent-ready workflows. Jentic's bet is that AI agents need a standards-based control plane built on OpenAPI plus Arazzo workflows plus MCP, rather than ad-hoc tool wiring inside every agent framework. The platform ships the Jentic Public APIs catalog, the Arazzo Engine (workflow runner), the Standard Agent (a composable ReWOO-style reasoning agent), the Jentic Mini self-hosted execution layer, a hosted Remote MCP server at api.jentic.com/mcp, and the Jentic API AI-Readiness Framework (JAIRF) for scoring API readiness for agents.

**Areas:** AI Agents · Arazzo · OpenAPI · MCP · Workflows · Integration · Agent Runtime · Standard Agent · Just In Time Tooling · Credential Vault · Agent Governance · Observability

## Jentic on APIs.io

Everything profiled for Jentic is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/jentic/](https://apis.io/providers/jentic/)** — or go straight to one of the APIs or properties below.

### APIs (8)

- [Jentic Remote MCP Server](https://apis.io/apis/jentic/jentic-mcp/) — The Jentic Remote MCP Server is the hosted Model Context Protocol endpoint that exposes the Jentic catalog to MCP-capable clients (Claude Desktop, ChatGPT,…
- [Arazzo Engine](https://apis.io/apis/jentic/arazzo-engine/) — Open-source Python engine that executes Arazzo workflow specifications alongside OpenAPI operation definitions. Powers the Jentic platform's workflow…
- [Jentic Standard Agent](https://apis.io/apis/jentic/standard-agent/) — Open-source composable reasoning agent framework that plans, acts, and recovers from failures, preconfigured with Jentic tools and a ReWOO reasoning loop.…
- [Jentic Mini](https://apis.io/apis/jentic/jentic-mini/) — Free, open-source, self-hosted API execution layer that sits between an agent and the outside world. The agent says what it wants to do and Jentic Mini…
- [Jentic API AI-Readiness Framework (JAIRF)](https://apis.io/apis/jentic/jairf/) — Technical specification for evaluating how interpretable, operable, and trustworthy an API is for AI systems and autonomous agents. Defines the signals,…
- [Jentic Authentication API](https://apis.io/apis/jentic/jentic-authentication-api/) — Registration and API key management for accessing the Jentic platform.
- [Jentic Execution API](https://apis.io/apis/jentic/jentic-execution-api/) — Load execution details and execute API operations or Arazzo workflows with managed authentication and credential injection.
- [Jentic Search API](https://apis.io/apis/jentic/jentic-search-api/) — Semantic search over the Jentic API and workflow catalog using natural language queries.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [jentic](https://apis.io/servers/jentic/jentic/)

#### Agent skills (3)

Agent skills built on the API.

- [jentic](https://apis.io/agent-skills/jentic/jentic/)
- [jentic-v1](https://apis.io/agent-skills/jentic/jentic-v1/)
- [jentic-workflows](https://apis.io/agent-skills/jentic/jentic-workflows/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Jentic Agentic Access](https://apis.io/agentic-access/jentic/jentic-agentic-access/)

#### JSON Schema (3)

The data models the API reads and writes.

- [Jentic Agent](https://apis.io/schemas/jentic/jentic-agent/)
- [Jentic Operation](https://apis.io/schemas/jentic/jentic-operation/)
- [Jentic Workflow](https://apis.io/schemas/jentic/jentic-workflow/)

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Jentic Operation Structure](https://apis.io/json-structure/jentic/jentic-operation-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Jentic Context](https://apis.io/jsonld/jentic/jentic-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Jentic Vocabulary](https://apis.io/vocabularies/jentic/jentic-vocabulary/)

#### Examples (5)

Example requests and responses.

- [Jentic Execute Example](https://apis.io/examples/jentic/jentic-execute-example/)
- [Jentic Load Example](https://apis.io/examples/jentic/jentic-load-example/)
- [Jentic Register Example](https://apis.io/examples/jentic/jentic-register-example/)
- [Jentic Search Example](https://apis.io/examples/jentic/jentic-search-example/)
- [Jentic Workflow Execute Example](https://apis.io/examples/jentic/jentic-workflow-execute-example/)

#### Collections (7)

Postman and Open Collection request collections.

- [Jentic API](https://apis.io/collections/jentic/open-jentic/)
- [Jentic Authentication API](https://apis.io/collections/jentic/open-jentic-authentication-api/)
- [Jentic Authentication Execution API](https://apis.io/collections/jentic/open-jentic-execution-api/)
- [Jentic Authentication Search API](https://apis.io/collections/jentic/open-jentic-search-api/)
- [Jentic Authentication API](https://apis.io/collections/jentic/postman-jentic-authentication-api/)
- [Jentic Authentication Execution API](https://apis.io/collections/jentic/postman-jentic-execution-api/)
- [Jentic Authentication Search API](https://apis.io/collections/jentic/postman-jentic-search-api/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Jentic — jsonschema rules](https://apis.io/rules/jentic/jentic-jsonschema-spectral-rules/)
- [Jentic API Rules](https://apis.io/rules/jentic/jentic-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Jentic Authentication](https://apis.io/security/jentic/jentic-authentication/)
- [Jentic Domain Security](https://apis.io/security/jentic/jentic-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Jentic Plans Pricing](https://apis.io/plans/jentic/jentic-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Jentic Rate Limits](https://apis.io/rate-limits/jentic/jentic-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Jentic Finops](https://apis.io/finops/jentic/jentic-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://jentic.com/)
- [Documentation](https://docs.jentic.com/)
- [Pricing](https://jentic.com/pricing)
- [Support](https://docs.jentic.com/community/support/)
- [Blog](https://jentic.com/blog)
- [Security](https://docs.jentic.com/community/security/)
- [Terms of service](https://jentic.com/terms)
- [Privacy policy](https://jentic.com/privacy)
- [GitHub](https://github.com/jentic)

## API Evangelist rating

**Kin Score 52.2** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 61.7 |
| Contract quality | 66.1 |
| Contract governance | 27.3 |
| Operational transparency | 23.7 |
| Developer ergonomics | 62.4 |
| Access clarity | 50.0 |

**Agent readiness 34.8** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | verified |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | unknown |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | na |

**Regulatory alignment 24.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/jentic/](https://apis.io/providers/jentic/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Jentic: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/jentic/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
