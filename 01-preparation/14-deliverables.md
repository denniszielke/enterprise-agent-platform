# Deliverables

> Status: Draft
> Canonical owner: Product or program lead - name to be assigned
> Required reviewers: Deliverable owners and gate authority
> Gate: G1 and downstream gates
> Last reviewed: Not reviewed

| ID | Deliverable | Owner role | Inputs | Acceptance criteria | Required evidence | Due gate | Status |
|---|---|---|---|---|---|---|---|
| `DEL-001` | Architecture-validated scenario and decision package | Product or program lead - not assigned | G0-G6 packages | Meets the canonical definition and assessment rules in [the architecture-validated scenario](../07-presentation/76-validated-scenario.md) | Phase reviews, accepted ADRs, estimates, and cited external evidence where available | G7 | Draft |
| `DEL-002` | Company-wide, product-independent agent-platform blueprint | Solution or enterprise architect - not assigned | [Framing artifacts](../00-framing/03-scenario.md); `SCP-001` to `SCP-010` | Covers the 24 committed capabilities, the six building blocks, the Build, Scale, Govern and Optimize lifecycle concerns and both operating-model alternatives without selecting one and without an implied product choice | Trace review from goals, objectives, scope and lifecycle scenarios into design and architecture | G3 | Draft |
| `DEL-003` | Platform enablement lifecycle coverage definition | Business owner - not assigned | `SCN-001` to `SCN-010`; `OBJ-001` to `OBJ-007` | The functional implementation scenarios constitute the traceable platform lifecycle and value chain; no named business scenario or representative business-solution slice is required (user clarification 2026-09-01) | Reviewed functional-scenario coverage and the downstream test and validation plan | G2 | Draft |
| `DEL-004` | Capability accountability and operating-model decision package | Product or program lead - not assigned | `SCP-010`, `SCP-011`; [governance](15-governance.md) | Shows both ownership alternatives, exactly one accountable owner per capability, the supplied decision criteria and readiness conditions, and the record contents the supplied material requires, without preselecting a model | Proposed ADR with a capability responsibility mapping and cited criteria evidence; acceptance only by the named authority | Not supplied | Draft |
| `DEL-005` | Objectives and measurement definition baseline | Test and evidence lead - not assigned | `OBJ-001` to `OBJ-007`; supplied measure names in [business goals](../00-framing/04-business-goals.md) | Every objective states the supplied outcome it restates and records that no baseline, threshold, target, population, window or date was supplied | Reviewed measurement definitions and evidence-gap record; no measured result claimed | G5 | Draft |
| `DEL-006` | Governance and lifecycle responsibility model | Product or program lead - not assigned | `VIS-011`, `VIS-012`, `VIS-013`; [governance](15-governance.md) | Build, Scale, Govern and Optimize responsibilities, artifact authority, change control and gate authority slots are explicit for either operating-model alternative | Governance review and downstream operating-model trace; assignments remain role placeholders until supplied | G6 | Draft |

## Deliverable rules

- A file existing is not acceptance evidence.
- Acceptance criteria must be observable and bounded.
- Deliverables that depend on an unresolved material choice link to its ADR.
- Production readiness, compliance, scale, and operating effectiveness require their own evidence.
- `DEL-001` is the default integrated architecture-harness delivery. Refine its scope and decision audience without removing its end-to-end traceability.
