# Muscle Vision — Product Requirements Document

## 1. Product Summary

**Muscle Vision** is an Astra-powered interactive 3D anatomy trainer that helps users understand how exercise technique changes muscle emphasis.

The user selects an exercise, grip, posture, playback speed, and viewing angle. A 3D anatomical human performs the exercise continuously on a stylized gym machine while relevant muscles are highlighted dynamically through the movement.

The core idea is:

> **Change how you move. See what changes inside your body.**

This is a hackathon prototype, not a medical or biomechanical simulator. It should be visually compelling, educational, easy to understand, and realistically buildable in approximately 3–4 hours.

## 2. WHAT — What Are We Building?

Muscle Vision is a futuristic, interactive 3D fitness and anatomy experience.

Instead of reading a static exercise guide, the user can:

- select an exercise
- select grip style
- select posture
- start and stop the movement
- change playback speed
- rotate and zoom around the anatomy while it is moving
- inspect front, side, and back views
- observe relevant muscles illuminate through the exercise cycle
- compare exercise variations
- use Astra-powered explanations to understand what changed

### Initial Exercise Scope

**Required / Hero**
- Seated Row

**Target**
- Lat Pulldown

**Stretch Goal**
- Chest Press

The project should prioritize depth and polish over a large exercise library.

## 3. HOW — How Will We Build It?

### Blender

Blender is used to prepare the 3D assets:

- anatomical human model
- armature / rig
- exercise animation
- stylized gym machine
- materials
- export to GLB / glTF

The anatomy should be visually detailed.

The gym machine should be visually simplified so it blends with the anatomy, using a futuristic style such as:

- transparent geometry
- wireframe accents
- cyan / blue edges
- holographic materials

### Three.js / React Three Fiber

Three.js is the interactive 3D runtime in the browser.

It will:

- load GLB assets
- play and loop exercise animations
- pause, resume, and reset animation
- adjust animation speed
- allow free camera orbit while motion continues
- provide front / side / back camera presets
- support zoom
- synchronize muscle highlighting with animation progress
- render the futuristic environment
- render visual transitions and click effects

### Exercise State Model

The application should maintain a simple shared state:

```json
{
  "exercise": "seated_row",
  "grip": "neutral",
  "posture": "upright",
  "speed": 1.0,
  "view": "front",
  "playing": true
}
```

Exercise variation data should be structured rather than scattered through the UI.

Example:

```json
{
  "exercise": "seated_row",
  "grip": "underhand",
  "posture": "upright",
  "muscles": {
    "latissimus_dorsi": "primary",
    "rhomboids": "primary",
    "biceps_brachii": "increased",
    "posterior_deltoid": "secondary"
  }
}
```

Use qualitative labels rather than unsupported activation percentages.

Preferred labels:

- Primary
- Secondary
- Increased emphasis
- Reduced emphasis
- Stabilizer

### Astra

GPT-6 Astra must provide meaningful product capability.

Astra should not be a decorative chatbot.

Useful Astra functions include:

- explain the current exercise configuration
- explain what changed after grip/posture changes
- compare two exercise variants
- reason over current app state
- guide the user to relevant muscles
- orchestrate parts of Demo mode

Example current state sent to Astra:

```json
{
  "exercise": "seated_row",
  "grip": "underhand",
  "posture": "upright",
  "speed": 0.5,
  "view": "back"
}
```

### ChatGPT Sites

The finished prototype must be deployable to ChatGPT Sites.

The deployed Site should support:

- normal interactive use by judges
- a dedicated **DEMO** button
- a scripted demo route or demo mode suitable for recording

## 4. HOW DOES IT WORK — User Experience

### Step 1 — Launch

The user enters a futuristic 3D exercise lab with:

- dark cinematic environment
- transparent floating panels
- cyan / blue holographic accents
- subtle ambient soundtrack
- anatomical human as the visual focus

### Step 2 — Select Exercise

