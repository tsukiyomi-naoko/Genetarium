---
name: parametric-schema-guard
description: Use this when designing or reviewing tank, substrate, water, preset, or asset-capable schemas so the data model stays clean, typed, and extendable.
---

Goal:
Protect the scene/domain schema from ad hoc growth and future rewrite pressure.

When invoked:
1. Review whether the current schema clearly represents product truth.
2. Keep types serialization-friendly where practical.
3. Make sure renderer-specific details do not pollute shared domain models without reason.
4. Preserve room for future asset classification and master-list metadata.

Rules:
- Favor explicit domain shapes.
- Avoid hidden data inside arbitrary component state.
- Avoid duplicated type definitions.
- Keep update actions/selectors understandable.
- Design current schema so it can later support:
  - presets
  - scene assets
  - printable/purchased/hybrid classification
  - recommended materials
  - quantity and dependency listing

Do not:
- build full later-phase systems too early
- let temporary convenience become long-term schema debt
