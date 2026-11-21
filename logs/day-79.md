# Day 79: Nov 21, 2026 — Cargo Manifest Validator Debugging & Immutability

## Executive Summary
Investigated the **Build a Cargo Manifest Validator** lab within the **Objects** module, working through immutable object copying and multi-field validation rules before pausing to step away for a break.

## Technical Milestones & Module Breakdown
1. **Build a Cargo Manifest Validator (Lab in Progress)**
   - Implemented `normalizeUnits(manifest)` to return a non-mutating normalized object copy, converting `"lb"` weights (`* 0.45`) to `"kg"` while preserving `"kg"` inputs[cite: 17].
   - Built initial missing-property (`undefined` -> `"Missing"`) guards in `validateManifest(manifest)` and scoped positive-integer checks (`Number.isInteger()`) for `containerId` alongside string/numeric validation cases (`destination`, `weight`, `unit`, `hazmat`)[cite: 17].

## Key Technical Takeaways
- **Non-Mutating Validation Contracts**: Returning fresh error/normalized objects without mutating the input `manifest` preserves caller state across validation pipelines[cite: 17].

---
*Target for subsequent session: Resume Build a Cargo Manifest Validator Lab[cite: 17]*
