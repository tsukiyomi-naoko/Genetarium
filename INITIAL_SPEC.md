# Aquarium Environment Builder — Initial Product Specification

## 1. Project Summary

Aquarium Environment Builder is a browser-based configurator for designing aquarium/tank environments with a strong real-time 3D viewport, live editing, camera interaction, configurable assets, and fabrication/planning outputs.

This is not just a visual mockup tool. It is intended to become a serious browser application that combines:

- visual aquarium/tank configuration
- real-time 3D scene editing
- metadata-rich asset management
- printable-part export support
- purchased-item identification
- master build/materials listing

The overall goal is to let a user design an aquarium environment in a premium, highly interactive browser UI and then extract practical outputs for fabrication, sourcing, and assembly.

---

## 2. Core Product Goals

### 2.1 Browser-based experience
The application must run in a browser and provide a smooth, modern configurator workflow.

### 2.2 Real-time 3D editing
The user must be able to see changes immediately in a strong 3D view and freely manipulate the camera.

### 2.3 Configuration-heavy UI
The interface should support a large number of sliders, toggles, dropdowns, numeric inputs, presets, and eventually drag-and-drop interactions.

### 2.4 Data-first architecture
Objects and scene elements must be driven by structured data, not only by visuals, so the application can later support exports, BOM generation, and fabrication-aware features.

### 2.5 Fabrication and sourcing outputs
3D-printable items must be exportable or prepared for export in a printable workflow, while non-printable items must be listed clearly by specific/common orderable identity.

---

## 3. Product Direction

### 3.1 V1 focus
The first meaningful version should focus on:

- freshwater-oriented environments first
- rectangular tanks first
- strong live viewport and camera interaction first
- slider-heavy editing first
- metadata-first asset foundations from the start
- future export/BOM support designed in from the beginning

### 3.2 Design philosophy
The product should feel like a premium configurator, similar in spirit to modern PC builders and organizer/design tools, but adapted for aquarium environment creation.

The builder should emphasize:

- immediacy
- clarity
- strong visual feedback
- modular architecture
- growth without rewrite

---

## 4. Non-Negotiable Requirements

## 4.1 Real-time 3D viewport
The app must include a real-time interactive 3D scene where changes update immediately.

Minimum required behavior:

- live visual updates from control changes
- orbit camera
- pan camera
- zoom camera
- readable perspective view
- front / side / top preset views
- frame whole tank
- preparation for focus on selected object
- strong visual readability for tank, water, substrate, and basic scene contents

The viewport is not decorative. It is a primary editing surface.

## 4.2 Live edit loop
The user must be able to change parameters and instantly see the result.

Examples:
- tank dimensions update tank geometry live
- water level updates live
- substrate depth/slope updates live
- visual settings change immediately
- object visibility and future placement changes update immediately

## 4.3 Control-heavy UI shell
The interface must support a left-side or equivalent configuration panel with room for many future controls.

Expected categories include:
- Tank
- Substrate
- Hardscape
- Plants / Decor
- Equipment
- Lighting / Background
- Presets
- Build / Materials

## 4.4 Scene architecture separation
The project must clearly separate:
- domain/state data
- rendering logic
- UI controls
- asset metadata
- export/list logic

This separation is mandatory to avoid collapse into a hard-to-maintain demo architecture.

---

## 5. Tank / Scene Configuration Scope

The system should be designed to support at least the following categories over time.

## 5.1 Tank
- length
- depth
- height
- rimless / rimmed / braced variations
- lid/open-top state
- glass-related display options
- water level

## 5.2 Substrate
- depth
- front/rear distribution
- slope
- material style/category
- color/look metadata

## 5.3 Hardscape
- rocks
- driftwood
- caves
- hides
- future placeable scene objects

## 5.4 Plants / Decorative content
- plant groupings
- leaves
- moss-like decorations
- artificial or purchased decor
- placement-ready object model

## 5.5 Equipment
- filters
- heaters
- tubing
- lights
- holders
- clips
- mounts
- other tank accessories

## 5.6 Visual environment
- lighting feel
- background
- water appearance
- surface atmosphere

---

## 6. Asset Classification Model

Every placeable or configurable item must belong to one of the following categories:

### 6.1 Printable
Items intended to be fabricated through 3D printing or a similar output workflow.

