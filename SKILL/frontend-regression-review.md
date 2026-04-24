---
name: frontend-regression-review
description: Use this when reviewing the app for UI/viewport integration issues, state-flow regressions, interaction problems, and obvious frontend maintainability risks.
---

Goal:
Catch practical frontend regressions without derailing the active phase.

When invoked:
1. Review control-to-state-to-scene flow.
2. Review viewport interaction quality.
3. Review component boundaries and obvious render inefficiencies.
4. Rank issues by severity.
5. Recommend minimal, high-confidence fixes.

Focus on:
- brittle architecture
- unnecessary re-renders
- dead or misleading controls
- weak typing
- viewport/camera usability issues
- UX friction in the live edit loop

Rules:
- Optimize for reliability, not perfection.
- Avoid demanding giant refactors unless absolutely necessary.
- Preserve the chosen architecture where possible.
- Keep findings practical and directly actionable.
