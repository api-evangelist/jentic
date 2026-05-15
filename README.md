# Jentic (jentic)

Jentic is an AI infrastructure company building the agentic knowledge layer for APIs. Founded in late 2024 in Dublin, Ireland and backed by $4.5M in pre-seed funding, Jentic enables enterprises to confidently manage, scale, and govern AI agent initiatives in a unified platform built on open standards. The platform provides secure execution, managed authentication, unified permissions, and observability for AI agents accessing 1,500+ public APIs and 2,000+ agent-ready Arazzo workflows.

Jentic's bet is that AI agents need a standards-based control plane built on **OpenAPI + Arazzo workflows + Model Context Protocol**, rather than ad-hoc tool wiring inside every agent framework. The platform ships the Jentic Public APIs catalog, the Arazzo Engine (workflow runner), the Standard Agent (a composable ReWOO-style reasoning agent), the Jentic Mini self-hosted execution layer, a hosted Remote MCP server at `api.jentic.com/mcp`, and the Jentic API AI-Readiness Framework (JAIRF) for scoring API readiness for agents.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/jentic/refs/heads/main/apis.yml)

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
- **Modified:** 2026-05-15

## APIs

### Jentic API

The hosted agent control plane. A small, stable surface that lets any agent dynamically discover, load, and execute API operations and Arazzo workflows from the Jentic catalog. Canonical flow: `search → load → execute`. Operation UUIDs are prefixed `op_` and workflow UUIDs are prefixed `wf_`. Authentication uses an agent-scoped API key (`X-JENTIC-API-KEY`).

- **Human URL:** https://docs.jentic.com/reference/public-apis/
- **Base URL:** https://api.jentic.com/api/v1
- **OpenAPI:** [openapi/jentic-openapi.yml](openapi/jentic-openapi.yml)

#### Endpoints

| Method | Path | OperationId | Summary |
|---|---|---|---|
| POST | `/auth/register` | registerAccount | Register A New Jentic Account |
| POST | `/agents/search` | searchApis | Search For APIs And Workflows |
| POST | `/agents/load` | loadExecutionInfo | Load Execution Information For Operations |
| POST | `/agents/execute` | executeOperation | Execute An API Operation Or Workflow |

### Jentic Remote MCP Server

The hosted Model Context Protocol endpoint at `https://api.jentic.com/mcp`. Exposes `search_apis`, `load_execution_info`, `execute`, and `list_credentials` to MCP-capable clients. OAuth 2.0 with PKCE and dynamic client registration recommended; API-key fallback supported for Cursor and Windsurf.

| Client | OAuth | API Key |
|---|---|---|
| Claude Desktop | yes | — |
| ChatGPT | yes | — |
| Cursor | yes | yes |
| Windsurf | yes | yes |
| VS Code | local | local |

### Arazzo Engine

Open-source Python engine that executes Arazzo workflow specifications alongside OpenAPI operation definitions. Powers Jentic's server-side workflow execution and is installable standalone as `arazzo-runner`. Handles authentication resolution (API key, OAuth 2.0, basic, bearer), dynamic server URL resolution, parameter chaining, and blob storage for large payloads.

- **Source:** https://github.com/jentic/arazzo-engine
- **Install:** `pip install arazzo-runner`

### Jentic Standard Agent

Open-source composable reasoning agent framework that plans, acts, and recovers from failures, preconfigured with Jentic tools and a ReWOO reasoning loop. Primary class `ReWOOAgent`. Bring-your-own LLM (Anthropic, OpenAI, Google).

- **Source:** https://github.com/jentic/standard-agent

### Jentic Mini

Free, open-source, self-hosted API execution layer that sits between an agent and the outside world. Intended for teams that want Jentic's execution model without sending traffic through the hosted Jentic API.

- **Source:** https://github.com/jentic/jentic-mini

### Jentic API AI-Readiness Framework (JAIRF)

Technical specification for evaluating how interpretable, operable, and trustworthy an API is for AI systems and autonomous agents. Defines the signals, dimensions, scoring model, and normalization rules used by the Jentic API Scorecard product.

- **Source:** https://github.com/jentic/api-ai-readiness-framework

## SDKs And Tools

