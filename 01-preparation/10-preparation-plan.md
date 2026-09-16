# Preparation Plan

> Status: Draft
> Canonical owner: Product or program lead - name to be assigned
> Required reviewers: CIO sponsor, business owner, solution architect, engineering lead
> Entry gate: G0 - Framing sufficient for preparation; accepted 2026-09-01 via [`GATE-EVENT-001`](17-gate-register.md#gate-decision-history)
> Exit gate: G1 - Preparation baseline accepted
> Last reviewed: Not reviewed

## Purpose

Convert the framing package into an executable, governed program baseline: narrative, objectives, scope, deliverables, roles, dependencies, evidence expectations, and gate criteria.

## Work packages

| Task ID | Task | Depends on | Output | Complete when | Status | Evidence |
|---|---|---|---|---|---|---|
| `TASK-PREP-01` | Reconcile framing | [G0 Accepted](17-gate-register.md#gate-decision-history) | Framing consistency findings | Conflicts and missing evidence are recorded | In progress | Preparation content reconciled to the framing artifacts; every substantive statement restates supplied material or the approved mandate |
| `TASK-PREP-02` | Build stakeholder narrative | `TASK-PREP-01` | [11-narrative.md](11-narrative.md) | Current and future experience has a bounded story; platform lifecycle scenarios constitute the end-to-end flow | In progress | Role narrative and the supplied functional implementation scenarios `SCN-001`-`SCN-010` in [11-narrative.md](11-narrative.md); platform lifecycle scenarios serve as the end-to-end flow (user clarification 2026-09-01) |
| `TASK-PREP-03` | Define measurable objectives | `TASK-PREP-01` | [12-objectives.md](12-objectives.md) | Objectives are traceable to goals and lifecycle scenarios | In progress | `OBJ-001`-`OBJ-007` restate the supplied MVP definition of done as MVP completion criteria, not blueprint-wide objectives; baselines and targets are recorded as not supplied |
| `TASK-PREP-04` | Set scope and exclusions | `TASK-PREP-02`, `TASK-PREP-03` | [13-scope.md](13-scope.md) | Scope, exclusions and deferrals are explicit | In progress | `SCP-001`-`SCP-015` restate the supplied scope statements and the approved mandate |
| `TASK-PREP-05` | Define deliverables and acceptance | `TASK-PREP-04` | [14-deliverables.md](14-deliverables.md) | Each deliverable has an owner role, inputs, acceptance, and evidence | In progress | `DEL-001`-`DEL-006` define role owners, bounded acceptance and evidence expectations |
| `TASK-PREP-06` | Establish governance and traceability | `TASK-PREP-01` | [15-governance.md](15-governance.md), registers | Roles, lifecycle, identifiers, change control, and gates are usable | In progress | Governance roles and registers reconciled; Requesting user — G0 gate authority is assigned; G1-G7 and operating-model decision authorities remain explicitly unassigned |
| `TASK-PREP-07` | Prepare G1 review | `TASK-PREP-02`-`TASK-PREP-06` | Gate recommendation | Conditions and unresolved dependencies are visible | In progress | G1 readiness recommendation and conditions in [17-gate-register.md](17-gate-register.md); no gate decision recorded |

## G1 criteria

- Objectives trace to supplied statements, assumptions, and goals.
- Objectives and deliverables identify the scenario steps whose outcomes they cover.
- Scope is sufficient to define a thin, testable end-to-end platform enablement flow.
- Deliverables have acceptance criteria and evidence expectations.
- Accountable roles and decision authorities are named or explicitly unassigned.
- Change, risk, ADR, and gate processes are usable.
- The default final delivery is the architecture-validated scenario and decision package.
- Downstream phases can identify their inputs without copying the baseline.

## Input change and replay

| Changed input | Rerun first | Then inspect |
|---|---|---|
| Framing meaning or goal | `TASK-PREP-01`-`TASK-PREP-05` as linked | All phases and gates |
| Objective or measure | `TASK-PREP-03` | Design acceptance, tests, sizing, claims |
| Scope or exclusion | `TASK-PREP-04`, `TASK-PREP-05` | Design, ADRs, backlog, cost, operating model |
| Governance or authority | `TASK-PREP-06` | Controlled headers, ADRs, gate records |
| Deliverable acceptance | `TASK-PREP-05` | Phase plans, tests, presentation evidence |

Use [16-change-impact-register.md](16-change-impact-register.md) to select the smallest replay set. Do not reopen unaffected accepted work without a traceable dependency.
