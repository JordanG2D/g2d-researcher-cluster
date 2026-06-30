# Lineage

This document describes the original G2D Researcher v1.0 lineage and how the separate public repositories map into this consolidated artifact.

The original system was not organized as one polished monorepo. It evolved through snapshots and specialized forks. That was messy, but it was also honest: the architecture emerged through direct experimentation.

---

## Original lineage

```text
G2-Researcher_v1.0_FROZEN
        ↓
G2-Researcher_v1.0_DEV
        ↓
        ├── G2-Researcher_v1.0_AGENT_B
        └── G2-Researcher_v1.0_AGENT_C
```

---

## FROZEN baseline

The FROZEN baseline represented the first stable reference point.

Its purpose was to preserve a known-good researcher engine that could be used as the canonical reference for future development.

It existed to answer:

> What was the last clean version that worked?

The baseline was intentionally not modified. It served as a stable comparison point for future variants.

Mapped folder:

```text
frozen-baseline/
```

---

## DEV branch

The DEV branch represented active development.

It was the environment for upgrades, refactors, backend changes, orchestration improvements, memory experiments, and dry-run validation.

It existed to answer:

> Where do we safely improve the system before creating specialized variants?

Mapped folder:

```text
dev-branch/
```

---

## AGENT_B: quantitative explorer

AGENT_B was the first specialized variant.

Its direction was quantitative exploration: statistical reasoning, pattern recognition, line movement tracking, high-frequency hypothesis cycling, and early expected-value modeling foundations.

It existed to answer:

> What happens when a researcher agent is optimized for fast quantitative exploration?

Mapped folder:

```text
agent-b-quant-explorer/
```

---

## AGENT_C: synthesis engine

AGENT_C was the second specialized variant.

Its direction was synthesis: model comparison, long-form experiment analysis, hypothesis synthesis across runs, and multi-agent evaluation logic.

It existed to answer:

> What happens when a researcher agent is optimized to read, merge, and interpret the outputs of other agents?

Mapped folder:

```text
agent-c-synthesis-engine/
```

---

## Why consolidate the lineage now?

The original split-repo structure made sense while experimenting. It made each fork explicit and reduced the risk of contaminating the baseline.

But as a public artifact, the split structure creates friction.

A reviewer, collaborator, or prospective partner should not have to reconstruct the system from scattered repositories.

This consolidated repo makes the lineage readable:

- one entry point
- one architecture narrative
- one folder per historical role
- one lessons-learned path
- one bridge to current G2D systems

---

## What this repo is not

This repo is not the current G2D private lab.

It is not a full production release.

It is not intended to expose proprietary current infrastructure.

It is a preserved public artifact showing how the first researcher cluster was organized and what it taught the lab.

---

## What this repo is

This repo is a public evidence trail.

It shows that the current G2D emphasis on validation, auditability, deterministic execution, report lanes, and control-plane infrastructure did not appear out of nowhere.

Those ideas grew out of early experiments with autonomous researcher systems.