The user selects an exercise such as:

- Seated Row
- Lat Pulldown

### Step 3 — Select Technique

The user chooses available options.

**Grip**
- Overhand
- Neutral
- Underhand

**Posture**
- Upright
- Slight forward lean
- Slight backward lean

### Step 4 — Play

The user presses **Play**.

The anatomical model performs the exercise continuously in a loop.

### Step 5 — Watch Muscle Activity

Muscle highlight intensity changes through the movement:

```text
START
  ↓
MOVEMENT / LOAD
  ↓
INCREASING EMPHASIS
  ↓
PEAK CONTRACTION
  ↓
STRONGEST HIGHLIGHT
  ↓
RETURN
  ↓
HIGHLIGHT REDUCES
  ↓
REPEAT
```

### Step 6 — Control Speed

Target speed controls:

- 0.25x
- 0.5x
- 1.0x
- 1.5x

### Step 7 — Rotate While Moving

The user can drag to orbit around the anatomy while the exercise continues.

Also provide:

- Front
- Side
- Back
- Reset View

### Step 8 — Pause and Inspect

The user can pause at any point, including peak contraction, then rotate around the frozen anatomy.

### Step 9 — Change Technique

The user can change grip or posture.

The app updates:

- pose / visual state where supported
- highlighted muscles
- insight panel
- comparison state

### Step 10 — Astra Explanation

The user clicks an Astra-powered action such as:

- Explain
- What Changed?
- Compare

Astra receives the current and previous state and explains the meaningful difference.

## 5. Core MVP Requirements

The first submit-ready MVP should include:

- futuristic visual shell
- transparent / holographic menus
- one working exercise
- looping movement
- play / pause / reset
- speed control
- free camera orbit
- zoom
- front / side / back views
- dynamic muscle highlighting
- at least one grip variation
- at least one posture variation
- Astra-powered explanation or comparison
- Demo button
- deployable to ChatGPT Sites

## 6. Visual Direction

### Environment

- futuristic gym / anatomy lab
- dark cinematic background
- glass / holographic panels
- subtle grid or technical lines
- cyan / blue accents
- restrained visual effects

### Anatomy

- detailed
- easy to inspect
- readable muscle separation
- target muscles use glow / emissive emphasis

### Machine

- stylized rather than photorealistic
- simplified geometry
- transparent / wireframe appearance
- should not overpower the anatomy

## 7. Audio

Normal site:
- subtle futuristic ambient sound
- mute control

Demo mode:
- trailer-like futuristic ambient music
- light UI click sounds
- transition whooshes
- subtle activation pulse

Do not build a complex audio system.

## 8. Astra Capability Requirement

The final prototype must make it obvious why Astra is present.

At least one of these must work end-to-end:

1. Explain the currently selected configuration.
2. Compare two variants and explain meaningful differences.
3. Explain what changed after a user changes grip/posture.
4. Orchestrate part of the live Demo flow.
5. Guide/highlight relevant anatomy based on current state.

Astra should operate on real application state rather than generic fitness prompts.

## 9. Non-Goals

Do not build:

- authentication
- accounts
- user profiles
- databases
- workout history
- workout plans
- nutrition
- calorie tracking
- payments
- leaderboards
- social features
- webcam pose estimation
- EMG prediction
- real-time biomechanical simulation
- physics-based muscle simulation
- large exercise library
- unnecessary backend infrastructure

## 10. Success Criteria

The prototype is successful when a judge can:

1. Open the deployed Site.
2. Select an exercise.
3. Select grip and posture.
4. Press Play.
5. Watch the exercise loop.
6. Adjust the movement speed.
7. Rotate around the anatomy while it is moving.
8. Pause and inspect the body.
9. Observe muscles highlight through the movement.
10. Change technique and see a meaningful difference.
11. Use an Astra-powered explanation or comparison.
12. Click DEMO and watch a polished <=90-second walkthrough.
