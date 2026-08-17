# Video Style Skill

A reusable Codex Skill for defining, applying, and checking a consistent video style.

Instead of hard-coding one audience, language, voice, palette, or animation system, this project turns those decisions into a portable `style-profile.md`. Use it to keep a series consistent, match a reference video, package a successful look as a preset, or diagnose why a new video no longer feels like the rest.

![Example preset preview](video-style-skill/presets/college-social/approved-reference-contact-sheet.jpg)

## What it controls

- Story structure, audience, language, tone, and wording
- Voice provider, exact voice, delivery, pacing, pauses, and mix
- Cover hierarchy and first-frame readability
- Palette, typography, layout, cards, icons, imagery, and captions
- Motion vocabulary, transitions, reveal timing, and settled holds
- Canvas, frame rate, duration, renderer, versioning, and quality gates

The core Skill is renderer-neutral. It includes additional checks for HyperFrames but can translate the same profile to Remotion, an editor, or another video pipeline.

## Install

Clone the project, then copy only the installable Skill folder:

```bash
git clone https://github.com/zhaohe0307-lgtm/video-style-skill.git
cp -R video-style-skill/video-style-skill ~/.codex/skills/video-style-skill
```

Start a new Codex session after installation.

## Create your style profile

Copy the bundled template into a video project:

```bash
cp ~/.codex/skills/video-style-skill/references/style-profile-template.md \
  ./style-profile.md
```

Fill only the decisions that matter. The profile covers identity, content, narration, cover, visuals, captions, motion, audio, output, and quality gates.

Then invoke the Skill:

```text
Use $video-style-skill with ./style-profile.md to create a 45-second vertical explainer about compound interest.
```

```text
Use $video-style-skill to compare this draft with our style profile and fix the voice, cover hierarchy, captions, and stiff transitions.
```

```text
Use $video-style-skill to analyze these three reference videos and save their shared decisions as a reusable profile.
```

## Use a preset

The repository includes `college-social`, a complete Chinese university tutorial preset showing how a profile can freeze a voice, cover system, palette, motion language, templates, and visual references.

```text
Use $video-style-skill with the college-social preset to create a campus socialization explainer.
```

The preset is an example, not the global default. Add more presets by creating another folder under `presets/` with a `profile.md` and only the assets needed to reproduce it.

## Decision priority

The Skill resolves conflicts in this order:

1. Current user instruction
2. Selected style profile
3. Selected preset
4. Neutral non-critical defaults

It never silently substitutes a named voice, brand asset, font, aspect ratio, or renderer.

## Project structure

```text
video-style-skill/
├── README.md
├── docs/plans/
├── LICENSE
└── video-style-skill/              # copy this folder to Codex skills
    ├── SKILL.md
    ├── agents/openai.yaml
    ├── references/
    │   ├── quality-checklist.md
    │   └── style-profile-template.md
    └── presets/college-social/
        ├── profile.md
        ├── approved-frame.md
        ├── approved-reference-contact-sheet.jpg
        └── approved-template.html
```

## License

MIT — use it, adapt it, and publish your own presets.
