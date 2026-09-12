# Muscle Vision — References

## Purpose

Use these references to improve:

- anatomy accuracy
- exercise terminology
- exercise mechanics
- 3D asset preparation
- interaction design

Accuracy is more important than adding many variations.

Do not invent precise muscle-activation percentages.

# 1. Z-Anatomy

## Purpose
Preferred starting point / reference for 3D human anatomy assets.

Use for:
- Blender anatomy reference
- anatomical mesh organization
- muscle structures
- possible source model subject to license compliance

Repository:
https://github.com/Z-Anatomy/Models-of-human-anatomy

## Notes
- check the current license before using/distributing assets
- preserve required attribution
- do not assume all assets can be redistributed without review

# 2. Kenhub

## Purpose
Anatomical reference.

Use for:
- correct muscle names
- location
- anatomical relationships
- origin / insertion / function background where needed

Website:
https://www.kenhub.com/

## Rule
Use as a knowledge reference. Do not copy proprietary images/assets into the project without permission.

# 3. ACE Exercise Library

## Purpose
Primary exercise-mechanics reference.

Use for:
- exercise setup
- movement path
- posture
- technique
- exercise naming
- safety-oriented movement descriptions

Exercise library:
https://www.acefitness.org/resources/everyone/exercise-library/

## Priority Exercises
Research first:
- Seated Row
- Lat Pulldown
- Chest Press

# 4. BioDigital Human

## Purpose
Visual / interaction inspiration.

Use for ideas such as:
- rotating anatomy
- isolating structures
- zooming
- interactive layers
- anatomy-first UX

Website:
https://www.biodigital.com/

## Rule
Use for inspiration only. Do not copy proprietary 3D assets or interface assets.

# 5. MuscleWiki

## Purpose
Secondary UX and exercise-to-muscle visualization reference.

Use for:
- exercise categorization
- exercise-to-muscle relationship inspiration
- simple muscle visualization patterns

Website:
https://musclewiki.com/

## Rule
Treat as a supporting reference rather than the sole anatomical authority.

# Evidence Rules

## Use qualitative labels
Preferred:
- Primary
- Secondary
- Increased emphasis
- Reduced emphasis
- Stabilizer

Avoid unsupported claims such as:

```text
Lat activation: 92%
Biceps activation: 74%
```

unless a credible source explicitly supports the exact measurement and context.

# Variation Accuracy

Grip/posture variations are the area most likely to produce oversimplified claims.

Before implementing a meaningful visual difference:

1. verify the exercise
2. verify the grip/posture variation is legitimate
3. verify the directional muscle-emphasis claim
4. use conservative language
5. do not overstate certainty

If the difference cannot be supported confidently, keep the visualization unchanged or omit the variation.

# MVP Research Priority

## Seated Row
Investigate:
- neutral grip
- overhand grip
- underhand grip
- upright torso
- controlled forward position
- slight backward lean
- lats
- rhomboids
- posterior deltoid
- trapezius
- biceps

## Lat Pulldown
Investigate:
- wide overhand grip
- neutral grip
- underhand grip
- upright torso
- slight backward lean
- latissimus dorsi
- biceps
- teres major
- scapular retractors / stabilizers where relevant

## Chest Press — Stretch
Investigate only if time remains:
- standard press
- elbow-path variation
- pectoralis major
- anterior deltoid
- triceps

# Technical References

## Three.js
Official docs:
https://threejs.org/docs/

Use for:
- GLTFLoader
- AnimationMixer
- OrbitControls
- materials
- camera animation
- rendering loop

## React Three Fiber
https://r3f.docs.pmnd.rs/

## Blender
https://docs.blender.org/

Use for:
- armatures
- rigging
- animation
- glTF / GLB export

# Asset Rules

- prefer open / permitted assets
- document the license
- retain required attribution
- do not scrape proprietary assets
- do not copy commercial anatomy models without permission
- optimize models for browser delivery where practical

# Audio Rules

Use only:
- royalty-free
- CC0
- appropriately licensed
- or otherwise permitted audio

Keep attribution if required.

Do not spend hackathon time building a music-generation pipeline unless directly necessary.
