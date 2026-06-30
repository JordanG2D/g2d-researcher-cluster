# Import Notes

This note records the archival import choices for the consolidated G2 Researcher v1.0 lineage.

## Source repositories inspected

- `JordanG2D/G2-Researcher_v1.0_FROZEN`
- `JordanG2D/G2-Researcher_v1.0_DEV`
- `JordanG2D/G2-Researcher_v1.0_AGENT_B`
- `JordanG2D/G2-Researcher_v1.0_AGENT_C`

## Import mapping

- `G2-Researcher_v1.0_FROZEN` -> `frozen-baseline/`
- `G2-Researcher_v1.0_DEV` -> `dev-branch/`
- `G2-Researcher_v1.0_AGENT_B` -> `agent-b-quant-explorer/`
- `G2-Researcher_v1.0_AGENT_C` -> `agent-c-synthesis-engine/`

## What was preserved

Each component folder keeps the original application source structure where useful, including the Python researcher engine files, historical guide documents, frontend source, package metadata, Dockerfile, and original repository README as `SOURCE_README.md`.

The existing consolidated repository README and docs remain the authoritative narrative entry point.

## What was excluded

The import intentionally excludes generated caches, private run logs, TypeScript build cache files, `.env` files, placeholder environment files, and live deployment configuration that did not add useful archival context.

The archive preserves historical environment-variable references in code because they explain how the early system expected model and sandbox dependencies to be supplied. No credential file, API key, token, or secret value is included.

## Scope boundary

This is historical archival material from the original public G2 Researcher v1.0 lineage. It is not Orion, not the current G2D private lab, not current Black Box Lab production infrastructure, and not a release of any current private system.
