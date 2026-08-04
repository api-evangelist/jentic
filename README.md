# Jentic (jentic)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Jentic is an AI infrastructure company building the agentic knowledge layer for APIs. Founded in late 2024 and backed by $4.5M in pre-seed funding, Jentic enables enterprises to confidently manage, scale, and govern AI agent initiatives in a unified platform built on open standards. The platform provides secure execution, managed authentication, unified permissions, and observability for AI agents accessing 1,500+ public APIs and 2,000+ agent-ready workflows. Jentic's bet is that AI agents need a standards-based control plane built on OpenAPI plus Arazzo workflows plus MCP, rather than ad-hoc tool wiring inside every agent framework. The platform ships the Jentic Public APIs catalog, the Arazzo Engine (workflow runner), the Standard Agent (a composable ReWOO-style reasoning agent), the Jentic Mini self-hosted execution layer, a hosted Remote MCP server at api.jentic.com/mcp, and the Jentic API AI-Readiness Framework (JAIRF) for scoring API readiness for agents.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/jentic/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/jentic/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- AI Agents
- Arazzo
- OpenAPI
- MCP
- Workflows
- Integrations
- Agent Runtime
- Standard Agent
- Just In Time Tooling
- Credential Vault
- Agent Governance
- Observability
- API AI Readiness

## Timestamps

- **Created:** 2026-01-02
- **Modified:** 2026-05-19

## APIs

### Jentic API

The Jentic API is the hosted agent control plane. It exposes a small, stable surface that lets any agent dynamically discover, load, and execute API operations and Arazzo workflows from the Jentic catalog. Authentication uses an agent-scoped API key (X-JENTIC-API-KEY). The canonical flow is search to load to execute: search the catalog by natural language, load the schema and auth requirements for the returned operation or workflow UUIDs, and execute with managed server-side credential injection. Operation UUIDs are prefixed op_ and workflow UUIDs are prefixed wf_, and both are accepted by the execute endpoint.

