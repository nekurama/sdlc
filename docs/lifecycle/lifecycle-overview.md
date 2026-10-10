# Universal work lifecycle

**Scope:** This lifecycle applies across the whole Nekurama business, for technical and non-technical work alike. Work type determines the specific artifacts, acceptance criteria, reviewers, and evidence; it does not replace the universal lifecycle.

**Status:** Working baseline. The complete transition matrix, named approval roles, and evidence gates are not yet finalized. See [nekurama/Bulb#7](https://github.com/nekurama/Bulb/issues/7).

Stages describe **where** work is. States describe **what is happening now**. They are independent dimensions; changing a state does not automatically advance the stage.

## Stages

| Order | Stage | Purpose | Typical outputs |
|---:|---|---|---|
| 1 | Research / Discovery | Understand the problem, opportunity, evidence, assumptions, and feasibility | Findings, problem statement, assumptions |
| 2 | Specification | Define required outcomes and constraints | Requirements, BRD/TRD, epics, stories, briefs |
| 3 | Planning / Design | Decide how to deliver the outcome | Solution design, dependencies, estimates, plan |
| 4 | Tasking / Readiness | Make work actionable and assignable | Work items, owners, acceptance criteria, sequencing |
| 5 | Execution / Production | Produce the deliverable | Code, documents, designs, media, reports, operational changes |
| 6 | Review / Validation | Verify correctness, quality, and suitability | Reviews, tests, fact checks, approvals, evidence |
| 7 | Integration / Delivery | Make the accepted outcome available to its recipient | Merge, deployment, publication, handover, delivery |
| 8 | Operate / Maintain | Keep the outcome useful and respond to later issues | Monitoring, feedback, fixes, updates, improvements |

## Universal states

| State | Baseline meaning |
|---|---|
| Draft | Being defined; not ready to execute |
| Ready | Scope, owner, criteria, and prerequisites are sufficiently clear |
| Active | Authorized work is underway |
| Blocked | A dependency, decision, resource, or external condition prevents progress |
| InReview | A deliverable is submitted and awaits required review |
| Accepted | The deliverable passed applicable review and acceptance checks |
| Completed | Required delivery and handover conditions are fulfilled |
| Cancelled | Work was explicitly withdrawn or stopped; history is preserved |

“Changes requested” is a review decision that returns work to Active, not a universal state. “Overdue,” “At risk,” “High priority,” and “Needs approval” are normally fields or flags, not lifecycle states.

## Regression and rework

The lifecycle is not a one-way funnel. Return to the earliest stage whose output is no longer valid, preserving earlier work and decisions for traceability.

Examples:

- Defect found in review → Execution.
- Design found inadequate → Planning / Design.
- Requirements missing or contradictory → Specification.
- New evidence invalidates the problem → Research / Discovery.
- Task breakdown reveals missing dependency → Tasking / Readiness or Planning / Design.
- Delivery check fails → appropriate earlier stage, often Execution or Review.
- Operational feedback reveals new work → create a linked maintenance or improvement item.

## Decision distinctions

- **Eligibility:** whether the item is in a state and stage where execution may be proposed.
- **Execution authorization:** a human has approved the specific plan and scope, or a narrowly scoped action is covered by explicit pre-authorization.
- **Acceptance:** the applicable reviewer confirms the deliverable meets its criteria using evidence.
- **Completion:** required delivery and handover conditions are fulfilled after acceptance.

A Ready item is not automatically authorized. A successful agent run does not automatically mean Accepted or Completed. Parent completion requires required child work to finish and the parent's own acceptance criteria to pass.

## Open contract work

The implementable transition table, guards, actors, evidence, exception paths, and hierarchy semantics are being completed in [#7](https://github.com/nekurama/Bulb/issues/7). This document must be updated when that contract is reviewed.
