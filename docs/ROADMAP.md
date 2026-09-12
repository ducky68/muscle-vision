# Muscle Vision — Roadmap

## Working Rule

Build phase-by-phase.

At the end of each phase:

1. verify functionality
2. run available tests
3. run the production build
4. perform a browser smoke test
5. update `PROGRESS.md`
6. report completed / failed / deferred items
7. STOP and wait for approval

Do not automatically proceed to the next phase.

# Phase 0 — Bootstrap

## Goal
Create the working application shell.

## Tasks
- initialize frontend project
- configure Three.js / React Three Fiber
- create Sites-compatible structure
- create basic 3D canvas
- create futuristic background
- create transparent / holographic menu panels
- add placeholder anatomy object if final model is not ready
- add header with Muscle Vision branding
- add visible DEMO button
- verify local development startup
- verify production build

## Acceptance Criteria
- app starts successfully
- 3D canvas renders
- futuristic shell is visible
- transparent UI panels render
- no blocking runtime errors

## Milestone
**M0 — Shell works**

# Phase 1 — Core MVP

## Goal
Create one complete working exercise experience.

## Hero Exercise
**Seated Row**

## Tasks
- load anatomy model
- load / display stylized exercise machine
- play seated-row animation
- loop movement continuously
- implement Play
- implement Pause
- implement Reset
- implement speed controls: 0.25x / 0.5x / 1.0x / 1.5x
- implement orbit camera while animation continues
- implement zoom
- implement Front / Side / Back / Reset View
- synchronize basic muscle highlighting with animation progress
- strongest highlight around relevant contraction phase

## Acceptance Criteria
The user can start, loop, pause, reset, slow down, rotate, zoom, change view, and see target muscles highlight dynamically.

## Milestone
**M1 — Submit-ready core MVP**

# Phase 2 — Exercise Variations

## Goal
Show how technique changes muscle emphasis.

## Tasks
### Grip
- Overhand
- Neutral
- Underhand

### Posture
- Upright
- slight forward lean
- slight backward lean

### Behaviour
- available options depend on exercise
- selected state clearly visible
- lightweight transition effect on change
- update muscle emphasis data
- update anatomy / pose where supported
- update insight panel
- preserve smooth playback

## Acceptance Criteria
The user can change grip/posture and observe a visible, understandable difference.

## Milestone
**M2 — Strong interactive prototype**

# Phase 3 — Second Exercise

## Goal
Demonstrate the exercise engine is reusable.

## Target Exercise
**Lat Pulldown**

## Tasks
- add exercise selector
- add lat-pulldown animation
- configure machine state / asset
- configure grip options
- configure posture options
- configure muscle mapping
- reuse playback controls
- reuse camera controls
- reuse muscle highlight engine
- reuse insight panel

## Acceptance Criteria
The user can switch between Seated Row and Lat Pulldown without breaking the experience.

## Milestone
**M3 — Multi-exercise prototype**

# Phase 4 — Astra Capability

## Goal
Make Astra visibly useful.

## Minimum Astra Feature
Implement at least one complete Astra-powered workflow.

Preferred order:
1. What Changed?
2. Compare
3. Explain

## Tasks
- expose current app state to Astra
- preserve previous state for comparison
- implement concise explanation panel
- implement error/fallback state
- avoid generic chatbot UX
- make Astra output directly relevant to selected exercise state

## Acceptance Criteria
A judge can change a technique variable and trigger an Astra explanation clearly based on actual app state.

## Milestone
**M4 — Astra showcase**

# Phase 5 — Cinematic Demo

## Goal
Create the live <=90-second demo experience.

## Tasks
- implement `/demo` or equivalent demo mode
- DEMO button launches demo
- use real working application components
- scripted scene sequence
- automatic exercise selection
- automatic speed change
- automatic camera movement
- muscle highlight sequence
- grip/posture change
- Astra explanation or comparison
- futuristic ambient music
- lightweight UI sound effects
- strong opening
- strong final reveal
- include mute control
- allow exit back to interactive mode

## Acceptance Criteria
- demo runs without manual intervention
- demo completes in <=90 seconds
- demo showcases real product functions
- demo showcases Astra capability
- suitable for OBS recording

## Milestone
**M5 — Demo ready**

# Phase 6 — Polish and Deploy

## Goal
Ship the project.

## Tasks
- improve loading state
- improve error handling
- polish camera transitions
- polish selection effects
- verify responsive layout
- verify audio controls
- optimize 3D asset loading where practical
- production build
- deploy to ChatGPT Sites
- smoke test deployed Site
- verify normal interactive mode
- verify Demo mode
- verify Astra workflow

## Acceptance Criteria
- deployed Site loads
- core functionality works
- Demo button works
- no major broken flows
- project is ready for judges

## Milestone
**M6 — Deployed**

# Stretch — Only If Ahead of Schedule

## Phase 7 — Chest Press

Possible additions:
- Chest Press exercise
- grip / elbow-position variation
- chest / anterior deltoid / triceps highlighting

Do not begin this phase unless Phases 0–6 are stable.

# Feature Priority Under Time Pressure

1. working Site shell
2. working 3D scene
3. exercise animation
4. play / pause / speed
5. camera orbit
6. muscle highlighting
7. grip / posture variations
8. Astra capability
9. Demo mode
10. deployment verification
11. second exercise
12. visual polish
13. third exercise

Astra capability and Demo mode must exist before final submission.
