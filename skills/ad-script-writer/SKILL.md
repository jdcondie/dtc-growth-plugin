---
name: ad-script-writer
description: TikTok and video script production — competitor hook research, positioning gap identification, full scripts with structured sections, brand voice check, 10 hook variations per script, and editor production brief. No API needed. Triggers on "video script batch for [brand/product]", "write TikTok scripts for [brand]", or "script batch for [campaign/product]".
---

# Playbook 15: TikTok / Video Script System

From blank page to 3-5 fully scripted, brand-checked videos with a hook bank and production brief. No API needed.

## When to Use
Producing video content: TikTok, Reels, YouTube Shorts. Need scripts with structured hooks, body, and CTA — plus a brief for editors and talent.

## Inputs Required
- Brand name + product URL
- Competitor brands (2-3) for ad library pull
- Target audience + platform
- Angle or product focus (if known)

## Sequence

### Step 1 — Competitor Hook Research
Use `competitive-ads-extractor`
Pull competitor video ads. Identify: hook formats, stop-scroll patterns, content structures, POV styles, testimonial formats, proof types.
**Output:** Competitor hook reference doc.

### Step 2 — Positioning Gap
Use `marketing:competitive-analysis`
Identify what angle competitors are NOT using. What mechanism, proof style, or format is underrepresented?
**Output:** 1-2 gap angles worth owning. This is the creative territory for your scripts.

### Step 3 — Write Scripts
Use `marketing:draft-content`
Write 3-5 full video scripts per angle:
- Hook (0-3 sec): the stop-scroll line
- Tension/body (3-45 sec): problem, mechanism, proof
- CTA (final 5 sec): clear next action
Include: b-roll notes, on-screen text callouts, delivery tone notes.

### Step 4 — Brand Voice + Voice DNA Pass
Use `brand-voice:brand-voice-enforcement`, then apply `/CLAUDE/Voice DNA.md`.
**If no client brand voice file exists:** skip `brand-voice:brand-voice-enforcement` and apply Voice DNA only.
Scripts especially: short punchy lines for hooks, physical verbs for the body, vary sentence length.
Hook (0-3 sec) must pass Voice DNA: no negation flips, no banned structures, no em dashes, specific not vague.
"I spent $50k on ads before I figured out this one thing" beats "Discover the secret most brands miss."

### Step 5 — Hook Variations
Use `headline-writer`
Generate 10 hook variations per script. The first line is everything — give editors and talent options to test.

### Step 6 — Production Brief
Use `marketing:draft-content` (second pass)
Wrap everything into a video production brief: script + hook options + visual direction + editor/talent notes + format specs.

## Output Stack
- Competitor hook reference doc
- Positioning gap angles (1-2)
- 3-5 full scripts per angle
- 10 hook variations per script
- Production brief ready for editor/talent handoff

## Trigger Phrases
- "Video script batch for [brand/product] — [angle or product focus]"
- "Write TikTok scripts for [brand]"
- "Script batch for [campaign/product]"
