# G2D Researcher Cluster

**Historical artifact documenting the original G2D autonomous researcher cluster and its evolution toward modern AI infrastructure.**

This repository preserves the G2 Researcher v1.0 lineage: four snapshots of an open-source autonomous researcher that Gen 2 Dynamics forked and organized by role in November 2025. It is not current Gen 2 Dynamics software. It is an engineering artifact: a readable snapshot of an early multi-agent research pattern.

The researcher engine itself (orchestrator, agents, API server and frontend) is [AI Researcher](https://github.com/mshumer/ai-researcher) by mshumer, used under the MIT License. See [Origin and attribution](#origin-and-attribution).

The G2D cluster organized that engine around a simple idea:

> Research workflows should be reproducible, inspectable, and separable by role.

The early cluster used a baseline engine, an active development branch, and specialized agent variants to explore how autonomous research systems could be organized, tested, and evolved without contaminating the original working snapshot.

---

## Repository status

**Status:** Public artifact / architecture snapshot  
**Current use:** Documentation and educational reference  
**Production status:** Not production infrastructure  
**Origin:** G2 Researcher v1.0 lineage, forked from [mshumer/ai-researcher](https://github.com/mshumer/ai-researcher) (MIT)  
**Maintainer:** JordanG2D / Gen 2 Dynamics

This repo is intended to show lineage, design intent, and lessons learned. Current Gen 2 Dynamics work is not published here.

The imported application code is preserved for historical review. It should not be treated as a maintained runnable product or used with live credentials without review.

---

## What this repository contains

```text
g2d-researcher-cluster/
  README.md
  LICENSE
  docs/
    architecture.md
    lineage.md
    philosophy.md
    lessons-learned.md
  frozen-baseline/
    README.md
    NOTES.md
    SOURCE_README.md
    ...
  dev-branch/
    README.md
    NOTES.md
    SOURCE_README.md
    ...
  agent-b-quant-explorer/
    README.md
    NOTES.md
    SOURCE_README.md
    ...
  agent-c-synthesis-engine/
    README.md
    NOTES.md
    SOURCE_README.md
    ...
  examples/
    sample-run.md
    sample-report.md
```

The component folders now include sanitized public archival source material from the original split repositories. Each folder keeps this repository's narrative `README.md`, the original source repository README as `SOURCE_README.md`, and a short `NOTES.md` describing archival context and exclusions.

---

## Origin and attribution

The application source in `frozen-baseline/`, `dev-branch/`, `agent-b-quant-explorer/` and `agent-c-synthesis-engine/` comes from [AI Researcher](https://github.com/mshumer/ai-researcher) by mshumer. It is used under the MIT License, and each component folder keeps the original `LICENSE` with its copyright notice.

Gen 2 Dynamics' contribution is:

- the cluster structure: a frozen baseline, a development branch and two role-labelled variants;
- one small patch to the engine in November 2025 (`agent.py`, `logger.py`, `main.py`: report return value, a model option, status logging);
- this consolidation, the narrative READMEs, `NOTES.md` files and everything under `docs/` and `examples/`.

The four component folders contain the same application code. The Agent B and Agent C specializations are described in their READMEs; they were not implemented as code differences.

**Known issue.** The November 2025 patch left the engine working only in `--test-mode`. `_run_gemini_experiment_loop` was indented inside the Claude function, and the CLI's Claude model names (`claude-opus-4.5`, `claude-3.5-sonnet`) do not match the names the code routes on (`claude-opus-4-5`, `claude-3-5-sonnet`). The code is preserved as it was and is not maintained; use the upstream project for a working researcher.

---

## Lineage overview

The original public researcher lineage was split into four repositories:

1. **FROZEN** — immutable baseline archive
2. **DEV** — active development branch
3. **AGENT_B** — quantitative exploration variant
4. **AGENT_C** — synthesis and meta-analysis variant

This repository consolidates that lineage into one coherent public artifact.

```text
FROZEN baseline
      ↓
DEV branch
      ↓
Specialized variants
      ├── AGENT_B: quant explorer
      └── AGENT_C: synthesis engine
      ↓
Lessons learned
```

---

## Why this matters

Most agent projects are presented as finished products. This repository is different.

It documents an early operating pattern:

- preserve a known-good baseline
- develop from a controlled branch
- fork specialized agents by role
- compare behaviors across variants
- keep research artifacts separate from production systems
- treat agent evolution as something that should leave evidence

---

## Design principles

The original researcher cluster was guided by a few principles that remain central to G2D:

- **Preserve baselines.** Do not destroy the last known-good system while experimenting.
- **Separate roles.** A quant explorer and a synthesis engine should not be the same agent by accident.
- **Keep lineage visible.** Architecture decisions should be explainable after the fact.
- **Prefer evidence over vibes.** Useful autonomous systems should produce artifacts, not just outputs.
- **Design for evolution.** Early systems should teach the next system what to become.

---

## Relationship to current G2D work

This repository is part of the public artifact trail for Gen 2 Dynamics.

Gen 2 Dynamics now builds Nexus, a control layer for AI agents that do accountable work. This repository is an early research prototype and is not part of Nexus.

---

## Suggested reading order

1. [`docs/philosophy.md`](docs/philosophy.md)
2. [`docs/lineage.md`](docs/lineage.md)
3. [`docs/architecture.md`](docs/architecture.md)
4. [`docs/lessons-learned.md`](docs/lessons-learned.md)
5. [`docs/import-notes.md`](docs/import-notes.md)
6. [`docs/validation.md`](docs/validation.md)
7. [`examples/sample-run.md`](examples/sample-run.md)
8. [`examples/sample-report.md`](examples/sample-report.md)

---

## License

MIT License. The application source is Copyright (c) 2025 mshumer; the consolidation and documentation are Copyright (c) 2026 JordanG2D. See [`LICENSE`](LICENSE) and each component folder's `LICENSE`.

This repository is shared as a public artifact and educational reference. It is not a release of current private G2D production systems.
