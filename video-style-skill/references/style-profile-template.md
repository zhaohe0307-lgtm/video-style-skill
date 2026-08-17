# Video style profile

Copy this file to the video project as `style-profile.md`. Replace bracketed prompts and delete guidance that does not apply.

## Identity

- Profile name: `[short stable name]`
- Purpose: `[what this style should help viewers feel or do]`
- Reference sources: `[files, URLs, or previous videos]`
- Must preserve: `[non-negotiable traits]`
- Must avoid: `[known failure modes]`

## Content

- Audience: `[who the video is for]`
- Language and locale: `[for example, English-US or Mandarin-China]`
- Topics: `[best-fit subject areas]`
- Tone: `[for example, calm, witty, premium, direct]`
- Story pattern: `[hook, explanation, actions, close]`
- Wording rules: `[sentence length, terminology, calls to action]`

## Narration

- Voice provider: `[service or local engine]`
- Voice identity: `[exact voice name when required]`
- Delivery: `[warm, restrained, energetic, authoritative]`
- Rate and pitch: `[values or relative guidance]`
- Pause logic: `[short, medium, and long pause use]`
- Pronunciation rules: `[names, acronyms, numbers]`
- Allowed fallback: `[explicitly approved substitute or none]`

## Cover

- Visual center: `[single main subject or title]`
- Main title: `[line count, size, weight, safe area]`
- Supporting text: `[optional eyebrow, subtitle, or badge]`
- First-frame promise: `[what must be understood immediately]`
- Avoid: `[competing headlines, clutter, low contrast]`

## Visual system

- Canvas background: `[colors, texture, image treatment]`
- Primary palette: `[hex values or named tokens]`
- Accent palette: `[limited supporting colors]`
- Typography: `[families, weights, hierarchy]`
- Layout: `[grid, margins, card system, density]`
- Shapes and borders: `[radius, stroke, shadow]`
- Icons and imagery: `[line style, photo treatment, illustration rules]`
- Brand assets: `[paths and placement constraints]`

## Captions

- Caption mode: `[full sentence, phrase, karaoke, keywords only]`
- Position and safe area: `[placement]`
- Typeface and size: `[mobile-readable values]`
- Highlight behavior: `[color, scale, background, timing]`
- Maximum lines and characters: `[limits]`

## Motion

- Motion character: `[composed, playful, cinematic, kinetic]`
- Entrances: `[fade, slide distance, duration, easing]`
- Exits and transitions: `[rules]`
- Stagger: `[range and grouping logic]`
- Emphasis: `[scale, pulse, draw, mask, none]`
- Reveal timing: `[how motion follows spoken meaning]`
- Forbidden motion: `[bounce, hard push, rapid zoom, etc.]`

## Audio mix

- Voice target: `[loudness and peak]`
- Music role: `[genre, energy, level, ducking]`
- Sound effects: `[allowed types and level]`
- Silence and breathing room: `[rules]`

## Output

- Renderer: `[HyperFrames, Remotion, editor, or unspecified]`
- Canvas: `[width × height and orientation]`
- Frame rate: `[fps]`
- Typical duration: `[range or content-led]`
- Delivery format: `[codec, container, filename rules]`
- Versioning: `[for example, name-v2.mp4]`

## Quality gates

- `[cover readable at phone size]`
- `[actual voice matches the named source]`
- `[all scenes have meaningful visual development]`
- `[captions remain inside safe areas]`
- `[no clipped, overlapping, stale, or empty frames]`
- `[renderer-specific checks pass]`

## Renderer notes

Record implementation details that reproduce the style without turning renderer quirks into creative rules.
