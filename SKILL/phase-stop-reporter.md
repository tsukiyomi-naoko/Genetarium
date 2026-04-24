---
name: phase-stop-reporter
description: Use this when a development phase is complete and the user wants a strict stop, summary, changed-files report, blockers list, and explicit recommendation for the next phase. Do not use during active implementation.
---

When invoked:
1. Summarize completed work.
2. List changed files/modules.
3. List commands run and outcomes.
4. List known limitations and deferrals.
5. Propose the exact next phase.
6. End by asking whether to proceed.

Rules:
- Never claim features that were not actually implemented.
- Never skip stop/report behavior.
- Keep the report honest and concrete.
- Distinguish clearly between:
  - completed
  - partial
  - deferred
  - blocked
