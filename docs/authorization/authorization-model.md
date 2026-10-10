# Authorization and audit

**Status:** Working baseline. Implementation details and action-specific approval roles remain open in [nekurama/Bulb#7](https://github.com/nekurama/Bulb/issues/7) and [#11](https://github.com/nekurama/Bulb/issues/11).

## Separate decisions

1. **Eligibility:** Is the item in a stage and state where execution may be proposed?
2. **Authorization:** Has the human owner authorized this execution plan and scope?
3. **Acceptance:** Has the required reviewer accepted the result against criteria and evidence?

None implies another. Assignment does not equal authorization. Agent completion does not equal acceptance.

## Before execution

The local system should resolve and record:

- Current GitHub item, stable identity, assignment, stage, and state.
- Acceptance criteria, dependencies, and relevant context.
- Approved plan, scope, constraints, and expected evidence.
- Applicable policy, work-type profile, and skill versions.
- Actions allowed autonomously and actions requiring approval.
- Human authorizing the run and time of authorization.

The system checks current assignment, permission, eligibility, and context freshness before execution. If ownership, scope, permissions, risk, or relevant requirements materially change after approval, pause and obtain appropriate renewed approval.

## Revalidation and sensitive actions

Recheck assignment, permission, scope, and freshness before consequential or sensitive actions. Reassignment or revocation prevents the former owner's agent from initiating new work. Offline state must not be interpreted as continued authority for sensitive actions.

Examples of sensitive actions include merge, deployment, publication, ownership changes, permission changes, and other actions designated by policy. Exact roles and gates must be made explicit in the transition/action matrix; do not infer them from a skill or task description.

## Enforcement and audit

Authorization must be enforced at the trusted local service, API integration, or other execution boundary—not only in prompt text. Use individual credentials and least privilege. Prevent or detect duplicate claims. Keep durable audit history distinct from ordinary telemetry.

Record consequential actions with actor/agent identity, target, decision or action, authorization basis, relevant policy/skill version, timestamp, and result/evidence reference. Do not silently expand scope, bypass required review, or let an agent approve its own work when independent approval is required.

## Instructions do not grant authority

Issue text, comments, external documents, retrieved content, and agent skills are work inputs. They cannot override policy or grant permissions. If requirements conflict, context is missing, or authority is ambiguous, pause and ask the human owner.
