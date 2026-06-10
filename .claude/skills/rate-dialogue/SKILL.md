---
name: rate-dialogue
description: Score a passage of Tartaros Cycle dialogue against bible/DIALOGUE_STYLE.md — rates idiolect, POV-colored narration, subtext, wit/vulnerability, mechanics, and voice-card fidelity, then gives specific line-level fixes and one rewritten beat. Use when asked to rate, score, critique, or pressure-test dialogue or a scene's voices.
---

# Rate Dialogue

Rigorously score a passage of Tartaros Cycle dialogue against the trilogy's
dialogue style, and return concrete fixes — never vague praise.

## Inputs

The passage to rate comes from the user's invocation: an inline paste, a file
path (optionally with a line range, e.g. `book_one/chapters/...ch5.md:74-120`), or
"the scene we just discussed." If none is given, ask which passage.

## Procedure

1. **Read the rubric and the cast.** Read `bible/DIALOGUE_STYLE.md` in full —
   especially the voice cards. Read the passage.
2. **Identify the POV** of the passage (whose close-third head are we in?) and
   which carded characters speak.
3. **Run the cover-the-tags test.** Mentally strip every "X said." Can you still
   attribute each line? Note any line that could belong to two characters.
4. **Score each dimension 1–5** (anchors below), quoting specific evidence from
   the passage for every score. Be honest; a 5 is rare.
5. **Voice-card fidelity.** For each carded character present, check the lines
   against their card (register, rhythm, tics, *what they refuse to say*, humor,
   signature). Flag any drift — a line the character wouldn't say, or a generic
   line where the card promises a distinctive one.
6. **Output** in the format below.

## The six dimensions (score each /5)

1. **Voice distinctness (cover-the-tags).** Can speakers be told apart with tags
   removed? *5:* every voice unmistakable. *3:* principals distinct, some
   interchangeable. *1:* everyone sounds the same.
2. **Idiolect depth.** Do voices use diction/rhythm/tics/refusals from their
   cards, not a default voice? Minor functional characters may stay plain — judge
   the principals.
3. **POV-colored narration.** Does the prose between lines take the POV
   character's diction, bias, and blind spots? *5:* the narration could belong to
   no other POV. *1:* neutral, camera-like narration.
4. **Subtext / not-info-dump.** Do people say less than they mean, and does
   information arrive *through* character action rather than as a lecture? Penalize
   uninterrupted expository monologues even when well-voiced.
5. **Wit & vulnerability.** Is there armor (dry, dark, sparing humor) and/or a
   rationed crack where control slips? Penalize melodrama and on-the-nose emotion.
6. **Mechanics.** Beats over "said"; no adverb-tags; italics for emphasis/internal;
   em-dash interrupt vs. ellipsis trail; no phonetic dialect; the
   declarative-question device used only by the cold/controlled cards.

## Output format

```
POV: <character> · Carded speakers: <list>

SCORECARD
  Voice distinctness     X/5 — <one line + quoted evidence>
  Idiolect depth         X/5 — <...>
  POV-colored narration  X/5 — <...>
  Subtext / not-info-dump X/5 — <...>
  Wit & vulnerability    X/5 — <...>
  Mechanics              X/5 — <...>
  OVERALL                X.X/5

VOICE-CARD FIDELITY
  <character>: match / drift — <evidence; if drift, the card line it violates>

TOP FIXES (most leverage first)
  1. <specific, line-level fix>
  2. ...
  3. ...

REWRITE — the weakest beat
  <quote the original beat, then a rewrite applying the fixes>
```

## Rules

- **Evidence or it doesn't count.** Every score cites a line from the passage.
- **No vague praise.** "Good dialogue" is not a finding; name the technique.
- **Respect the author.** The goal is uplift, not a takedown — but be candid about
  weak spots; that is the point of the score.
- **Don't invent canon.** If a character has no voice card, say so and rate by the
  general principles; suggest adding a card if they recur.