- **Human URL:** [https://docs.jentic.com/reference/public-apis/](https://docs.jentic.com/reference/public-apis/)
- **Base URL:** `https://api.jentic.com/api/v1`

#### Tags

- AI Agents
- Arazzo
- OpenAPI
- Workflows
- Integrations
- MCP
- Agent Runtime

#### Properties

- [Website](https://jentic.com/)
- [Documentation](https://docs.jentic.com/)
- [Getting Started](https://docs.jentic.com/getting-started/quickstart/)
- [API Reference](https://docs.jentic.com/reference/public-apis/)
- [Sign Up](https://app.jentic.com/sign-up)
- [Console](https://app.jentic.com/)
- [Base U R L](https://api.jentic.com/api/v1)
- [OpenAPI](openapi/jentic-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/jentic.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/jentic.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Spectral Rules](rules/jentic-rules.yml)
- [JSON Schema](json-schema/jentic-operation-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/jentic-agent-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/jentic-workflow-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/jentic-operation-structure.json)
- [Example](examples/jentic-search-example.json)
- [Example](examples/jentic-load-example.json)
- [Example](examples/jentic-execute-example.json)
- [Example](examples/jentic-register-example.json)

### Jentic Remote MCP Server

The Jentic Remote MCP Server is the hosted Model Context Protocol endpoint that exposes the Jentic catalog to MCP-capable clients (Claude Desktop, ChatGPT, Cursor, Windsurf, VS Code). It speaks the same search / load / execute pattern as the Jentic API, but packaged as MCP tools. Supports OAuth 2.0 with PKCE and dynamic client registration, with an API key fallback for Cursor and Windsurf.

- **Human URL:** [https://docs.jentic.com/guides/mcp/remote-mcp/](https://docs.jentic.com/guides/mcp/remote-mcp/)
- **Base URL:** `https://api.jentic.com/mcp`

#### Tags

- MCP
- AI Agents
- OAuth
- Remote MCP

#### Properties

- [Documentation](https://docs.jentic.com/guides/mcp/)
- [Getting Started](https://docs.jentic.com/guides/mcp/remote-mcp/)
- [Base U R L](https://api.jentic.com/mcp)
- [Postman Collection](collections/jentic.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/jentic.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Arazzo Engine

Open-source Python engine that executes Arazzo workflow specifications alongside OpenAPI operation definitions. Powers the Jentic platform's workflow execution and is also installable standalone as arazzo-runner for direct use in agents and automation. Handles authentication resolution (API key, OAuth 2.0, basic, bearer), dynamic server URL resolution, parameter chaining between steps, and blob storage for large binary payloads.

- **Human URL:** [https://github.com/jentic/arazzo-engine](https://github.com/jentic/arazzo-engine)

#### Tags

- Arazzo
- OpenAPI
- Workflows
- Open Source

#### Properties

- [Source Code](https://github.com/jentic/arazzo-engine)
- [Documentation](https://docs.jentic.com/getting-started/arazzo-runner/)
- [Python Package](https://pypi.org/project/arazzo-runner/)
- [Postman Collection](collections/jentic.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/jentic.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Jentic Standard Agent

Open-source composable reasoning agent framework that plans, acts, and recovers from failures, preconfigured with Jentic tools and a ReWOO reasoning loop. Primary entry point is the ReWOOAgent Python class. Bring-your-own LLM (Anthropic, OpenAI, Google). Demonstrates how to build an agent that uses Jentic's just-in-time tooling without committing to a specific agent framework.

- **Human URL:** [https://github.com/jentic/standard-agent](https://github.com/jentic/standard-agent)

#### Tags

- Agent Framework
- ReWOO
- Open Source
- Python

#### Properties

- [Source Code](https://github.com/jentic/standard-agent)
- [Documentation](https://docs.jentic.com/getting-started/standard-agent/)
- [Postman Collection](collections/jentic.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/jentic.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Jentic Mini

Free, open-source, self-hosted API execution layer that sits between an agent and the outside world. The agent says what it wants to do and Jentic Mini handles the how: finding the right API, injecting credentials at runtime, and brokering the request. Intended for teams that want Jentic's execution model without sending traffic through the hosted Jentic API.

- **Human URL:** [https://github.com/jentic/jentic-mini](https://github.com/jentic/jentic-mini)

#### Tags

- Self Hosted
- Open Source
- Agent Runtime

#### Properties

- [Source Code](https://github.com/jentic/jentic-mini)
- [Postman Collection](collections/jentic.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/jentic.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Jentic API AI-Readiness Framework (JAIRF)

Technical specification for evaluating how interpretable, operable, and trustworthy an API is for AI systems and autonomous agents. Defines the signals, dimensions, scoring model, and normalization rules used by the Jentic API Scorecard product. Apache 2.0.

- **Human URL:** [https://github.com/jentic/api-ai-readiness-framework](https://github.com/jentic/api-ai-readiness-framework)

#### Tags

- Specification
- API AI Readiness
- Open Source

#### Properties

- [Source Code](https://github.com/jentic/api-ai-readiness-framework)
- [Postman Collection](collections/jentic.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/jentic.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://jentic.com/)
- [Blog](https://jentic.com/blog)
- [Documentation](https://docs.jentic.com/)
- [Pricing](https://jentic.com/pricing)
- [Sign Up](https://app.jentic.com/sign-up)
- [Console](https://app.jentic.com/)
- [Contact](https://jentic.com/contact)
- [About](https://jentic.com/company)
- [GitHub Organization](https://github.com/jentic)
- [Privacy Policy](https://jentic.com/privacy)
- [Terms of Service](https://jentic.com/terms)
- [LinkedIn](https://www.linkedin.com/company/jentic)
- [YouTube](https://youtube.com/@JenticAI)
- [Support](https://docs.jentic.com/community/support/)
- [F A Q](https://docs.jentic.com/community/faq/)
- [Security](https://docs.jentic.com/community/security/)
- [Contributing](https://docs.jentic.com/community/contributing/)
- [Press](https://jentic.com/blog/press)
- [Blog Feed](https://jentic.com/blog/feed.xml)
- [Python Package](https://pypi.org/project/jentic/)
- [Python Package](https://pypi.org/project/arazzo-runner/)
- [Vocabulary](vocabulary/jentic-vocabulary.yml)
- [JSON-LD](json-ld/jentic-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [JSON Schema](json-schema/jentic-operation-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/jentic-agent-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/jentic-workflow-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Agent Skill](https://github.com/jentic/jentic-skills)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
