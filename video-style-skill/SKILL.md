---
name: video-style-skill
description: Define, apply, and verify a reusable video style across scripts, narration, covers, visuals, captions, motion, audio, and rendering. Use when creating or revising videos that must follow a style guide, match a previous video or series, turn a reference into a reusable style profile, keep multiple videos consistent, create a new video-style preset, or fix style drift such as the wrong voice, weak cover hierarchy, unnatural pacing, inconsistent captions, or stiff animation. Works with HyperFrames and other video workflows.
---

# Video Style Workflow

Treat a video style as a portable profile, not as a topic-specific prompt.

## Resolve the style source

Use the first available source:

1. A profile or preset named by the user.
2. A `style-profile.md` in the current project.
3. A profile derived from supplied references or an existing video.
4. A working profile created from [references/style-profile-template.md](references/style-profile-template.md).

When the user selects the bundled example, read [presets/college-social/profile.md](presets/college-social/profile.md) and use its adjacent assets.

Apply decisions in this order: current user instruction → selected profile → selected preset → neutral defaults. Never let a default override an explicit choice.

## Build the profile before the video

Define or infer these layers:

- audience, language, tone, and story structure;
- voice provider, voice identity, delivery, pauses, and audio mix;
- cover hierarchy and mobile-size readability;
- palette, typography, layout, cards, icons, imagery, and captions;
- motion vocabulary, transition rules, reveal timing, and settled holds;
- canvas, frame rate, duration, renderer, and quality gates.

Ask only for a missing decision that would materially change the result. Derive non-critical details coherently and record them in the working profile.

Do not silently replace a named voice, logo, font, brand color, reference asset, aspect ratio, or renderer. If a critical dependency is unavailable, retry when reasonable, report the limitation, and request approval before substituting it.

## Produce consistently

1. Write the spoken script before final timing.
2. Structure narration into semantic beats and use natural, varied pauses.
3. Design the cover as a deliberate first frame with one clear visual center.
4. Map each spoken beat to a visual change; avoid scenes that reveal everything immediately and then remain static.
5. Reuse the profile's visual tokens and motion vocabulary instead of inventing unrelated treatments scene by scene.
6. Align captions, effects, and transitions to meaning rather than equal time slices.
7. Preserve versioned outputs during revisions; do not overwrite an already delivered render.

Use the user's requested renderer. For HyperFrames projects, enter through `/hyperframes`, route footage-free topic explainers through `/faceless-explainer`, and run the HyperFrames checks before rendering. For another renderer, translate the same profile without changing its creative intent.

## Verify against the profile

Read [references/quality-checklist.md](references/quality-checklist.md) before final delivery. Inspect the cover and at least one settled frame per scene, confirm the actual audio source, and check that pacing, captions, palette, typography, motion, and output settings match the selected profile.

When creating a reusable style from a successful result, save the finalized profile and only the assets that materially help reproduce it.
