# Scenario

> Status: Accepted
> Canonical owner: Not supplied
> Required reviewers: Not supplied
> Gate: G0
> Last reviewed: 2026-09-01

## Basis of this framing

The framing in this folder is written directly from the supplied enterprise concept material and from the approved, CIO-sponsored mandate for a company-wide agent-platform blueprint that supports either centralized platform operation or multiple federated operations. Statements below restate that material.

## Representative business scenario

A representative business scenario is not required. The user confirmed (2026-09-01) that this is a platform investment intended to enable developer teams to build business solutions faster through streamlined governance, release management, and cost management. The functional implementation scenarios below (`SCN-001` to `SCN-010`) constitute the platform's end-to-end lifecycle and value chain.

## Current situation

- Enterprises are moving from isolated AI experiments towards portfolios of agent-enabled products, services and processes that operate across business units, data platforms, user channels and enterprise systems.
- The challenge is to create an operating environment in which many teams can deliver many solutions without repeatedly rediscovering the same security, identity, networking, model management, observability and governance patterns; as portfolios grow, the decisive scaling constraint becomes reusable enterprise context rather than the number of available models.
- Teams commonly define their own protocols, discovery mechanisms, orchestration patterns, roles, accountability and interpretation of business meaning, so bespoke integration, local interpretation and limited reuse become the default.
- When each project makes local decisions about subscriptions, network access, model endpoints, secrets, tool connections, telemetry, cost attribution and lifecycle ownership, identity, security, governance, observability and compliance cannot consistently follow every interaction from source to context, agent and action.

## Trigger and desired change

The trigger is the approved enterprise mandate for a company-wide agent-platform blueprint. The desired change, as stated in the supplied material, is that foundational work and enterprise context become shared, reusable and governed capabilities, so that project teams consume prepared building blocks for infrastructure, composition, semantics, organisational scope and controls instead of repeatedly rebuilding infrastructure and controls. A project receives a usable environment, identities, model contract, telemetry and deployment path rather than an empty subscription.

## Roles named in the supplied material

| Role or team | Responsibility as supplied |
|---|---|
| CIO sponsor | Sponsors the approved enterprise mandate |
| Cloud Platform team | Owns the management hierarchy, hub connectivity, shared DNS, policy definitions and identity foundation |
| Application Platform team | Provides regional execution and integration services for containerized agents, MCP servers, APIs and supporting workflows |
| AI Platform team | Owns model catalogue publication and the technical model lifecycle, and provides governed model access |
| Data Platform team | Owns enterprise data products; semantic definitions are co-owned with the Agent Project team |
| Agent Governance | Accountable for agent policy and publication processes in the Agent Control Plane |
| API management or gateway team | Owns tool and MCP gateway policy together with Agent Governance |
| Agent Project team | Owns the business outcome, the user journey, agent behavior, solution logic and the evidence that the solution is safe, useful and measurable |

## Context and boundaries

| Boundary | As supplied |
|---|---|
| Organization and users | An internal enterprise platform in one identity tenant, shared across business domains with project-level isolation; the approved mandate applies company-wide and supports either centralized platform operation or multiple federated operations |
| Platform scope | Multi-region platform foundations with regional workload execution, container runtime patterns for custom agents, APIs and MCP servers, governed model access through an AI gateway, structured and unstructured grounding, agent and MCP identity, inventory, publication and security governance, private network integration and user-facing ingress, evaluation, observability, operational support, cost attribution, lifecycle automation, and a repeatable onboarding blueprint |
| Excluded | A mandate for one agent SDK, orchestration framework or user-interface technology; replacement of existing enterprise API, data, cloud or application platforms; unrestricted autonomous write access to enterprise systems |
| Separate design boundary | A customer-facing, multi-tenant control plane or acceptance of identities from other tenants requires a separate tenant-isolation design |
| Data | Governed data products, semantic models, retrieval indexes and session and memory stores with classification, lineage, freshness, retention and deletion rules |

## Enterprise-platform and operating-model intent

The blueprint is positioned as an operating model, not as a single technology deployment. It supports two viable options built on the same 24 capabilities and architecture.

