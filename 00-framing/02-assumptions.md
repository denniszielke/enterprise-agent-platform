# Assumptions

> Status: Accepted
> Canonical owner: Not supplied
> Required reviewers: Not supplied
> Gate: G0 and continuous review
> Last reviewed: 2026-09-01

The entries below are the assumptions and design boundaries stated as such in the supplied material, restated with their original qualifications. They are stated assumptions, not verified facts about any environment.

| ID | Domain | Assumption or design boundary as supplied |
|---|---|---|
| `ASM-003` | Platform | The reference design is an internal enterprise platform in one identity tenant, shared across business domains with project-level isolation. Building a customer-facing, multi-tenant SaaS control plane or accepting identities from other tenants requires a separate tenant-isolation design |
| `ASM-004` | Platform | Hub-and-spoke networking is established. Centrally managed components such as firewalls and shared egress live in the hub, together with shared DNS and inspection, while application, data and AI platforms are implemented as spokes with defined ingress and egress patterns. Private network consumption is the default for most enterprise resources, including models, gateways, agents, MCP servers, data stores and platform services, unless a specific scenario requires public exposure for user access or external integration |
| `ASM-005` | Platform | Application hosting for custom agents and MCP servers primarily uses containers, with managed Kubernetes and container-app services as the main runtime options. Prompt-hosted agents are not treated as the primary scoped runtime where current limitations make container-hosted agents the required pattern |
| `ASM-006` | Security | Key-based authentication for models, storage accounts and other resources is assumed to be denied by policy where possible. User-assigned managed identities, workload identities and directory-based authentication patterns are the preferred control model |
| `ASM-007` | AI | Registry product features are used subject to tenant availability, licensing and product maturity. The logical registry and identity requirements remain mandatory even when an interim implementation is required |
| `ASM-015` | Platform | The cloud platform is available across multiple regions while individual workloads are deployed and consumed as regional resources; an agent project is regional unless its business continuity tier requires a second deployment |
| `ASM-016` | AI | Model deployments can be global, data-zone or regional and can use provisioned or consumption capacity. The model gateway hides deployment location and capacity selection from consumers and can abstract model hosting across regions where capacity and redundancy require it |
| `ASM-017` | Platform | Agent project resources are placed in a dedicated subscription or resource group with delegated permissions and inherited policy |
| `ASM-018` | Experience | User interfaces can be custom web or mobile applications, collaboration-platform applications or assistant agents. Internet-facing channels terminate at approved edge and ingress services |
| `ASM-019` | Security | User-assigned managed identities and workload identity federation are pre-provisioned where practical |
| `ASM-020` | Platform | Model gateway and API or MCP gateway patterns are the supported path for many model, tool and MCP consumption scenarios. Exceptions can exist, but they should be deliberate architecture decisions with explicit control, telemetry and cost trade-offs |
| `ASM-021` | Security | The default identity unit is one workload identity per registered agent and environment. Replicas of that deployment share the identity; unrelated agents do not. A registry record can map to separate development, test and production identities, while the release manifest and trace identify the exact deployed version |

## Review rule

When an assumption changes, create a `CHG-NNN` record before updating dependent artifacts. Preserve the old statement and evidence when it influenced an accepted gate or decision.
