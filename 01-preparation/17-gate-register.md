# Gate Register

> Status: Draft
> Canonical owner: Product or program lead - name to be assigned
> Required reviewers: Gate authority and affected phase owners
> Gate: G0-G7
> Last reviewed: Not reviewed

Agents and phase owners may write readiness recommendations. Only an actual gate authority may record a decision.

| Gate | Scope or baseline | Readiness recommendation | Evidence reviewed | Decision | Authority | Date | Conditions, risks, or follow-up |
|---|---|---|---|---|---|---|---|
| G0 | Framing baseline for the approved company-wide agent-platform blueprint | Ready for authority decision | [Scenario](../00-framing/03-scenario.md), [vision](../00-framing/01-vision.md), [assumptions](../00-framing/02-assumptions.md), [business goals](../00-framing/04-business-goals.md), [risks](18-risk-register.md) | Accepted | Requesting user — G0 gate authority | 2026-09-01 | Framing restates the supplied material and the approved mandate, and separates supplied statements from stated assumptions. The user confirmed (2026-09-01) that this is a platform investment and no representative business scenario is required; the functional implementation scenarios serve as the end-to-end lifecycle. Operating-model selection is not a G0 condition |
| G1 | Preparation baseline for the company-wide blueprint | Recommend Ready with conditions — preparation baseline populated from supplied material and platform lifecycle scenarios; G1 gate authority not assigned — agent recommendation, not a decision | [Narrative](11-narrative.md), [objectives](12-objectives.md), [scope](13-scope.md), [deliverables](14-deliverables.md), [governance](15-governance.md), [risks](18-risk-register.md) | Not decided | Gate authority - not assigned | - | Narrative, objectives, scope, deliverables and governance are populated from supplied material. The platform lifecycle scenarios constitute the end-to-end flow per user clarification 2026-09-01. No G1 gate authority is assigned, so no G1 decision can be recorded |
| G2 | Design | Not assessed | [Links] | Not decided | [Role/name] | - | [Open actions] |
| G3 | Architecture | Not assessed | [Links] | Not decided | [Role/name] | - | [Open actions] |
| G4 | Implementation handoff | Not assessed | [Links] | Not decided | [Role/name] | - | [Open actions] |
| G5 | Delivery effort, sizing model, and validation plan | Not assessed | [Links] | Not decided | [Role/name] | - | [Open actions] |
| G6 | Operating model and readiness plan | Not assessed | [Links] | Not decided | [Role/name] | - | [Open actions] |
| G7 | Architecture-validated scenario and decision package | Not assessed | [Links] | Not decided | [Role/name] | - | [Open actions] |

Readiness note 2026-09-01: G0 was accepted on 2026-09-01 by Requesting user — G0 gate authority (GATE-EVENT-001). The G1 recommendation above was produced by an agent workflow from the supplied material and the approved mandate. It is a recommendation only. No G1 gate event or gate decision has been recorded. G1 gate authority is not assigned.

## Decision values

- `Not decided`
- `Accepted`
- `Accepted with conditions`
- `Hold`
- `Returned`

If a changed input invalidates evidence or a gate condition, link the `CHG-NNN` record and mark the readiness recommendation for reassessment. Preserve the original decision record and add a dated review note rather than silently replacing history.

## Gate decision history

Append one row per actual decision or reassessment. The summary above shows current state; this table preserves history.

| Event ID | Gate | Baseline or change | Date | Authority | Decision | Evidence reviewed | Conditions, dissent, and accepted risk | Supersedes event |
|---|---|---|---|---|---|---|---|---|
| `GATE-EVENT-001` | G0 | [Framing baseline for the approved company-wide agent-platform blueprint](../00-framing/00-framing-plan.md) | 2026-09-01 | Requesting user — G0 gate authority | Accepted | [Scenario](../00-framing/03-scenario.md), [vision](../00-framing/01-vision.md), [assumptions](../00-framing/02-assumptions.md), [business goals](../00-framing/04-business-goals.md), [risks](18-risk-register.md) | None | Not applicable |