- In the centralized model, one platform team owns the enterprise foundations and the full agent lifecycle. This maximises consistency, direct accountability and control, and remains viable where central capacity can meet demand or risk requires concentrated delivery ownership.
- In the federated model, the central platform owns the responsibilities that must remain consistent: identity policy, subscription hierarchy, baseline security, network guardrails, model and tool mediation, registries, telemetry standards, compliance evidence, lifecycle automation and cost attribution. Domain teams choose appropriate solution patterns, runtimes and user experiences, then build and operate agents within those guardrails.
- Both options remain viable and neither is an assumed maturity destination. The supplied operating-model decision guidance places the formal choice at the end of Phase 2, while the centralized MVP roadmap requires a centralized choice in its Phase 0 charter and the federated MVP roadmap assumes centralized foundations through Phase 2. This timing inconsistency remains unresolved. The decision guidance says to use production evidence about demand, risk, central capacity, domain skills and control maturity, score its stated criteria and readiness conditions, and record the result in an architecture decision record. A hybrid outcome is described as legitimate and common.
- The decision determines who builds and operates agents; it does not change the 24 capabilities the platform must provide. Each capability has exactly one accountable owner, and deciding per capability whether it is owned centrally, owned by domains or shared is the operating-model choice.

## Blueprint capability areas

| Domain | Numbers | Capability names as supplied |
|---|---|---|
| Enterprise Platform Foundations | 1-6 | Billing, FinOps & Commercial Management; Resource Organization & Platform Hierarchy; Identity, Roles & Access Management; Network Topology & Connectivity; Platform Management & Operations; Business Continuity & Resilience |
| Governance & Security | 7-10 | Identity & Trust Foundation; AI Security, Trust & Runtime Protection; Governance, Risk & Compliance Platform; Lifecycle, Platform Engineering & Automation |
| Runtime & Experience | 11-14 | AI Runtime & Execution Platform; Workflow Orchestration & Agent Coordination; Agent Memory & Context Management; User Experience & Channel Integration |
| Intelligence | 15-18 | Model Gateway & AI Access Platform; Enterprise Knowledge & Semantic Foundation; Knowledge & Data Platform; Evaluation, Benchmarking & Quality Engineering |
| Interoperability | 19-21 | Tool, API & MCP Connectivity Platform; Agent & MCP Registry; Enterprise Capability Marketplace |
| Operations | 22-24 | Observability, Telemetry & Evaluation Platform; AI FinOps & Cost Management Platform; Enterprise Agent Enablement & Operating Model |

## Functional implementation scenarios

The identifiers below organize the functional implementation scenarios supplied by the concept.

