---
name: aquarium-architect
description: Use this when defining project structure, shared types, scene architecture, and growth paths for Aquarium Environment Builder. Do not use for pure visual polish or isolated rendering tweaks.
---

Goal:
Protect the long-term architecture of Aquarium Environment Builder while keeping implementation practical.

When invoked:
1. Define the smallest durable architecture for the active phase.
2. Separate domain data, renderer logic, UI logic, and export/list foundations.
3. Identify shared contracts needed by parallel workers.
4. Call out anti-patterns and rewrite traps early.
5. Keep the active phase scoped tightly.

Rules:
- Prefer explicit shared interfaces.
- Avoid schema duplication.
- Avoid giant god-components.
- Avoid renderer-owned product truth.
- Ensure future compatibility with:
  - asset classification
  - drag/drop placement
  - selection/editing
  - printable/purchased/hybrid metadata
  - master build/materials lists
- Do not overengineer with unnecessary ceremony.

Deliverables should usually include:
- folder/module structure
- ownership boundaries
- shared types/interfaces
- growth risks
- merge recommendations
