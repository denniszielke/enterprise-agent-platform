# Framing Plan

> Status: Accepted
> Canonical owner: Not supplied
> Required reviewers: Not supplied
> Entry: A problem statement, opportunity, or scenario source
> Exit gate: G0 - Framing sufficient for preparation
> Last reviewed: 2026-09-01

## Purpose

Turn supplied source material into a bounded vision, explicit assumptions, a neutral scenario, and business goals without choosing products or inventing facts.

## Inputs

- The supplied enterprise concept material, integrated directly as framing language.
- The approved, CIO-sponsored enterprise mandate for a company-wide agent-platform blueprint that supports either centralized platform operation or multiple federated operations.
- The authoritative user clarification dated 2026-09-01: no concrete business scenario is required because this is a platform investment intended to enable developer teams to build business solutions faster through streamlined governance, release management, and cost management.

## Work packages

| Task ID | Task | Depends on | Output | Complete when | Status | Evidence |
|---|---|---|---|---|---|---|
| `TASK-FRM-01` | Integrate the supplied material as framing content | Supplied material | Framing artifacts in this folder | Every substantive framing statement is a direct or faithful restatement of supplied material | Complete with evidence | Supplied concept material and the approved mandate are integrated into [01-vision.md](01-vision.md), [02-assumptions.md](02-assumptions.md), [03-scenario.md](03-scenario.md) and [04-business-goals.md](04-business-goals.md) |
| `TASK-FRM-02` | Define vision and guardrails | `TASK-FRM-01` | [01-vision.md](01-vision.md) | Future state, principles, non-goals, and boundaries are reviewable | Complete with evidence | [01-vision.md](01-vision.md) holding the mandate, mission, outcomes, `VIS-001` to `VIS-013` and non-goals |
| `TASK-FRM-03` | Record assumptions and design boundaries | `TASK-FRM-01` | [02-assumptions.md](02-assumptions.md) | Supplied assumptions and design boundaries are restated with their qualifications | Complete with evidence | [02-assumptions.md](02-assumptions.md) holding the supplied assumptions and design boundaries |
| `TASK-FRM-04` | Define business goals | `TASK-FRM-01`, `TASK-FRM-02`, `TASK-FRM-03` | [04-business-goals.md](04-business-goals.md) | Goals restate supplied outcome intent and keep supplied measure names separate from targets | Complete with evidence | [04-business-goals.md](04-business-goals.md) holding `GOAL-001` to `GOAL-006` with supplied measure names recorded as source input |
| `TASK-FRM-05` | Prepare G0 review | `TASK-FRM-01`-`TASK-FRM-04` | Readiness recommendation in [../01-preparation/17-gate-register.md](../01-preparation/17-gate-register.md) | Gaps and conditions are visible | Complete with evidence | G0 readiness recommendation in [the gate register](../01-preparation/17-gate-register.md) and risks in [the risk register](../01-preparation/18-risk-register.md) |

## G0 criteria

- The problem, affected stakeholders, desired change, constraints, and non-goals are explicit.
- The supplied platform lifecycle scenarios provide traceable end-to-end platform enablement and exception coverage; a representative business scenario is not required.
- Supplied statements and assumptions are visibly different.
- Goals are outcome-oriented rather than a product list.
- No unrecorded decision is presented as approved.

## Input change and replay

| Changed input | Rerun first | Then inspect |
|---|---|---|
| New or corrected supplied material | `TASK-FRM-01` | Vision, assumptions, goals, all downstream links |
| Business-priority change | `TASK-FRM-02`, `TASK-FRM-04` | Objectives, scope, design priorities, presentation |
| Assumption change | `TASK-FRM-03` | Every artifact linked to the assumption |
| Constraint or non-goal change | `TASK-FRM-02` | Scope, design, ADRs, backlog, sizing, operations |

Record every material change as `CHG-NNN` in the [change impact register](../01-preparation/16-change-impact-register.md). Reopen G0 only when the accepted framing meaning or gate conditions changed.
