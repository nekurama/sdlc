# Local Paperclip setup

**Status:** Outline only. Do not use this as an installation procedure yet. The exact Paperclip version, supported API/MCP connectivity, adapters, wake-up behavior, continuation limits, and installation model must be verified in [nekurama/Bulb#9](https://github.com/nekurama/Bulb/issues/9).

## Intended model

Each person runs an independently managed local environment containing Paperclip, a local database, agent adapters, approved configuration, skills, and required credentials. Each user's ChatGPT connects to that person's local Paperclip service through a supported API or MCP path.

GitHub remains the shared coordination layer. Local Paperclip remains the execution layer. Do not point independent Paperclip instances at a shared database unless the topology is explicitly supported.

## Sections to complete after technical proof

1. Supported operating systems and prerequisites.
2. Version pinning and installation steps.
3. Local database setup, backup, restore, and upgrade.
4. Agent adapter setup and least-privilege credentials.
5. Supported API/MCP connection from ChatGPT.
6. GitHub sync configuration, identity, and local record mapping.
7. Skills and policy installation, versioning, and update process.
8. Human authorization and sensitive-action approval setup.
9. Health checks, logs, recovery, and offline behavior.
10. Uninstall and data-retention procedures.

## Separation from implementation

This repository contains human-readable setup instructions and operational policy. The separate setup/implementation repository should hold executable code such as installers, integration services, adapters, and configuration tooling. Its repository name and boundary will be chosen when implementation begins.

## Validation record

Record tested Paperclip version, platform, adapter versions, connection path, limitations, and evidence links here after #9 is complete. Do not claim a capability based only on the conceptual architecture.
