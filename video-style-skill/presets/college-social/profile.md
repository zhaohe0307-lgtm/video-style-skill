# College social explainer profile

This complete example implements the generic video-style profile for Chinese university-student tutorials.

## Identity

- Profile name: `college-social`
- Purpose: Make practical campus and first-time-life guidance feel friendly, useful, and composed.
- Reference sources: [approved-frame.md](approved-frame.md), [approved-reference-contact-sheet.jpg](approved-reference-contact-sheet.jpg), and [approved-template.html](approved-template.html).
- Must preserve: Yunxi voice, natural semantic pauses, one-center cover, cream and pale-blue sticker cards, restrained motion.
- Must avoid: preachy wording, people-pleasing advice, competing headlines, silent voice substitution, and bouncy repeated entrances.

## Content

- Audience: Chinese university students.
- Language and locale: Spoken Mandarin, China.
- Topics: Socialization, campus growth, first-time life tasks, practical how-tos.
- Tone: Friendly senior-student guidance; grounded and never preachy.
- Story pattern: Large-title hook → correct one misconception → 3–5 causal actions → reassuring close.
- Wording rules: Prefer short clauses, concrete verbs, and connective logic. Avoid slogan piles, abrupt fragments, corporate jargon, fake statistics, and manipulation.

## Narration

- Voice provider: Microsoft Edge TTS.
- Voice identity: `zh-CN-YunxiNeural`.
- Delivery: Calm, conversational, lightly energetic.
- Rate and pitch: Opening `+4%`; explanations `+5%` to `+8%`; closing `+3%`; base pitch `-2Hz`.
- Pause logic: Generate semantic paragraphs separately, trim edge silence, then insert varied 240–380 ms gaps.
- Allowed fallback: None without telling the user and receiving approval.

Master voice with `highpass=f=70`, `lowpass=f=14000`, and `loudnorm=I=-16:TP=-1.5:LRA=9`. Keep transition effects around `0.07` relative level.

## Cover

- Visual center: One dominant topic title.
- Main title: Approximately 145–155 px heavy type, normally two lines.
- Supporting text: One small category pill and, only when useful, one short sticker qualifier.
- First-frame promise: The topic and angle are immediately readable at phone size.
- Avoid: Multiple headlines, long paragraphs, fragmented hierarchy, and decorative competition.

## Visual system

- Canvas background: Cream `#FFF8EF` alternating with pale blue `#EEF5FF`.
- Primary palette: Ink `#243247`; blue `#2672EA` and `#4B8FFF`.
- Accent palette: Coral `#FF7D66`, yellow `#FFD467`, mint `#7ED9C5`.
- Typography: Large, heavy headings with compact supporting copy.
- Layout: One action or decision per screen with generous empty space.
- Shapes and borders: Cards use a 4 px dark border, about 40 px radius, and an offset soft shadow.
- Icons and imagery: Original thick-line SVG icons and sticker-like accents.

## Captions

- Caption mode: Short semantic phrases rather than dense transcription.
- Position and safe area: Keep clear of platform controls and card edges.
- Highlight behavior: Use the limited accent palette; do not animate every word.
- Maximum lines: Prefer one or two concise lines.

## Motion

- Motion character: Alive but composed.
- Scene entrances: About 54 px horizontal movement, 0.65–0.70 s, `power3.out`, alternating direction.
- Headers: About 22 px vertical movement, 0.55 s, `power2.out`.
- Cards: About 38–46 px vertical movement, 0.70–0.75 s, `power3.out`.
- Stagger: 0.12–0.18 s for paired cards.
- Emphasis: Scale from about 0.94 to 1 with `power3.out`.
- Reveal timing: Spread reveals across the spoken paragraph and leave a short settled hold.
- Forbidden motion: Bounce, elastic, and `back.out` unless explicitly requested.

For the approved HyperFrames seed, use one paused GSAP timeline registered on `window.__timelines`. Keep grid cards `position: relative` so shared absolute rules cannot collapse them.

## Output

- Renderer: HyperFrames.
- Canvas: 1080 × 1920 portrait.
- Frame rate: 30 fps.
- Typical duration: 35–50 seconds, led by natural narration.
- Versioning: Never overwrite a delivered MP4; use names such as `topic-v2.mp4`.

## Quality gates

- Confirm the audio file is the Yunxi render rather than a stale system voice.
- Confirm all tracks and timelines share the final duration.
- Run `hyperframes check` until it passes.
- Snapshot the cover and one settled frame per scene.
- Inspect clipped titles, overlapping cards, empty late frames, and visual reveals that lag behind narration.