| ID | Lifecycle scenario | Trigger as supplied | Behavior and control points as supplied |
|---|---|---|---|
| `SCN-001` | Onboard an Agent Project | An approved business use case needs a development and production path | The project submits owner, sponsor, business outcome, data classes, target users, regions, expected usage, required tools and preliminary risk tier. An automated workflow creates the project hierarchy, network attachment, groups, identities, runtime tenancy, model access, telemetry, budget and a draft inventory record. Platform owners approve only exceptions and privileged access. The risk tier selects runtime isolation, evaluation depth, write-action policy and resilience pattern, and production credentials and data permissions are not granted to non-production identities |
| `SCN-002` | Build and run a grounded read-only agent | An employee asks a question that requires approved enterprise knowledge | The channel authenticates the user, the project API starts a trace and invokes the agent, the agent calls the model gateway and, when grounding is needed, a read-only retrieval tool through the tool gateway. The retrieval service evaluates the effective user or project scope and returns bounded results with source identifiers. Retrieved content is treated as untrusted data rather than instructions, document-level access is enforced by the retrieval service, the model receives only the minimum required context, and sensitive prompt or document content is not placed in default logs |
| `SCN-003` | Consume models across regions | The primary model deployment is throttled, unavailable or lacks sufficient capacity | The project calls a logical model endpoint. The gateway authenticates the runtime, applies project quota and selects an eligible backend using health, residency and capacity policy, with bounded retry for safe failure classes, and records backend region, deployment version, token usage and fallback reason. The fallback list is approved before production, data-zone and regional restrictions override availability, and a materially different model requires an explicit project acceptance decision and separate evaluation results |
| `SCN-004` | Publish and consume an MCP server | A project or platform team exposes a reusable capability for agents | The provider packages the MCP server and publishes its tool schemas, owner, version, authorization mode, data classification, operation risk and SLO. The server is deployed privately, the gateway applies token validation, operation allow-lists, quotas and audit policy and publishes discovery metadata, and consumers receive the gateway endpoint rather than the runtime endpoint. Tool descriptions are reviewed because they influence model behavior, schemas use bounded types, server-side authorization remains authoritative, and breaking schema changes require a new version |
| `SCN-005` | Execute a state-changing business action | An agent proposes creating, updating or closing a business record | The agent calls a validation operation that has no side effect, a deterministic service checks schema, business rules, authorization and duplicate risk, and the workflow classifies the action. Low-risk pre-authorized actions can proceed; higher-risk actions produce a human approval containing the exact proposed change, after which a dedicated transaction tool executes with an idempotency key and returns the authoritative result. Write scope is separate from read scope, approval cannot be inferred from conversational language, and compensating action or manual recovery is defined for partial failure |
| `SCN-006` | Register and publish an enterprise agent | A project version is ready for production or cross-team reuse | The release pipeline submits an agent manifest containing identity, owner, sponsor, runtime, version, capabilities, intended users, data classes, tools, models, risk tier, evaluation report, threat model, SLO, support route and retirement date. Automated checks verify required evidence and endpoint ownership, and the approved version is registered and, when reusable, listed in the enterprise catalogue, with deployment and registry version linked. Publication does not grant tool or data access, consumer authorization remains separate, and material changes to tools, autonomy, data, model class or business effect trigger re-evaluation |
| `SCN-007` | Maintain session state and long-term memory | An agent needs continuity within a conversation or across sessions | State is classified as ephemeral session context, durable workflow state or long-term memory, each using a separate logical store and retention policy. Session context expires automatically, workflow state records deterministic progress and is not summarized away, and long-term memory is written only for an approved purpose, is scoped to user or team and supports inspection and deletion. Retrieval filters memory by effective identity and purpose before it enters model context, secrets and prohibited data are filtered, shared memory requires an explicit authorization model, and memory writes and deletes are auditable |
| `SCN-008` | Evaluate and promote an agent release | Code, prompt, model route, retrieval configuration or tool description changes | Continuous integration builds an immutable image, scans it and runs deterministic unit and contract tests. The evaluation stage runs curated multi-turn scenarios covering expected outcomes, tool selection, authorization, groundedness, safety, latency and cost, compared with the production baseline, and a release is promoted only when mandatory thresholds pass and no protected cohort regresses beyond tolerance. Evaluation datasets are versioned and separated from prompts, a model change is treated as a release even when application code is unchanged, and rollback restores the prior complete configuration rather than only the container image |
| `SCN-009` | Expose an agent through a public user channel | Customers, partners or mobile users need controlled access | Public traffic terminates at approved edge services and routes to regional application ingress. The project API authenticates the caller, establishes tenant and user context, applies abuse controls and invokes the private agent endpoint, and the agent reaches models, tools and data only through private platform paths. The agent runtime, model gateway and data endpoints remain private, edge protection does not replace application authorization, and anonymous use, if allowed, uses a restricted agent policy, isolated data and strict quotas |
| `SCN-010` | Detect and contain unsafe agent behavior | Monitoring detects anomalous tool use, repeated policy denial, suspected prompt injection, data exfiltration or compromised identity | Security, gateway and application signals create a correlated incident in the enterprise security process. The responder identifies the affected agent version, identity, users, tools and traces. Containment disables the agent identity, removes a gateway route, revokes tool scope or scales the deployment to zero according to blast radius. Evidence is retained under incident policy, and recovery requires corrected configuration, targeted evaluation and governance approval. Containment does not depend on cooperation from the agent; security teams have read access to required metadata and a pre-approved emergency action path; prompt-content access follows privacy and incident-handling policy |

## Terminology

- **Enterprise Agent Platform** means the complete blueprint and operating environment; **Agent Control Plane** is the governance, identity, inventory and policy building block within it. The supplied material notes that its planning input called that block the Agent Platform.
- An **Agent Project** is the delivery boundary in which a team composes approved models, tools, data, runtime components and user experiences into an agent-enabled solution.
- A **golden path** or **paved road** is a prepared, governed onboarding and delivery route.
- A **building block** groups coherent platform responsibilities; the supplied material names six of them: Cloud Platform, Application Platform, AI Platform, Data Platform, Agent Control Plane and Agent Project.
- An **MCP server** is a governed tool or context interface with ownership, identity, lifecycle and telemetry requirements.
- A **data product** is a governed source of enterprise context with ownership, consumer scope, lineage, freshness, retention and permission-trimming expectations.
- The supplied material uses Phase 0 to Phase 4 for its implementation roadmap; this repository uses G0 to G7 for harness gates. References to the supplied roadmap are written as concept roadmap Phase N.
- The word federated appears in the supplied material both as a delivery principle for project teams and as one of two ownership models. The approved mandate supports centralized platform operation and multiple federated operations and selects neither.
