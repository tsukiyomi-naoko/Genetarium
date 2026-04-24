---
name: r3f-viewport-builder
description: Use this when implementing or reviewing the real-time 3D viewport, camera interactions, scene readability, and renderer-side structure for Aquarium Environment Builder.
---

Goal:
Build and protect a strong real-time 3D configurator viewport for browser use.

When invoked:
1. Focus on a live, readable 3D scene.
2. Ensure camera interaction is good enough for real editing.
3. Keep rendering code modular and state-driven.
4. Preserve future compatibility with object selection and manipulation.

Rules:
- The viewport must be real, not decorative.
- Prioritize:
  - orbit
  - pan
  - zoom
  - readable framing
  - sensible lighting
  - real-time update response
- Avoid camera jank.
- Avoid broken clipping behavior in normal use.
- Avoid pushing scene truth into renderer-only state.
- Keep components modular and easy to extend for picking/selection later.

Do not:
- build fake preview panels
- hardcode UI-owned geometry logic in a brittle way
- overcomplicate rendering before the active phase requires it
