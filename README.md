# G2D Researcher Cluster

**Historical artifact documenting the original G2D autonomous researcher cluster and its evolution toward modern AI infrastructure.**

This repository preserves the first public generation of the Gen 2 Dynamics autonomous researcher architecture. It is not the current private production lab. It is an engineering artifact: a readable, reusable snapshot of the early multi-agent research pattern that helped shape later G2D systems such as Orion, the Black Box Lab, and the broader control-plane architecture.

The original researcher system was built around a simple idea:

> Research workflows should be reproducible, inspectable, and separable by role.

The early cluster used a baseline engine, an active development branch, and specialized agent variants to explore how autonomous research systems could be organized, tested, and evolved without contaminating the original working snapshot.

---

## Repository status

**Status:** Public artifact / architecture snapshot  
**Current use:** Documentation and educational reference  
**Production status:** Not production infrastructure  
**Origin:** G2 Researcher v1.0 lineage  
**Maintainer:** JordanG2D / Gen 2 Dynamics

This repo is intended to show lineage, design intent, and lessons learned. The current active systems are maintained elsewhere in private lab infrastructure.

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
    evolution-to-orion.md
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
      ↓
Evolution toward Orion and modern G2D lab infrastructure
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

That pattern later influenced G2D's current emphasis on validation workflows, control-plane infrastructure, audit trails, reporting lanes, and reproducible system behavior.

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

The current G2D direction is broader than the original researcher cluster. Today the work centers on AI-native control-plane infrastructure, validation workflows, autonomous systems research, deterministic execution, auditability, and pilot-grade lab operations.

This repository shows one early origin point of that direction.

---

## Suggested reading order

1. [`docs/philosophy.md`](docs/philosophy.md)
2. [`docs/lineage.md`](docs/lineage.md)
3. [`docs/architecture.md`](docs/architecture.md)
4. [`docs/lessons-learned.md`](docs/lessons-learned.md)
5. [`docs/evolution-to-orion.md`](docs/evolution-to-orion.md)
6. [`docs/import-notes.md`](docs/import-notes.md)
7. [`docs/validation.md`](docs/validation.md)
8. [`examples/sample-run.md`](examples/sample-run.md)
9. [`examples/sample-report.md`](examples/sample-report.md)

---

## License

MIT License.

This repository is shared as a public artifact and educational reference. It is not a release of current private G2D production systems.
