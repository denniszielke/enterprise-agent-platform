# Vision

> Status: Accepted
> Canonical owner: Not supplied
> Required reviewers: Not supplied
> Gate: G0
> Last reviewed: 2026-09-01

## Mandate

The mandate is approved and sponsored by the CIO. Its objective is a company-wide agent-platform blueprint that supports either centralized platform operation or multiple federated operations. Neither operating-model alternative is selected here. Funding and sponsorship mechanics are not material to this framing.

## Mission

Give the enterprise a governed, reusable and resilient foundation for building and operating agents. This is a platform investment: it enables developer teams to build business solutions faster through streamlined governance, release management, and cost management. Reduce the amount of foundational work each agent project team has to solve on its own, while increasing the trust, observability, security and accountability with which agents, agent-enabled applications, MCP servers, models, tools and data products are created and operated. The goal is not to standardise every agent or solution; it is to standardise the conditions under which many different agents and solutions can be built safely, quickly and repeatedly.

The blueprint establishes an open, scalable ecosystem in which business and technology teams compose agents, models, tools, data products and enterprise services across multiple runtimes and delivery channels. Rather than prescribing a single technology path, it provides shared standards, reusable capabilities and governed interoperability so that teams can select the right components for each business scenario while remaining aligned with enterprise-wide security, identity, data and operational requirements.

## Why the blueprint matters

- Enterprises are moving from isolated AI experiments towards portfolios of agent-enabled products, services and processes; the challenge is to create an operating environment in which many teams can deliver many solutions without repeatedly rediscovering the same security, identity, networking, model management, observability and governance patterns.
- As portfolios grow, the decisive scaling constraint becomes reusable enterprise context rather than the number of available models.
- When each project makes local decisions about subscriptions, network access, model endpoints, secrets, tool connections, telemetry, cost attribution and lifecycle ownership, identity, security, governance, observability and compliance cannot consistently follow every interaction from source to context, agent and action. The enterprise then struggles to answer who owns an agentic asset, what data it can reach, which identity and model it used, what it cost, how it was evaluated and what evidence exists for compliance.
- The committed 24 capabilities are broader than a model gateway, broader than a Foundry setup and broader than an application runtime; they describe the full operating surface required to build, govern, secure, observe and scale AI workloads.
- Deciding, per capability, whether it is owned centrally, owned by domains or shared is the operating-model choice, and it is the decision most often made by accident.

## Future-state outcomes

- A project receives a usable environment, identities, model contract, telemetry and deployment path rather than an empty subscription.
- Platform controls are implemented once and inherited by projects.
- Each model call, tool call and state-changing action is attributable to a user, workload and agent.
- Shared agents, tools and MCP servers are discoverable, owned, versioned and governed.
- Quality, safety, cost and operational evidence are available before and after production release.
- A model, runtime or implementation product can be replaced without changing the platform's logical contracts.
- The platform is not perceived as extra governance overhead but as the fastest and safest path to production.

## Principles and guardrails

These principles and guardrails restate the architecture principles, lifecycle structure and capability-ownership rule in the supplied material. None of them is an accepted architecture decision.

| ID | Principle or guardrail | Design consequence |
|---|---|---|
| `VIS-001` | Centralize systemic controls and federate solution delivery | Identity policy, model mediation, registry, network baselines, security signals and minimum telemetry are central. Business logic, prompts, tools, user experience and project evaluation remain with the Agent Project team |
| `VIS-002` | Treat every agent as a workload identity | Human identity, agent identity and runtime identity are related but not interchangeable; authorization decisions identify the actor, the agent and the requested resource |
| `VIS-003` | Separate model, agent and tool gateways logically | They may share gateway infrastructure, but they have different policies, owners, scaling profiles and audit requirements |
| `VIS-004` | Keep business process state out of prompts | Durable process state, approvals, retries and compensating actions belong in workflow and state services |
| `VIS-005` | Use private connectivity by default | Public ingress is deliberate, authenticated and protected; platform-to-platform traffic stays on private enterprise paths where supported |
| `VIS-006` | Deny static keys where managed identity is supported | Credentials that remain necessary are stored in a vault, rotated and never embedded in code or agent instructions |
| `VIS-007` | Make write actions explicit | Read tools and transaction tools use different scopes, policies and approval requirements; high-impact writes require deterministic validation and, where appropriate, human confirmation |
| `VIS-008` | Evaluate the system, not only the model | Acceptance covers retrieval, reasoning, tool selection, authorization, workflow outcome, latency, cost and safety |
| `VIS-009` | Design regional workloads for failure | A regional project remains the default, but dependencies have declared failover, degradation and recovery behavior |
| `VIS-010` | Automate registration and evidence | Deployment pipelines update inventory and attach evaluation, security and operational evidence to the released version |
| `VIS-011` | Keep the capability set and architecture invariant to the ownership model | The ownership decision determines who builds and operates agents; it does not change the 24 capabilities the platform must provide, and the hub-and-spoke concept keeps a later ownership change from becoming a re-architecture |
| `VIS-012` | Treat Build, Scale, Govern and Optimize as a cross-cutting lifecycle overlay | The four lifecycle pillars are applied across the six building blocks so that runtime, governance or quality does not become the responsibility of one product or one team |
| `VIS-013` | Give every capability exactly one accountable owner | Ownership is recorded per capability as central, domain or shared; writing the ownership column explicitly turns an implicit product decision into a deliberate operating-model choice |

## Non-goals

- Standardising every agent or solution rather than the conditions under which many different agents and solutions can be built safely, quickly and repeatedly.
- A mandate for one agent SDK, orchestration framework or user-interface technology.
- Prompt-hosted agents as the default runtime for workloads requiring direct private network access; their use can be evaluated separately when their networking and hosting characteristics satisfy the project requirements.
- Replacement of existing enterprise API, data, cloud or application platforms.
- Unrestricted autonomous write access to enterprise systems.
- A claim that every feature of another vendor's agent platform has an exact product equivalent.
- Selection between centralized platform operation and multiple federated operations; the blueprint supports both alternatives and selects neither.

## Separate design boundary

A customer-facing, multi-tenant control plane or acceptance of identities from other tenants requires a separate tenant-isolation design.

## Product references

Product names used in the supplied material are its reference implementation. The material states that equivalent open-source, marketplace or commercial products can be substituted when they satisfy the same contract and controls. No product choice is accepted in this framing.
