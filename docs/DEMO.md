# Muscle Vision — <=90 Second Demo Plan

## Purpose

The Demo button should launch a scripted walkthrough of the **real working application**.

The Demo is not a separate fake application.

It should be suitable for recording with OBS and submitting as the hackathon video.

Maximum duration: **90 seconds**

# Demo Goal

Within 90 seconds, demonstrate:

- futuristic 3D interface
- exercise selection
- looping anatomy animation
- muscle highlighting
- slow motion
- camera movement
- grip/posture variation
- Astra capability
- strong visual finale

# Scene Plan

## Scene 1 — Opening
**0–8 seconds**

Visual:
- dark screen
- futuristic ambient music begins
- subtle HUD / scanning effect
- MUSCLE VISION appears

Text:

> **MUSCLE VISION**  
> Change how you move. See what changes inside your body.

Transition into the lab.

## Scene 2 — Enter the Exercise Lab
**8–18 seconds**

Visual:
- transparent UI panels appear
- anatomical human appears
- stylized machine materializes
- Seated Row becomes selected

Action:
- exercise starts automatically

Show:
- anatomy moving
- machine moving
- subtle muscle highlighting beginning

## Scene 3 — Slow It Down
**18–30 seconds**

Action:
- speed changes from 1.0x to 0.5x
- then briefly to 0.25x

Visual:
- camera rotates toward rear / three-quarter view
- lats and rhomboids become more visible
- highlight intensity increases through the pull phase
- strongest glow around peak contraction

Optional overlay:

> Slow the movement. See the muscles work.

## Scene 4 — Change Grip
**30–43 seconds**

Action:
- Neutral Grip -> Underhand Grip

Visual:
- selected grip panel pulses
- subtle holographic transition
- hand position / state updates where supported
- muscle-emphasis visualization changes

## Scene 5 — Change Posture
**43–54 seconds**

Action:
- Upright -> slight backward lean

Visual:
- torso position changes
- highlight state updates
- camera shifts slightly to side / rear angle

Keep the movement running.

## Scene 6 — Astra: What Changed?
**54–67 seconds**

Action:
- trigger Astra-powered **What Changed?**

Astra receives:
- previous state
- current state

Display a concise explanation.

Example style:

> Underhand grip increases elbow-flexor contribution while the lats and rhomboids remain the primary pulling muscles.

Keep Astra output short enough to read quickly.

## Scene 7 — Compare
**67–79 seconds**

Action:
- Compare Neutral vs Underhand

Possible visual:
- split view
- side-by-side state
- or rapid A/B comparison if split-screen is too expensive

Highlight:
- common primary muscles
- meaningful difference

## Scene 8 — Finale
**79–90 seconds**

Visual:
- return to full anatomy scene
- smooth cinematic camera orbit
- exercise continues
- muscles glow at peak
- UI panels fade slightly
- music rises
- final title appears

Text:

> **MUSCLE VISION**

> **Slow it down. Rotate around it. See what moves you.**

Fade out.

# Demo Audio

## Music
Use one permitted futuristic ambient / cinematic track.

Desired character:
- futuristic
- energetic but not aggressive
- technical / medical-lab atmosphere
- trailer-like build

## Sound Effects
Keep lightweight:
- UI click
- holographic selection pulse
- camera / scene whoosh
- subtle muscle activation tone
- final reveal impact

## Audio Rules
- provide mute control
- do not overpower visuals
- do not build complex audio infrastructure
- use permitted / appropriately licensed audio only

# Demo Technical Requirements

- DEMO button visible in main Site
- use `/demo` route or explicit demo state
- demo should auto-run
- normal interactive Site remains available
- demo uses the same application components/state where practical
- demo can be exited
- demo should be deterministic enough for recording
- no manual typing required during the demo
- should complete in <=90 seconds

# Recording

Record the live Demo mode using OBS.

The final submitted video should show the real deployed/working prototype rather than a disconnected mock-up.
