# Frozen Baseline

**Role:** Immutable reference snapshot  
**Original source:** `G2-Researcher_v1.0_FROZEN`  
**Status:** Historical component placeholder

The frozen baseline represents the first known-good G2 Researcher v1.0 engine.

Its purpose was to preserve a stable reference point before active development and specialized variants began.

---

## Purpose

The frozen baseline existed to answer:

> What was the clean working version before experiments started?

It provided:

- a stable comparison point
- a known-good reference state
- a source for later development branches
- protection against uncontrolled experimental drift

---

## Why this folder exists

This folder is reserved for importing or adapting the original frozen baseline artifact.

The first narrative pass intentionally does not import source code automatically. A later development pass should review the original repository, remove anything unnecessary or sensitive, and copy only the safe public artifact material into this folder.

---

## Dev handoff notes

When importing source material:

1. Preserve original file structure where useful.
2. Remove secrets, local paths, credentials, and private assumptions.
3. Add a local `NOTES.md` if the artifact requires explanation.
4. Do not mutate this folder into the active development version.
5. Keep this folder stable after import.

---

## Historical interpretation

This component represents G2D's first discipline around baseline preservation.

That lesson remains important:

> You cannot evaluate system evolution if you destroy the reference state.