# Video Style Skill Design

## Goal

Turn the existing personal college-video preset into a public, reusable project that lets any Codex user define and consistently apply a video style.

## Architecture

The repository is a distribution wrapper. The installable skill lives in `video-style-skill/`; public documentation and project plans stay outside that folder. The core skill is topic-, language-, voice-, palette-, and renderer-neutral. A style profile defines the creative decisions, while presets provide complete examples.

Style resolution follows this priority:

1. Current user instruction.
2. Selected style profile.
3. Selected preset.
4. Explicit neutral defaults for non-critical details only.

Never silently replace critical choices such as a named voice, logo, font, or rendering requirement.

## Components

- `video-style-skill/SKILL.md`: concise engine-neutral workflow and resource routing.
- `video-style-skill/references/style-profile-template.md`: copyable profile covering story, voice, cover, visuals, captions, motion, output, and quality gates.
- `video-style-skill/references/quality-checklist.md`: renderer-independent review checklist with a HyperFrames section.
- `video-style-skill/presets/college-social/`: the original approved college-social style as a complete example preset.
- `README.md`: project introduction, installation, customization, examples, and directory map outside the installable Skill folder.

## User flow

Users copy the profile template, fill only the decisions they care about, and invoke `$video-style-skill` with either that profile or a bundled preset. The skill derives missing non-critical details consistently, creates the video, and verifies the output against the profile. For HyperFrames projects it also runs the standard timing, snapshot, and render checks.

## Verification

Run the official skill validator on `video-style-skill/`, verify every Markdown link and preset path, confirm the example binary asset is present, and compare the published GitHub tree with the local project.
