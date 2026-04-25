---
name: brand-voice-profiler
description: Profiles a brand's writing voice from 3-5 content samples. Reads existing brand-dna.md (if present) and the supplied content, then produces a brand-voice.md file covering tone keywords, sentence rhythm, banned phrases, signature moves, and 5 voice rules a writer can follow. Use when the user asks to profile a voice, build a voice file, codify how a brand writes, or after building brand DNA.
---

# Brand Voice Profiler

Codifies how a brand writes so any future content (emails, ads, posts, landing pages) sounds like the same hand wrote it.

## When to run

After `brand-dna-builder` has produced `brand/brand-dna.md`, or anytime the user provides 3-5 content samples and wants a voice file.

## Inputs you need

1. **Content samples.** 3-5 pieces. Newsletters, emails, landing page copy, tweets. Real, not generated.
2. **Optional:** existing `brand/brand-dna.md` (read it if present, use the tone keywords as a calibration check).

If the user hasn't provided samples, ask once: "Paste 3-5 pieces of content, or point me to a folder/URL."

## Output

Write to `brand/brand-voice.md`. Format:

```
# [Brand] Voice Profile

## Tone keywords
5-7 adjectives. Specific. "Direct, irreverent, lived-in" beats "professional, friendly."

## Sentence rhythm
- Average sentence length
- Paragraph length (1-3 sentences? 4-6?)
- How they vary (short punchy + long carrying)

## Signature moves
3-5 patterns this brand uses repeatedly. Examples:
- Opens with a stat, not a hook
- Parenthetical asides for editorial commentary
- Closes with a question, not a CTA
- Ends paragraphs on a single short sentence

## Banned phrases / structures
What this voice would never say. Patterns to avoid in future content.

## Voice rules (5)
Numbered, actionable. A writer should be able to follow these without reading the rest of the doc.

1. ...
2. ...
3. ...
4. ...
5. ...

## Calibration sample
Write 1 paragraph in this voice on any topic. Used as a reference for future generations.
```

## How to read the samples

Look for:

- **Recurring sentence shapes.** Does every piece open with a stat? A question? A scene?
- **Word choice tells.** Contractions vs formal. Industry jargon vs plain English. Hedges ("kinda," "probably") vs absolutes.
- **Punctuation tics.** Em dashes? Parens? Lots of one-line paragraphs?
- **What's NOT there.** No bullet lists? No exclamation marks? No "we"? Absence is voice too.

## Verification

After writing the file, ask: "Want me to draft one piece of content using this profile so we can pressure-test it?" If yes, write 100-150 words on a topic the user provides, in the voice. Check it back against the rules.

## Takeaway

A voice file isn't a style guide. It's a pattern recognition document. The job is to make the brand's existing voice repeatable, not to invent a new one.