| Name | Repository | Language | Install |
|---|---|---|---|
| Jentic Python SDK | https://github.com/jentic/jentic-sdks | Python | `pip install jentic` |
| Jentic TypeScript SDK | (not yet available) | TypeScript | — |
| Arazzo Runner | https://github.com/jentic/arazzo-engine | Python | `pip install arazzo-runner` |
| Jentic Mini | https://github.com/jentic/jentic-mini | Python | — |
| Standard Agent | https://github.com/jentic/standard-agent | Python | `make install` |
| Jentic OpenAPI Tools | https://github.com/jentic/jentic-openapi-tools | Python | — |
| Jentic Arazzo Tools | https://github.com/jentic/jentic-arazzo-tools | TypeScript | — |
| Jentic Skills (OpenClaw) | https://github.com/jentic/jentic-skills | Python | — |
| Jentic Quick Claw | https://github.com/jentic/jentic-quick-claw | Shell | — |
| Jentic Cursor | https://github.com/jentic/jentic-cursor | JavaScript | — |
| API Problem Details | https://github.com/jentic/api-problem-details | Python | — |

## Editions

| Edition | Price | Notes |
|---|---|---|
| Core | Free | Single-user. Public APIs catalog. AI-readiness diagnostics. Platform-managed execution. |
| Enterprise | Contact sales | Agentic Sandbox, private API ingestion, governance, VPC/customer-managed hosting, SLAs, dedicated support. |

Detailed plan entries: [plans/jentic-plans-pricing.yml](plans/jentic-plans-pricing.yml). Rate limits: [rate-limits/jentic-rate-limits.yml](rate-limits/jentic-rate-limits.yml). FinOps mapping: [finops/jentic-finops.yml](finops/jentic-finops.yml). Both plans and rate-limits files carry `reconciled: false` because Jentic does not publish numeric quotas.

## Artifacts

- **OpenAPI:** [openapi/jentic-openapi.yml](openapi/jentic-openapi.yml)
- **Naftiko Capabilities:**
  - [capabilities/jentic-capability.yaml](capabilities/jentic-capability.yaml)
  - [capabilities/arazzo-workflow-execution.yaml](capabilities/arazzo-workflow-execution.yaml)
  - [capabilities/agent-tool-discovery.yaml](capabilities/agent-tool-discovery.yaml)
  - [capabilities/mcp-publishing.yaml](capabilities/mcp-publishing.yaml)
- **JSON Schema:**
  - [json-schema/jentic-operation-schema.json](json-schema/jentic-operation-schema.json)
  - [json-schema/jentic-workflow-schema.json](json-schema/jentic-workflow-schema.json)
  - [json-schema/jentic-agent-schema.json](json-schema/jentic-agent-schema.json)
- **JSON Structure:** [json-structure/jentic-operation-structure.json](json-structure/jentic-operation-structure.json)
- **JSON-LD:** [json-ld/jentic-context.jsonld](json-ld/jentic-context.jsonld)
- **Vocabulary:** [vocabulary/jentic-vocabulary.yml](vocabulary/jentic-vocabulary.yml)
- **Spectral Rules:** [rules/jentic-rules.yml](rules/jentic-rules.yml)
- **Examples:** [examples/](examples/) — register, search, load, execute (operation), execute (workflow)
- **Plans / Pricing:** [plans/jentic-plans-pricing.yml](plans/jentic-plans-pricing.yml)
- **Rate Limits:** [rate-limits/jentic-rate-limits.yml](rate-limits/jentic-rate-limits.yml)
- **FinOps:** [finops/jentic-finops.yml](finops/jentic-finops.yml)

## Common Properties

- [Website](https://jentic.com/)
- [Blog](https://jentic.com/blog)
- [Documentation](https://docs.jentic.com/)
- [Pricing](https://jentic.com/pricing)
- [SignUp](https://app.jentic.com/sign-up)
- [Console](https://app.jentic.com/)
- [Contact](https://jentic.com/contact)
- [About](https://jentic.com/company)
- [GitHubOrganization](https://github.com/jentic)
- [PrivacyPolicy](https://jentic.com/privacy)
- [TermsOfService](https://jentic.com/terms)
- [LinkedIn](https://www.linkedin.com/company/jentic)
- [YouTube](https://youtube.com/@JenticAI)
- [Support](https://docs.jentic.com/community/support/)
- [FAQ](https://docs.jentic.com/community/faq/)
- [Security](https://docs.jentic.com/community/security/)
- [PythonPackage](https://pypi.org/project/jentic/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
