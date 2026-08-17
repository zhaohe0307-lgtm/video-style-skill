# Approved style specification

## Output

- Canvas: 1080×1920 portrait.
- Frame rate: 30 fps.
- Typical duration: 35–50 seconds; let natural narration determine the final duration.
- Audience: Chinese university students.
- Tone: practical senior-student guidance, friendly and grounded, never preachy.

## Story and wording

Use this spine when appropriate:

1. Large-title cover and one-sentence hook.
2. Correct one common misconception before giving advice.
3. Present 3–5 concrete actions in causal order.
4. Close with three memorable qualities or one reassuring sentence.

Write as spoken Mandarin. Prefer short clauses, specific verbs, and connective logic such as “先别误会”, “第一”, “真做不到，也提前说一声”. Avoid slogan piles, abrupt fragments, corporate jargon, fake statistics, and advice that promotes people-pleasing or manipulation.

## Voice and pauses

Use Microsoft Edge TTS voice `zh-CN-YunxiNeural`.

- Base pitch: `-2Hz`; use `-3Hz` only for a slightly firmer dense step.
- Opening: rate around `+4%`.
- Explanatory paragraphs: `+5%` to `+8%`.
- Closing: around `+3%`.
- Generate one semantic paragraph per file.
- Trim leading and trailing silence from every segment.
- Reinsert varied pauses of roughly 240–380 ms between paragraphs. Do not use identical gaps everywhere.
- Master the concatenated voice with `highpass=f=70`, `lowpass=f=14000`, and `loudnorm=I=-16:TP=-1.5:LRA=9`.
- Use low transition SFX volume, approximately `0.07`, and never let it compete with the voice.

If the Yunxi service is temporarily unavailable, retry the same voice. Do not fall back to Reed, Tingting, or another system voice without telling the user.

## Cover

Create one dominant topic title, readable immediately at phone size.

- Use approximately 145–155 px heavy type for the main title.
- Keep supporting pills small and secondary.
- Use one short sticker subtitle only when it clarifies the angle.
- Avoid several competing headlines, a long paragraph, or a fragmented title hierarchy.
- A reliable structure is: small category pill → one two-line topic title → one short sticker qualifier.

Approved example: `大学生 / 社会化指南`, with `不圆滑 · 不讨好` as the small qualifier.

## Visual system

- Backgrounds alternate cream `#FFF8EF` and pale blue `#EEF5FF`.
- Ink: `#243247`; primary blue: `#2672EA` / `#4B8FFF`.
- Supporting stickers: coral `#FF7D66`, yellow `#FFD467`, mint `#7ED9C5`.
- Cards use a 4 px dark border, about 40 px radius, and offset soft shadow.
- Use large headings, one decision or action per screen, ample empty space, and original thick-line SVG icons.
- Grid cards must use `position: relative`; do not let a shared absolute-card rule collapse grid items onto each other.

## Motion

Use a single paused GSAP timeline registered on `window.__timelines`.

- Scene entrances: about 54 px horizontal movement, alternating direction, 0.65–0.70 s, `power3.out`.
- Headers: about 22 px vertical movement, 0.55 s, `power2.out`.
- Cards: about 38–46 px vertical movement, 0.70–0.75 s, `power3.out`.
- Paired cards: stagger 0.12–0.18 s.
- Sticker emphasis: scale from about 0.94 to 1 with `power3.out`.
- Use `back.out`, elastic, or bounce only if the user explicitly asks for a playful bouncy register.
- Reveal elements across the spoken paragraph and leave a short settled hold before the next scene.

The approved style should feel alive but composed: smooth beats bouncy.

## Quality gates

- Confirm the audio file really uses the Yunxi render, not a stale system-voice file.
- Confirm root, audio, scene clips, SFX, and the GSAP timeline share the same final duration.
- Run `hyperframes check` until it passes.
- Snapshot the cover and settled frame of every scene.
- Inspect for clipped titles, overlapping cards, empty late frames, and visual reveals that lag behind narration.
