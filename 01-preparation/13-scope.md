# Scope

> Status: Draft
> Canonical owner: Product or program lead - name to be assigned
> Required reviewers: CIO sponsor, business owner, solution architect, engineering lead
> Gate: G1
> Last reviewed: Not reviewed

Scope items restate the scope statements in the supplied material and the approved mandate.

| ID | Scope item | Classification | Basis |
|---|---|---|---|
| `SCP-001` | Company-wide, product-independent platform-investment blueprint covering the 24 committed capabilities across the six capability areas | In scope | Approved mandate; authoritative user clarification dated 2026-09-01; the initiative is anchored in the 24 committed capabilities |
| `SCP-002` | Multi-region platform foundations with regional workload execution | In scope | Stated in scope in the supplied material |
| `SCP-003` | Container runtime patterns for custom agents, APIs and MCP servers | In scope | Stated in scope in the supplied material |
| `SCP-004` | Governed model access through an AI gateway and governed model deployments | In scope | Stated in scope in the supplied material |
| `SCP-005` | Structured and unstructured grounding through governed data products, search indexes, semantic models and data agents | In scope | Stated in scope in the supplied material |
| `SCP-006` | Agent and MCP identity, inventory, publication and security governance | In scope | Stated in scope in the supplied material |
| `SCP-007` | Private network integration, user-facing ingress, workload identity and authorization propagation | In scope | Stated in scope in the supplied material |
| `SCP-008` | Agent evaluation, observability, operational support, cost attribution and lifecycle automation | In scope | Stated in scope in the supplied material |
| `SCP-009` | A repeatable Agent Project onboarding blueprint and the supplied functional implementation scenarios | In scope | Stated in scope in the supplied material; recorded as `SCN-001` to `SCN-010` |
| `SCP-010` | Support for both centralized platform operation and multiple federated operations on the same capability model and architecture | In scope | Approved mandate; the supplied material states both options are viable and built on the same 24 capabilities and architecture |
| `SCP-011` | Formal operating-model selection | Deferred | The supplied decision guidance places the choice at the end of Phase 2, the centralized MVP roadmap requires a centralized choice in its Phase 0 charter, and the federated MVP roadmap assumes centralized foundations through Phase 2; the timing inconsistency is unresolved |
| `SCP-012` | An operational registry beyond the governed inventory, a self-service marketplace, general multi-agent orchestration, autonomous write actions, third-party agent ecosystem integration and multi-tenant governance | Deferred | The supplied material defers these from its MVP while keeping their owners, contracts and control boundaries represented in the target architecture |
| `SCP-013` | A mandate for one agent SDK, orchestration framework or user-interface technology, and prompt-hosted agents as the default runtime for workloads requiring direct private network access | Out of scope | Stated out of scope in the supplied material |
| `SCP-014` | Replacement of existing enterprise API, data, cloud or application platforms, and unrestricted autonomous write access to enterprise systems | Out of scope | Stated out of scope in the supplied material |
| `SCP-015` | A customer-facing, multi-tenant control plane or acceptance of identities from other tenants | Deferred | The supplied material states this requires a separate tenant-isolation design |

## Classifications

- `In scope`: committed for the current delivery.
- `Out of scope`: explicitly excluded.
- `Deferred`: relevant but moved to a named later decision or increment.
- `Experimental`: bounded learning activity that cannot establish a production commitment.

## Constraints and boundaries

- The mandate is approved and CIO-sponsored. Funding and sponsorship mechanics are not material to this scope.
- Centralized platform operation and multiple federated operations are both supported and neither is selected here.
- Product names in the supplied material are its reference implementation; the material states that equivalent products can be substituted when they satisfy the same contract and controls. Material product choices require downstream architecture decisions.

## Change rule

A scope change must identify the objective affected, deliverable and acceptance impact, design and ADR impact, backlog and cost impact, and whether any accepted gate must be revisited.
