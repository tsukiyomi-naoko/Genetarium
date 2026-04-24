# Acceptance Checklist — Phase 1

Use this before declaring Phase 1 complete.

---

## 1. App Boot / Local Run

- [ ] The app starts locally with clear setup steps
- [ ] There are no hand-wavy missing instructions
- [ ] The project structure is coherent enough for future growth

---

## 2. Main Layout

- [ ] The main application layout exists
- [ ] The layout feels like the foundation of a real configurator
- [ ] The control area is usable and not just decorative
- [ ] The viewport has appropriate space and prominence

---

## 3. Control Panel

- [ ] A left-side or equivalent control panel exists
- [ ] It contains real controls, not dead placeholders
- [ ] Multiple controls are connected to shared state
- [ ] The current controls meaningfully affect the scene
- [ ] The panel structure can grow into future categories without immediate redesign

---

## 4. 3D Viewport

- [ ] A real live 3D viewport exists
- [ ] The viewport is not a static image or fake preview
- [ ] The scene is readable
- [ ] The tank is visible
- [ ] The scene responds to state updates in real time

---

## 5. Camera Behavior

- [ ] Orbit works
- [ ] Pan works
- [ ] Zoom works
- [ ] Camera interaction feels stable
- [ ] There is no obvious clipping disaster or jank during normal use
- [ ] The camera is good enough to judge edits immediately

---

## 6. Live Parametric Editing

- [ ] At least several tank-related controls update the 3D scene in real time
- [ ] Basic dimension-related changes are visible
- [ ] Water/substrate/tank visual changes are meaningfully represented where included
- [ ] The edit loop feels immediate enough to validate the core concept

---

## 7. State / Data Foundations

- [ ] Shared types exist
- [ ] Scene state is not trapped inside rendering-only components
- [ ] UI and renderer consume shared state/contracts
- [ ] The structure supports future growth without obvious rewrite pressure

---

## 8. Asset / Metadata Foundations

- [ ] There is a clear path for future asset classification
- [ ] Printable / purchased / hybrid foundations are accounted for in the architecture
- [ ] There is an obvious path to recommended materials and master-list generation later
- [ ] Export/BOM planning is not hard-coupled to rendering internals

---

## 9. Code Quality

- [ ] No giant god-component dominates the whole app
- [ ] File/module names are clear
- [ ] The implementation does not rely on fake mock architecture
- [ ] There is no unnecessary schema duplication
- [ ] The code is readable enough for Phase 2 work to continue cleanly

---

## 10. Reporting Requirements

Before Phase 1 is marked complete, the final report must include:

- [ ] What was built
- [ ] Where it lives
- [ ] Files changed
- [ ] Commands run
- [ ] What was intentionally deferred
- [ ] Known limitations
- [ ] Exact recommended Phase 2 scope
- [ ] A stop asking whether to proceed

---

## 11. Failure Conditions

Phase 1 should NOT be considered complete if any of the following are true:

- [ ] The viewport is fake or mostly fake
- [ ] The panel is mostly disconnected from real state
- [ ] Camera interaction is weak or broken
- [ ] The app structure already looks rewrite-prone
- [ ] Asset/BOM/export growth has been ignored architecturally
- [ ] The phase report hides missing work or overclaims completion
