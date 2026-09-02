# Risk Register

> Status: Draft
> Canonical owner: Product or program lead - name to be assigned
> Required reviewers: Owners of affected outcomes, controls, and gates
> Gate: Continuous
> Last reviewed: Not reviewed

Every risk below restates a risk, mistake or condition stated in the supplied material. No scoring method, risk appetite, owner assignment or treatment plan was supplied, so those cells record that state rather than an invented value.

| ID | Risk or condition as supplied | Consequence as supplied | Likelihood | Impact | Exposure | Treatment | Owner role | Linked artifacts | Status |
|---|---|---|---|---|---|---|---|---|---|
| `RISK-001` | Central ownership without sufficient capacity for forecast demand | A central delivery bottleneck instead of accelerated delivery | Not scored | Not scored | Method not supplied | Not supplied | Not supplied | `GOAL-003`, `SCN-001` | Open |
| `RISK-002` | Federating delivery while guardrails still depend on human review rather than pipeline and gateway enforcement | Federation distributes risk while the central team remains accountable for it | Not scored | Not scored | Method not supplied | Not supplied | Not supplied | `VIS-001`, `SCP-011` | Open |
| `RISK-003` | The operating-model decision guidance warns that deciding before the end of Phase 2 relies on assumptions, while the centralized MVP roadmap requires a centralized choice in its Phase 0 charter | The supplied material does not reconcile the decision timing | Not scored | Not scored | Method not supplied | Not supplied | Not supplied | `GOAL-006`, `SCP-011` | Open |
| `RISK-004` | Manual tagging in the cost attribution chain | Cost attribution never becomes reliable | Not scored | Not scored | Method not supplied | Not supplied | Not supplied | `GOAL-005`, `OBJ-007`, `SCN-003` | Open |
| `RISK-005` | Granting direct model access for speed | Metering and safety gaps that are painful to close | Not scored | Not scored | Method not supplied | Not supplied | Not supplied | `OBJ-003`, `SCN-003` | Open |
| `RISK-006` | Building the registry and marketplace first | Empty catalogues and no reuse to capture | Not scored | Not scored | Method not supplied | Not supplied | Not supplied | `GOAL-004`, `SCN-006` | Open |
| `RISK-007` | Skipping evaluation until the agent stabilises | The agent can never be safely changed | Not scored | Not scored | Method not supplied | Not supplied | Not supplied | `OBJ-002`, `SCN-008` | Open |
| `RISK-008` | Registry product features remain subject to tenant availability, licensing and product maturity | The logical registry and identity requirements remain mandatory and may need an interim implementation | Not scored | Not scored | Method not supplied | Not supplied | Not supplied | `ASM-007`, `SCN-006` | Open |
| `RISK-009` | Capability ownership assigned implicitly rather than deliberately | The operating-model choice is made by accident instead of as a deliberate decision | Not scored | Not scored | Method not supplied | Not supplied | Not supplied | `VIS-013`, `GOAL-006`, `SCP-011` | Open |

## Risk rules

- State uncertainty as a risk, a current problem as an issue, and an unverified belief as an assumption.
- Define the scoring method and risk appetite before comparing exposures.
- Link treatment actions to phase tasks, implementation items, controls, tests, evidence, and decision owners.
- Only the named authority may accept residual risk.
- Reassess a risk when its trigger, linked assumption, ADR, evidence, exposure, or treatment changes.

## Review summary

| Gate | Blocking risks | Residual-risk decisions needed | Evidence gaps |
|---|---|---|---|
| G0 | None identified in the framing content | None recorded | None — platform lifecycle scenarios serve as the end-to-end flow |
| G1 | None identified in the preparation content | None recorded | G1 gate authority is not assigned |
| G2-G7 | Not assessed | Not assessed | Not assessed |
