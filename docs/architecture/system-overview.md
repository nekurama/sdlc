# System overview

**Status:** Working baseline, based on the agreed Nekurama/BABAI architecture.

## Purpose

Coordinate **all Nekurama business work**, technical and non-technical, through shared GitHub records while allowing each person to use local AI tools and agents. The same universal lifecycle governs research, strategy, product, operations, marketing, software, and other work; work-type profiles define the artifacts, criteria, and approval gates relevant to each. A human selects eligible work, reviews the proposed plan, authorizes execution, inspects evidence, and makes the applicable acceptance decision.

## System roles

| Part | Responsibility | Boundary |
|---|---|---|
| GitHub | Canonical shared work items, assignment, criteria, dependencies, and lifecycle record | A sync event or assignment is not execution authorization |
| Human owner | Select work, authorize scope, resolve ambiguity, review evidence, accept or reject outcomes | Remains accountable when an agent performs the work |
| ChatGPT | Conversational interface for understanding work, proposing plans, coordinating local execution and presenting evidence | Must not silently expand authority or scope |
| Local Paperclip | Local execution orchestration, agent runs, retries, and local execution records | Its internal task state does not dictate GitHub lifecycle state |
| Local sync component | Fetch and reconcile shared GitHub changes into the local environment | Sync updates context and may notify; it never starts work by itself |
| Policies and skills | Versioned instructions, work-type requirements, and operational procedures | Skills explain how to act; they do not grant authority |

## Authority and source of truth

- GitHub is canonical for shared work.
- Paperclip is canonical for local execution details.
- The lifecycle policy defines valid shared transitions and gates.
- The trusted execution boundary must enforce authorization; prompts alone are insufficient.
- Each person uses their own identity and least-privilege credentials.

## Invariants

1. Sync never implicitly authorizes an agent.
2. Eligibility, explicit authorization, and acceptance are separate checks.
3. Every work item has verifiable acceptance criteria.
4. Agent-reported completion is not human acceptance or lifecycle completion.
5. Assignment, permissions, scope, and context freshness are checked at execution start and revalidated before sensitive actions.
6. Reassignment or revoked permission prevents the previous owner's agents from initiating new work.
7. Duplicate claims must be prevented or safely detected.
8. Consequential actions produce attributable audit records.
9. Stale offline state cannot authorize sensitive actions.
10. Independent Paperclip instances must not use a shared database unless that topology is explicitly supported.

## Work lifecycle and execution lifecycle

The universal lifecycle describes shared work. Paperclip describes a local execution run. They are connected through an explicit mapping, but are not the same state machine. A local run may finish while shared work is Active, InReview, or Accepted. Closing a local run does not force a GitHub transition.

## Current implementation work

The implementation and validation backlog is tracked in [nekurama/Bulb#6](https://github.com/nekurama/Bulb/issues/6). Its first contract dependency is [#7](https://github.com/nekurama/Bulb/issues/7).
