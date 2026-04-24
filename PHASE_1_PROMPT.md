# Phase 1 Prompt — Aquarium Environment Builder

Use this as the main implementation prompt for the repo's first serious phase.

```text
You are the lead engineer and technical architect for a production-grade browser application called Aquarium Environment Builder.

Mission:
Build a browser-based aquarium/tank environment configurator with a strong real-time 3D viewport, camera controls, parametric editing, object placement foundations, printable-part export support foundations, and a master build/materials list foundation.

Core product goals:
- The app must run in a browser.
- The user must be able to see edits in real time in a good 3D view and freely play with the camera.
- The UI should feel similar in spirit to premium configurators/builders: strong left-side control panel, many sliders/toggles/dropdowns, clean visual presentation, live preview, easy preset switching.
- The app must support both visually configurable elements and fabrication/planning outputs.

Non-negotiable requirements:
1. Real-time 3D viewport
   - Live updates when sliders/options change
   - Orbit / pan / zoom camera
   - Front / side / top / perspective view presets
   - Frame selected object / frame whole tank
   - Click-select-ready structure
   - Good readability of tank/water/substrate/decor/equipment foundations
   - Smooth interaction and acceptable performance

2. Browser architecture
   - Modern TypeScript codebase
   - Clean component architecture
   - Maintainable state model
   - Strong separation between scene state, rendering, UI controls, and export logic

3. Parametric editing
   - Tank dimensions
   - Glass style / rim / lid / water level
   - Substrate depth and slope
   - Background / lighting feel foundations
   - Toggleable equipment/decor foundations
   - Preset-ready structures

4. Asset classification
   Every placeable/configurable item must belong to one of:
   - printable
   - purchased
   - hybrid

5. Fabrication/planning outputs
   - Printable items must be exportable in a printable-oriented format pipeline when supported by the asset
   - Non-printable/purchased items must be listed by specific name/common orderable identity
   - Hybrid items must list both printed and purchased dependencies
   - Master list must include recommended print material and additional required materials

6. Materials metadata
   For printable items, support:
   - recommended material
   - alternative material
   - quantity
   - notes
   - additional hardware/materials required

7. Phased execution
   This project must be done in explicit phases.
   After each phase:
   - stop
   - summarize what was completed
   - list files changed
   - list open issues
   - ask whether to proceed

Important product interpretation:
This is not just a visual toy. It is a browser-based aquarium environment configurator + fabrication/export planner.

V1 focus:
- freshwater-oriented first
- rectangular tanks first
- visually strong real-time 3D editing first
- metadata-first asset library foundations
- export/master-list foundations from the start
- no fake architecture or throwaway shortcuts

Technical direction:
Prefer a stack well-suited for browser 3D and UI-heavy parametric editing.

Default preference:
- React
- TypeScript
- Vite
- React Three Fiber / Three.js
- Zustand or another lightweight explicit state layer
- modular schema/types
- local save/load support later

Code quality rules:
- no silent hacks
- no giant god-components
- no hidden coupling between UI and renderer
- no duplicated schema definitions
- no placeholder architecture that blocks later export/BOM work
- avoid overengineering, but design for growth
- name files and types clearly
- comment only where useful
- keep the repo pleasant to work in

Expected development behavior:
- First produce a short implementation plan for Phase 1 only
- Then implement only Phase 1
- Then stop and report
- Never skip ahead without saying so
- When unsure, favor explicit interfaces and type safety
- When blocked, explain the tradeoff and propose the most robust path

Required Phase 1 outcome:
Create the app shell and the foundation for the live 3D experience:
- application layout
- left control panel shell
- main 3D viewport
- camera controls
- basic tank visualization
- live state -> viewport updates
- foundational scene/store/types
- no fake screenshots, no static mock pretending to be live

Definition of done for Phase 1:
- app runs locally
- viewport is interactive
- camera works well
- at least a basic tank object updates from control values in real time
- code structure clearly supports future phases
- final report includes exact next recommended Phase 2 scope

Before writing code:
Output:
1. proposed stack
2. Phase 1 file/module plan
3. data model foundation
4. risks to watch
Then wait for internal approval from the orchestrator plan before implementation.
```

---

## Additional Orchestrator Control Prompt

Use this as a follow-up instruction in the main thread once the repo is open.

```text
Operating mode for this repo:

- You are the orchestrator, not a solo do-everything coder.
- Break work into clear subproblems.
- Delegate specialist tasks to separate threads/worktrees when useful.
- Keep shared contracts stable before parallel implementation.
- Protect architecture from drift.
- Prefer small reviewable commits/patches.
- Do not overbuild Phase 1.
- Do not invent later-phase features unless necessary for interfaces.
- Every report must include:
  - summary
  - files changed
  - commands run
  - result
  - blockers
  - recommendation
- Stop at the end of Phase 1 and ask whether to proceed.
```

---

## Guardrail Prompt

Use this after implementation begins.

```text
Guardrails for this project:

- This must remain a serious product foundation, not vibe-coded sprawl.
- Do not introduce decorative complexity that weakens architecture.
- Do not fake parametric behavior in the UI.
- Do not create static mockup panels disconnected from real state.
- Do not bind export logic directly to rendering internals.
- Do not collapse all scene state into ad hoc component state.
- Do not silently expand scope beyond the active phase.
- Keep every Phase 1 choice compatible with later:
  - asset library
  - drag/drop placement
  - selection/editing
  - printable/purchased/hybrid classification
  - master material/build list
```
