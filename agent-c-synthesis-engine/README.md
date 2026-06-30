# Agent C — Synthesis Engine

**Role:** Synthesis and meta-analysis variant  
**Original source:** `G2-Researcher_v1.0_AGENT_C`  
**Status:** Historical component with sanitized source import

Agent C represented the second specialized fork of the original G2 Researcher system.

Its intended direction was synthesis: reading outputs from other agents, merging findings into coherent reports, comparing model behavior, and identifying higher-order patterns across runs.

---

## Purpose

Agent C existed to explore whether a researcher agent could specialize in synthesis rather than raw exploration.

Target capabilities included:

- long-form experiment analysis
- cross-run summarization
- hypothesis synthesis
- model comparison
- multi-agent evaluation logic
- report generation support

---

## Expected strengths

Agent C was designed to turn scattered outputs into coherent findings.

Its value was in connecting observations across runs and helping the operator understand what the system had discovered.

---

## Expected risks

Synthesis agents can create smooth narratives that hide weak evidence.

Known risks:

- hallucinated coherence
- loss of source-level traceability
- over-compression of disagreement
- premature conclusion formation
- weak links back to raw artifacts

---

## Dev handoff notes

The original source README is preserved as `SOURCE_README.md`. Import-specific context and exclusions are documented in `NOTES.md`.

When importing source material:

1. Preserve role-specific synthesis configuration and README material.
2. Remove obsolete or private local configuration.
3. Add example report structures if safe.
4. Preserve notes explaining how Agent C differed from Agent B and DEV.
5. Keep the historical framing explicit.

---

## Historical interpretation

Agent C taught an important lesson:

> Synthesis is only trustworthy when it remains connected to the evidence it summarizes.

That lesson later influenced G2D's report-shaped agent and audit-lane thinking.
