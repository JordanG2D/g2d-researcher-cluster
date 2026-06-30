# Architecture

The original G2D Researcher Cluster used a simple but important architecture pattern:

> preserve a baseline, develop from a controlled branch, and create specialized agent variants for different research roles.

This was not a cloud-scale architecture. It was an early lab architecture for learning how autonomous research workflows should be separated, evaluated, and evolved.

---

## Conceptual model

```text
                 ┌─────────────────────┐
                 │  FROZEN baseline     │
                 │  known-good engine   │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │  DEV branch          │
                 │  active experiments  │
                 └──────────┬──────────┘
                            │
              ┌─────────────┴─────────────┐
              ▼                           ▼
┌─────────────────────────┐   ┌─────────────────────────┐
│ AGENT_B                 │   │ AGENT_C                 │
│ Quant Explorer           │   │ Synthesis Engine        │
└─────────────────────────┘   └─────────────────────────┘
```

---

## Core components

### 1. Baseline engine

The baseline engine represented a stable researcher loop.

Its role was not to be the most advanced system. Its role was to be a reference implementation that could be trusted after experiments started to diverge.

Responsibilities:

- preserve the first known-good researcher behavior
- remain unchanged during active experimentation
- provide a comparison point for future variants
- prevent uncontrolled drift

Mapped folder:

```text
frozen-baseline/
```

---

### 2. Development branch

The development branch was the active improvement lane.

Responsibilities:

- test model backends
- improve reasoning loops
- add or adjust tools
- experiment with memory and logging
- validate behavior before creating variants

Mapped folder:

```text
dev-branch/
```

---

### 3. Agent variants

The agent variants explored role specialization.

The key architectural question was:

> Should one general researcher do everything, or should separate agents specialize by workflow role?

The early answer was that role separation makes the system easier to reason about.

Mapped folders:

```text
agent-b-quant-explorer/
agent-c-synthesis-engine/
```

---

## AGENT_B: Quant Explorer

AGENT_B represented fast quantitative exploration.

Intended strengths:

- numerical reasoning
- pattern detection
- repeated hypothesis testing
- line movement tracking
- experiment batching
- early expected-value modeling

Expected failure modes:

- over-indexing on local patterns
- generating too many weak hypotheses
- requiring downstream synthesis
- needing strong recordkeeping to remain useful

AGENT_B pointed toward a recurring G2D lesson:

> Exploration creates value only if the results can be traced and interpreted later.

---

## AGENT_C: Synthesis Engine

AGENT_C represented cross-run synthesis and meta-analysis.

Intended strengths:

- reading outputs from other agents
- merging findings into reports
- identifying higher-order patterns
- comparing model behavior
- creating coherent summaries across runs

Expected failure modes:

- smoothing over important disagreements
- hallucinating coherence where none exists
- losing source-level traceability
- requiring stronger links back to raw artifacts

AGENT_C pointed toward another recurring G2D lesson:

> Synthesis is only useful when it remains connected to evidence.

---

## Operating flow

A typical intended flow looked like this:

```text
1. Begin from known-good baseline.
2. Modify or improve the DEV branch.
3. Validate the changed behavior with dry runs.
4. Fork or adapt a specialized variant.
5. Run the specialized agent against a target research task.
6. Preserve outputs as artifacts.
7. Compare findings across variants.
8. Feed lessons into the next architecture cycle.
```

---

## What this architecture taught

The original cluster made several lessons obvious:

- agent roles need names and boundaries
- output artifacts matter as much as agent responses
- a system without lineage becomes hard to trust
- development and reference state should be separated
- synthesis needs source evidence
- orchestration becomes more important as agents multiply

These lessons later pushed G2D toward stronger control-plane thinking, workflow ledgers, report lanes, validation bundles, and the deeper Orion research direction.

---

## Current status

This repository currently documents the architecture and provides a skeleton for future code import.

It is intentionally not claiming to be the active G2D lab or the current Orion implementation.