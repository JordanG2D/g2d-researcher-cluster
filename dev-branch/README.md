# Development Branch

**Role:** Active experimentation lane  
**Original source:** `G2-Researcher_v1.0_DEV`  
**Status:** Historical component placeholder

The development branch represented the working lane for improving the original researcher engine after the frozen baseline was preserved.

---

## Purpose

The DEV branch existed to test and validate changes before creating specialized variants.

It was the place for:

- model backend experiments
- reasoning loop changes
- tool orchestration updates
- memory and logging experiments
- dry-run validation
- feature expansion

---

## Why this folder exists

This folder is reserved for importing or adapting the original DEV artifact.

The first narrative pass intentionally creates structure before code import. A later development pass should review the source material and decide what belongs in the public consolidated artifact.

---

## Dev handoff notes

When importing source material:

1. Compare against `frozen-baseline/`.
2. Preserve changes that show meaningful evolution.
3. Remove local machine assumptions, secrets, and obsolete configuration.
4. Add notes explaining major changes from the baseline.
5. Avoid turning this folder into the modern private stack.

---

## Historical interpretation

This component represents the first controlled experimentation lane.

The lesson was simple:

> Active development needs a boundary, otherwise every experiment becomes the new baseline by accident.