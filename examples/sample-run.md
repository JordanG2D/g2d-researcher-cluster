# Sample Run

This file describes a representative run pattern for the original G2D Researcher Cluster.

It is illustrative. It is not a live execution log.

---

## Example task

```text
Research prompt:
Evaluate whether a candidate market pattern appears meaningful enough to justify deeper testing.
```

---

## Intended workflow

```text
1. Operator defines research question.
2. DEV or specialized variant receives the task.
3. Agent B explores quantitative angles.
4. Agent C synthesizes findings across outputs.
5. Operator reviews artifacts.
6. Useful findings are preserved.
7. Weak or unsupported hypotheses are discarded.
```

---

## Example run record

```yaml
run_id: g2r-demo-001
system: G2 Researcher v1.0
mode: historical-example
operator: human
primary_agent: agent-b-quant-explorer
secondary_agent: agent-c-synthesis-engine
status: completed
```

---

## Example inputs

```yaml
research_question: "Does this observed pattern justify deeper testing?"
constraints:
  - do not treat early observations as conclusions
  - preserve assumptions
  - identify weak evidence
  - produce a synthesis-ready output
```

---

## Example Agent B output

```text
Agent B identifies several candidate observations:

1. Pattern appears in multiple adjacent windows.
2. Signal quality weakens when the window is expanded.
3. The observation may be regime-dependent.
4. More testing is required before assigning confidence.
```

---

## Example Agent C synthesis

```text
Agent C reviews the exploratory notes and produces a synthesis:

The pattern is worth preserving as a candidate hypothesis, but not strong enough to treat as a decision rule. The useful next step is to define a cleaner test window, preserve the original assumptions, and compare future runs against the same criteria.
```

---

## Example preserved artifact

```yaml
artifact_type: candidate_hypothesis
confidence: low_to_medium
next_action: deeper_validation
notes:
  - preserve original observation
  - avoid premature conclusion
  - compare against wider sample
```

---

## Why this matters

The important part of the run is not that the agent produced an answer.

The important part is that the workflow preserved:

- the question
- the assumptions
- the role split
- the exploratory output
- the synthesis output
- the next action

That is the bridge from simple agent use toward auditable research infrastructure.