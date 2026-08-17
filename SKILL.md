---
name: college-social-video-style
description: Create or revise Chinese vertical social-media explainer videos in Mona's approved college-student tutorial style. Use for university-student education, socialization, first-time life guides, campus growth, practical how-tos, or when the user says to match the previously approved video, use the same voice, make it less stiff, add a large cover title, or follow the established style. Applies to HyperFrames video creation and edits unless the user explicitly requests a different visual or voice direction.
---

# Approved College Social Video Style

Treat this skill as the user's default for related Chinese vertical explainers. Follow the user's current instructions when they conflict with these defaults.

## Start correctly

1. Use `/hyperframes` as the mandatory video entry point.
2. For topic explainers without source footage, route to `/faceless-explainer`.
3. Read [references/style-spec.md](references/style-spec.md) before writing the script, generating voice, or designing frames.
4. Use [assets/approved-template.html](assets/approved-template.html) as the preferred structural seed when it fits the request.
5. Use [assets/approved-frame.md](assets/approved-frame.md) and [assets/approved-reference-contact-sheet.jpg](assets/approved-reference-contact-sheet.jpg) as the approved visual baseline.

## Preserve the approved character

- Keep the narration conversational, calm, and logically connected.
- Use the approved Yunxi neural male voice; never silently substitute a macOS system voice.
- Make the cover a single, obvious visual center with a very large topic title.
- Keep the cream/light-blue sticker-card system and original thick-line SVG icons.
- Prefer gentle fades and small moves. Avoid repeated hard pushes and bouncy card entrances.
- Pace reveals across the spoken sentence so the scene develops instead of freezing after its first second.

## Build and verify

1. Write the spoken script before final timing.
2. Generate narration in separate semantic paragraphs and derive scene boundaries from the processed audio.
3. Align visual entrances with meaning, not merely equal time slices.
4. Run `hyperframes check` after every HTML edit and fix all errors.
5. Capture a cover frame plus one settled frame per scene. Compare them with the approved contact sheet.
6. Render only after confirming the cover, voice source, scene timing, and card layout.

Do not overwrite a previously delivered MP4 during revisions; render a versioned file such as `*-v2.mp4`.
