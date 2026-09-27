---
type: state
---

# Current state

The module list below is the initial scaffold snapshot. For current project membership and metadata update rules, follow `../references/project.md`.

## Generated baseline

- `HeimForgeExample.ServerCore`: server-only gameplay and administration features.
- `HeimForgeExample.Shared.Diagnostics`: independent two-sided module with its own compatibility requirements.
- `HeimForgeExample.Client`: client-only UI, visual, input, and convenience features.
- `HeimForgeExample.Common`: shared pure code and protocol primitives.

## Working

- HeimForgeExample generated from HeimForge.
- Generated MSBuild and C# package metadata is synchronized and validated.
- Cross-platform `net48` reference assemblies are explicitly declared.
- Metadata-driven deployment prevents client/server DLL cross-contamination.
- Deterministic local package generation and SHA-256 checksums are implemented.
- Portable scaffold tests cover repository invariants.
- Portable agent instructions and project skills are available through `AGENTS.md` and `.agents/skills/`.

## In progress

- Local WSL/Valheim environment verification.
- First successful full plugin build against installed Valheim/Jotunn.

## Next

1. Configure `Environment.props` and `.valheim/dev.json`.
2. Run `./scripts/preflight.sh`.
3. Run `./scripts/bootstrap.sh`.
4. If publicized Valheim references are absent, run `python3 scripts/update-game-stack.py refresh` after verifying `VALHEIM_INSTALL`; this refreshes references, builds, and runs preflight.
5. Otherwise run `./scripts/build.sh Debug` for an ordinary parallel build.
6. Design and implement the first real feature using `docs/features/TEMPLATE.md`.

## Initial milestones

0. Repository and portable agent-tooling scaffold.
1. Runtime plugin shells and side boundaries.
2. Shared Diagnostics CustomRPC proof.
3. First real feature (see `docs/features/TEMPLATE.md`).
4. Packaging/profile generation.

## Unverified or pending

- Installed Valheim version is not yet recorded.
- Runtime gameplay behavior and multiplayer compatibility still require verification on the user's installation.
- Public Thunderstore manifests and assets are not generated yet. Local deterministic ZIP packaging is implemented.

## Last verified

- Valheim: UNVERIFIED LOCALLY
- Repository scaffold tests: PASS at generation time
- Server build: NOT RUN IN USER ENVIRONMENT
- Client build: NOT RUN IN USER ENVIRONMENT