Examples:
- clips
- brackets
- holders
- dividers
- guards
- custom caves
- feeding rings
- tube guides

### 6.2 Purchased
Items that are not intended to be printed and must instead be purchased or sourced.

Examples:
- leaves
- plants
- substrate
- heaters
- sponge filters
- airline tubing
- biomedia
- lights
- suction cups when off-the-shelf
- driftwood
- rocks

### 6.3 Hybrid
Items that involve both printed and purchased components.

Examples:
- printed holder + suction cups
- printed frame + mesh
- printed mount + acrylic insert
- printed guide + silicone tube

This classification must be reflected in shared metadata types, not only in UI labels.

---

## 7. Fabrication / Materials Requirements

The app must be designed so that each printable-capable asset can later support:

- recommended material
- alternate material
- quantity
- notes
- additional required materials/hardware
- export relationship to print-ready file generation

Examples of recommended materials:
- PLA
- PETG
- TPU
- ABS/ASA later where appropriate

The app must also be designed so that purchased items can support:

- specific/common item name
- category
- quantity
- notes
- orderable identity or supplier-facing naming later

Hybrid items must support both printed and purchased dependencies.

---

## 8. Required Planning Outputs

The product must be architected so a scene can later generate:

## 8.1 Printable Export Package
For printable items:
- part name
- quantity
- export relationship
- recommended material
- alternate material
- additional required materials
- notes

## 8.2 Master Build List
A master list containing:
- printable parts
- purchased items
- hybrid dependencies
- consumables
- additional materials/hardware

The master list should eventually function like a fabrication + sourcing sheet.

---

## 9. Technical Direction

Preferred stack for the implementation path:

- React
- TypeScript
- Vite
- React Three Fiber / Three.js
- lightweight explicit state layer such as Zustand
- modular domain types
- modular component structure

The implementation should favor:

- strong typing
- explicit interfaces
- maintainable boundaries
- future export/list support
- browser performance
- smooth scene interaction

---

## 10. Phase-Based Delivery Rules

This project must be executed in explicit phases.

For every phase:
1. define the scope
2. implement only that scope
3. stop at the end
4. summarize completed work
5. list changed files
6. list open issues / known limitations
7. recommend the next phase
8. ask whether to proceed

No uncontrolled scope creep.

No fake completeness.

No skipping phase stops.

---

## 11. Phase 1 Definition

## 11.1 Goal
Build the app shell and the live 3D foundation.

## 11.2 Required outcomes
Phase 1 must include:
- browser app foundation
- application layout
- control panel shell
- real 3D viewport
- working camera controls
- basic tank visualization
- live state-driven updates from controls to scene
- foundational scene/store/types
- code structure that clearly supports later phases

## 11.3 Explicitly not required in Phase 1
Phase 1 does not need to fully implement:
- advanced drag-and-drop asset placement
- full export pipeline
- full BOM generation
- full object selection workflow
- full preset library
- full save/load system
- advanced equipment rules
- advanced performance optimization beyond sensible defaults

Those should only be scaffolded where necessary.

---

## 12. Definition of Done for Phase 1

Phase 1 is considered complete only if:

- the app runs locally
- the main layout is usable
- the viewport is genuinely interactive
- camera orbit/pan/zoom works well
- at least a basic tank representation is visible
- multiple controls update the 3D scene in real time
- module boundaries are clean enough for future phases
- the foundation clearly supports later asset metadata and master list work

---

## 13. Architecture Guardrails

Avoid the following:
- giant god-components
- fake mock UI disconnected from real state
- duplicated schema definitions
- direct coupling between export logic and rendering internals
- hidden ad hoc component state for scene-critical data
- placeholder architecture that must later be thrown away
- uncontrolled phase creep
- purely visual hacks that block real growth

Prefer:
- explicit domain models
- clean store updates
- renderer components that consume state rather than own product truth
- shared types/interfaces
- gradual growth without rewrite

---

## 14. Long-Term Growth Path

Likely future phases after Phase 1:
- richer parametric tank controls
- substrate and water refinement
- object library and placement
- picking / selection / manipulation
- asset metadata-backed library
- master build list generation
- printable export workflows
- save/load scenes
- preset system
- fabrication- and sourcing-aware validation

This spec is intentionally meant to support that path from the start.
