# Lessons Learned

The original G2D Researcher Cluster produced more value as a learning system than as a final architecture.

This document captures the practical lessons that came out of the first researcher lineage.

---

## 1. A working agent is not the same as a reliable system

The early researcher engine could produce useful outputs, but usefulness alone was not enough.

A reliable research system needs:

- clear inputs
- durable outputs
- traceable intermediate steps
- repeatable run behavior
- named roles
- observable failure points

This lesson later influenced G2D's focus on validation workflows and reportable system behavior.

---

## 2. Baselines matter

The FROZEN baseline was important because agent systems change quickly.

Without a preserved reference point, every improvement becomes ambiguous.

Did the system get better?

Did the model change?

Did the prompt change?

Did the workflow drift?

Did a tool update alter behavior?

A frozen baseline does not solve every evaluation problem, but it prevents the entire system from becoming unknowable.

---

## 3. Specialized agents need stronger orchestration

AGENT_B and AGENT_C proved that specialization is useful, but it also creates a coordination burden.

A quant explorer can generate hypotheses.

A synthesis engine can merge findings.

But the system still needs a way to decide:

- what each agent should receive
- what each agent should output
- how outputs are compared
- how disagreements are recorded
- when a run is considered complete

This lesson pointed toward the need for a stronger control plane.

---

## 4. Reports are not decoration

Early agent systems often treat reports as a final formatting step.

G2D learned the opposite.

Reports are part of the system architecture.

A report defines what the workflow believed mattered enough to preserve. It creates a durable interface between the run and the human operator.

This eventually led to stronger report-shaped agent thinking and the Donna direction.

---

## 5. Synthesis must remain connected to evidence

AGENT_C highlighted a common problem with synthesis agents.

They can create coherent narratives even when the underlying evidence is thin, conflicting, or incomplete.

That is dangerous.

A useful synthesis system should preserve links back to:

- raw outputs
- source observations
- prior summaries
- run metadata
- unresolved disagreements

This lesson directly supports the modern G2D emphasis on audit records and validation bundles.

---

## 6. The research cluster needed a better memory model

The original cluster made it clear that memory cannot be treated as a casual add-on.

Useful autonomous research requires memory that can distinguish between:

- raw transcript
- generated summary
- hypothesis
- conclusion
- operator note
- system decision
- stable fact
- temporary assumption

This lesson became part of the bridge toward deeper research infrastructure and more structured knowledge workflows.

---

## 7. The lab needed fewer clever agents and more operating structure

The early instinct was to create more agents.

The better lesson was to create clearer operating structure.

More agents do not automatically produce better research.

Better workflow boundaries, records, evaluation, routing, and reporting often matter more.

This became one of the central lessons behind the shift from a loose researcher cluster toward a more disciplined lab architecture.

---

## 8. Public artifacts matter

The original researcher repos were useful, but scattered.

They showed pieces of the work without explaining the system as a whole.

This repository exists because public technical work should be legible.

If a reviewer, collaborator, pilot, or researcher visits the GitHub profile, they should be able to understand:

- what the system was
- why it existed
- what it taught
- how it connects to the current direction

That is the purpose of this consolidation.

---

## Summary

The first G2D Researcher Cluster taught that autonomous research infrastructure is not just about model calls or agent prompts.

It is about architecture, lineage, evidence, workflow design, and the discipline to make the system understandable after it runs.