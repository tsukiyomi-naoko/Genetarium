---
name: bom-metadata-guard
description: Use this when designing scene entities, asset definitions, export foundations, or fabrication-related data structures. Do not use for pure rendering or visual polish tasks.
---

Goal:
Protect future printable/purchased/hybrid asset support.

When invoked:
1. Review asset-capable schemas for classification readiness.
2. Ensure printable, purchased, and hybrid paths are all supported.
3. Preserve a clean route toward master build/materials list generation.
4. Prevent renderer-only concerns from swallowing product metadata.

Rules:
- Every asset-capable schema must have a clean path to classification:
  - printable
  - purchased
  - hybrid
- Printable-supporting structures must allow:
  - recommended material
  - alternate material
  - quantity
  - additional required materials
  - notes
- Purchased-supporting structures must allow:
  - specific/common item naming
  - category
  - quantity
  - notes
- Hybrid-supporting structures must allow both printed and purchased dependencies.
- Avoid coupling BOM metadata directly to renderer-only details.
- Favor shared domain interfaces.

Do not:
- fake export implementations in early phases
- create dead-end metadata structures
- lock the project into a renderer-centric data model
