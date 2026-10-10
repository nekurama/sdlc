# Nekurama SDLC

Shared lifecycle, governance, policies, and operating guides for **all Nekurama business work**, across Nekurama and BABAI.

This repo defines the company-wide way of working for both **technical and non-technical work**: business strategy, research, product, operations, marketing, finance, people processes, software, and other company work. The lifecycle is universal; work-type guidance adds the artifacts, criteria, and approvals appropriate to each kind of work. Here, “SDLC” names the shared work lifecycle, not a software-only process.

This repository explains **how we organize, authorize, execute, review, deliver, and maintain work**. It is a documentation and governance home. Executable Paperclip integration, sync services, adapters, and installation code belong in a separate implementation repository when that work is started.

## Working principles

- GitHub is canonical for shared work; each person's local Paperclip instance is canonical for local execution.
- Synchronization and assignment never authorize execution.
- Eligibility, execution authorization, review acceptance, and lifecycle completion are separate decisions.
- Human owners remain accountable for authorized work and acceptance.
- Agents operate only within approved scope and applicable policy.
- Consequential actions require enforced permission checks and auditable evidence.
- Work may regress to the earliest lifecycle stage whose output is no longer valid; history is preserved.
- Policies, templates, and skills are versioned and reviewed.

## Repository map

- [Architecture](docs/architecture/system-overview.md) — system roles, boundaries, and invariants.
- [Lifecycle](docs/lifecycle/lifecycle-overview.md) — stages, states, and the current contract status.
- [Authorization](docs/authorization/authorization-model.md) — eligibility, approval, revalidation, and audit requirements.
- [Ways of working](docs/operations/working-agreement.md) — shared norms for human and AI work.
- [Local Paperclip setup](docs/setup/paperclip-local-setup.md) — intended setup guide; exact product behavior must be verified before instructions are finalized.
- [Work item template](templates/work-item.md) — reusable work definition.
- [Decision record template](templates/decision-record.md) — record material decisions and their evidence.
- [Interactive lifecycle guide](site/index.html) — browser-based stages, transitions, state management, and department journeys.
- [Webapp notes](docs/webapp/README.md) — design scope and hosting status.
- [Implementation roadmap](docs/roadmap.md) — links to the active GitHub workstream.

## Status and change control

Documents identify whether they are a working baseline, draft, or verified procedure. Do not treat a draft as an approved implementation contract. Material changes should link the question, evidence, decision, implementation or validation, and resulting document update.

The current lifecycle contract is being specified in [nekurama/Bulb#7](https://github.com/nekurama/Bulb/issues/7). Until that work is reviewed and incorporated here, this repository records the agreed baseline without claiming that every transition and approval rule is final.
