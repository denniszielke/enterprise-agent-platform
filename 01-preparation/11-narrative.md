# Project Narrative

> Status: Draft
> Canonical owner: Business owner - name to be assigned
> Required reviewers: CIO sponsor, product or program lead, solution architect
> Gate: G1
> Last reviewed: Not reviewed

## One-sentence change

This platform investment enables developer teams to build business solutions faster through streamlined governance, release management, and cost management, using a company-wide agent-platform blueprint that supports either centralized platform operation or multiple federated operations.

## Current experience

Teams commonly define their own protocols, discovery mechanisms, orchestration patterns, roles, accountability and interpretation of business meaning, and project-local decisions about subscriptions, network access, model endpoints, secrets, tool connections, telemetry, cost attribution and lifecycle ownership prevent identity, security, governance, observability and compliance from following every interaction from source to context, agent and action.

## Future experience

As stated in the supplied material, agent project teams no longer ask basic platform questions from scratch. They do not invent their own model endpoint strategy, decide independently how secrets are handled, create unmanaged telemetry, design their own cost attribution, register tools manually in isolated documents or negotiate basic network patterns for every workload. A project team begins with a known platform pattern and receives an approved runtime option, a managed identity model, private connectivity patterns, access to the model gateway, approved data or tool interfaces, logging and tracing requirements, deployment automation and clear ownership metadata. Its work then becomes selecting the relevant business process, designing the user experience, composing agents or workflows, grounding the solution in trusted data, validating quality and proving impact.

The blueprint supports either one central platform team owning the enterprise foundations and the full agent lifecycle, or a federated model in which the central platform owns the responsibilities that must remain consistent while domain teams choose solution patterns, runtimes and user experiences and then build and operate agents within those guardrails. Both options are built on the same 24 capabilities and architecture. This narrative selects neither.

## Roles

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

## Platform enablement lifecycle coverage

A representative business scenario is not required for this platform investment (user clarification 2026-09-01). The functional implementation scenarios `SCN-001` to `SCN-010` in [../00-framing/03-scenario.md](../00-framing/03-scenario.md) constitute the traceable platform lifecycle and value chain. No representative business-solution slice is selected.

## Narrative boundaries

- The narrative selects neither centralized platform operation nor multiple federated operations.
- Product names in the supplied material are its reference implementation; the material states that equivalent products can be substituted when they satisfy the same contract and controls.
- Excluded: a mandate for one agent SDK, orchestration framework or user-interface technology; replacement of existing enterprise API, data, cloud or application platforms; unrestricted autonomous write access to enterprise systems.
- Separate design boundary: a customer-facing, multi-tenant control plane or acceptance of identities from other tenants requires a separate tenant-isolation design.
- No baseline, threshold, target, measured benefit, compliance status, implementation result or production-readiness claim is made in this preparation baseline.
