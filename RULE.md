---
description: "Forbid dead, unused, or unreachable code"
alwaysApply: true
---

# NoDeadCode Rule

A codebase under NoDeadCode must contain no dead, unused, or unreachable code.

## Requirements

- Code must be part of a live, reachable behavior surface and executed by automated tests. If a function or branch is not covered, it is dead: add test coverage or delete it.
- Commented‑out code for history or “just in case” is forbidden. Version control is the archive.
- Unused parameters, flags, feature toggles, legacy shims, and permanently‑off branches are forbidden unless they are actively used and publicly exercised.

## Enforcement

- CI must run automated tests with coverage and fail when uncovered code exists. Use any coverage tooling appropriate to the language.
