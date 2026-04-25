---
name: creative-brief-generator
description: Creative brief production sequence — competitor ad research, positioning gap identification, brief drafting, brand voice check, and hook bank generation. Use when briefing a designer, video editor, or UGC creator on a new ad batch. Triggers on "build a creative brief for [product/campaign]", "brief the creative team on [brand]", or "I need ad briefs for [brand]".
---

# Playbook 06: Creative Brief Builder

From raw angle to a fully deployable creative brief with a hook bank attached. One session.

## When to Use
Need to brief a designer, video editor, or UGC creator on a new batch of ads. Have a product or campaign but no brief yet.

## Inputs Required
- Brand name + product URL
- Competitor names (2-3)
- Target audience + platform (Meta, TikTok, etc.)

## Sequence

### Step 1 — Competitor Ad Reference
Use `competitive-ads-extractor`
Pull competitor ads for the product/category. Identify: formats performing, hook types, proof styles, offer structures.
**Output:** Competitor ad reference doc. This is the creative landscape map.

### Step 2 — Positioning Gap
Use `marketing:competitive-analysis`
Extract the messaging gap — what angle are competitors NOT using? What proof type is missing? What format is underrepresented?
**Output:** 1-2 gap angles. The brief owns one of these. This step determines brief quality.

### Step 3 — Draft the Brief
Use `marketing:draft-content`
Write the full creative brief: hook angles, visual direction, copy lines, offer framing, CTA, do/don't examples, format specs.
**Brief input:** The gap angle from Step 2 is the north star. Brief everything around it.

### Step 4 — Brand Voice Check
Use `brand-voice:brand-voice-enforcement`
Run the brief through voice check. Confirm tone, terminology, and positioning are on-brand before it goes to the creative team.
**If no client brand voice file exists:** skip this step and proceed to Step 4b.

### Step 4b — Voice DNA Pass
Reference `/CLAUDE/Voice DNA.md` and apply to all copy lines in the brief: hook angles, CTA copy, do/don't examples.
Physical verbs over generic ones. Specific details over vague claims. Short punchy lines for hooks.
Fail any hook that uses a banned word or banned sentence structure.

### Step 5 — Hook Bank
Use `headline-writer`
Generate 10 hook/headline variations per angle. Attach directly to the brief as testable options for editors and talent.
**Brief input:** Every hook is a variation on the gap angle — not a scatter.

## Output Stack
- Competitor ad reference doc
- Positioning gap rationale
- Fully formatted creative brief
- 10 hook variations per angle (attached to brief)

## Trigger Phrases
- "Build a creative brief for [product/campaign] — [brand name]"
- "Brief the creative team on [brand]"
- "I need ad briefs for [brand]"

## Notes
Brief quality is set in Step 2, not Step 3. If the gap is weak or generic, the brief will be too.
Do not send the brief without running Step 4 — tone drift in a creative brief compounds downstream.
