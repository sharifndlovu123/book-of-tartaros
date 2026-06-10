# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this project is

The workspace for **the Tartaros Cycle**, a science-fiction trilogy by Sharif. Book one (*The Warden of Tartaros*) is complete at ~52,600 words across 11 chapters. Book two is unstarted. This is a writing project — the deliverables are markdown prose files. There is no build system, no tests, no application.

## Source of truth — read before acting on any substantive task

Two files are the canonical source of truth for everything in the trilogy:

1. **`bible/TARTAROS_CYCLE_BIBLE.md`** — worldbuilding, characters, geography, timeline, family trees, institutional structure. Revision 0.17, ~1,022 lines, nine parts. Do not write or edit trilogy content without reading this first.
2. **`bible/TARTAROS_QUESTIONS.md`** — character development question tracker: 152 answered, 14 partial, 56 open. Read when resolving character detail.

If a task is purely mechanical (rename a file, fix a typo), the bible is optional. For anything touching plot, character, worldbuilding, or voice — read the bible first.

## The trilogy's load-bearing ironies

Do not contradict these. If new work seems to, flag it and ask before proceeding.

1. The Cleanse is built partly in response to Xerxes's wife and child dying of black death — which the Keris engineered and withhold the cure for. Xerxes does not know this.
2. Xerxes is preparing for a Keris return that he caused by manufacturing the discrediting evidence two centuries ago. He does not know this either.
3. The Synedrion has nine chairs; the Keris chair has been empty 200 years because the seat was never legally reassigned. The empty chair is the legal mechanism of reinstatement.
4. Mother Hessa's patience is not innocent — she chose for decades not to confirm what she suspected because confirming would damage the Vendine she loves.
5. The Adjudicate (the Keris's lost fifth arm) is restored at the trilogy's end; the Architect role becomes structurally redundant. The trilogy ends with institutional restoration, not just exposure.
6. Marcus mirrors Bastien's withdrawal back at him at the cascade — *you wanted space; now Marcus wants space*.

## Prose voice

Interior, slightly cool, attentive to institutional textures and character interiority. Avoid melodrama. Hold complications open rather than resolving them too cleanly. Do not reach for heroic gestures, assassin-daughter tropes, or neat redemption arcs — the bible documents the harder, truer choices.

**Naming registers:**
- Latinate-Greek: senior aristocracy and institutional figures (Bastien, Aemilius, Aurelius, Quintus, Marcus)
- Persian/pre-Hegemony: figures outside the aristocratic stratum (Xerxes, Cyrus, Soraya)
- Norman-French: Vendine houses (Orrel, Aldric, Roderic, Mireille)
- Slavic-leaning: the Keris (Imir, Kazimir, Milana, Ivana)
- Plainer Anglo-Norman: serving families (Beatrice Carnay)

**Honorifics:** Summum (the Architect), Dux (arm directors — Dux Vren for Marella), Mother/Sister (Sisters of the Long Patience), Mistress (older Healer tradition), Professor (medical academic), Director (medical arm head).

## Current state of the work

- **Bible**: revision 0.17.
- **Book one**: complete, 11 chapters, `book_one/chapters/`, consolidated at `book_one/full/`.
- **Book two**: not drafted. Four structural decisions are still open — see `book_two/notes/STARTING_NOTES.md`. These are the user's to decide; propose options, do not pick.
- **Book three**: not drafted. Substantial beats locked — see `book_three/notes/LOCKED_BEATS.md`.
- **Questions**: 152 answered, 14 partial, 56 open. Mostly Round Seven (Lira's family, Marella's daughter) and remaining names (homeworlds, Aurelius and Veliya surnames, Mireille's surname).

## Workflow principles

1. **The bible is the source of truth.** If the bible is silent on a detail, propose it explicitly and mark it `[TBD]` or `[Author-decided, pending review]`.
2. **Update the bible when decisions are made.** If a session resolves a question, update both `bible/TARTAROS_CYCLE_BIBLE.md` and `bible/TARTAROS_QUESTIONS.md`. Bump the revision number (0.17 → 0.18) and update the footer description.
3. **Suggest a commit after meaningful changes.** Git history is the trilogy's edit memory.

## Closing open questions — the Q&A process

There is an agreed workflow for working through the open/partial questions in
`bible/TARTAROS_QUESTIONS.md`. **Read `QA_PROCESS.md` before running a Q&A
session.** In short:

- The user answers in `open_questions.html` (a self-contained page listing all
  open/partial questions by collective, each with a "ripples" panel showing what
  the answer affects), clicks **Copy answers**, and pastes the block into chat.
- Each answer arrives tagged with an **ID** like `R7-C25-Q5` (Round 7,
  Character 25, Question 5) so both sides agree on what is being answered.
- For each answer: give feedback (fit with bible, effect on load-bearing
  ironies), ask follow-ups only where a real new decision opens, and propose
  gap-fills (marked `[Author-decided, pending review]`) only where the user
  leaves a blank or says "you decide".
- Write settled answers back into **both** the questions document and the bible;
  bump the revision; suggest a commit.
- **Book-two blockers come first** (`R8-4`, `R8-7`, `R8-3`, `R7-C25-Q5`).

If the question set in `bible/TARTAROS_QUESTIONS.md` changes, regenerate the
question data in `open_questions.html` to match.

## Common task patterns

**"Help me draft chapter X of book two."**
1. Read the bible (at least Part II for characters, Part III for geography, Part IX for ethical spine).
2. Read `book_two/notes/STARTING_NOTES.md` for open structural questions.
3. Read any existing drafts in `book_two/drafts/`.
4. Confirm the chapter's plot beats before drafting.

**"Update the bible with this new decision."**
1. Read the relevant section of the bible.
2. Make the edit; mark new content `[CONFIRMED]` or `[Author-decided]`.
3. Update the footer revision number and description.
4. Update the questions document if a question is now answered. Suggest a commit.

**"Review the bible for inconsistencies."**
1. Read the whole bible.
2. Flag specific contradictions with file locations.
3. Propose resolutions but do not edit without user confirmation.

## Useful searches

```bash
grep -n "^## PART" bible/TARTAROS_CYCLE_BIBLE.md      # list all Parts
grep -n "^### " bible/TARTAROS_CYCLE_BIBLE.md          # list all character entries
grep -n "\[TBD\]" bible/TARTAROS_CYCLE_BIBLE.md        # find open items in the bible
grep -n "OPEN" bible/TARTAROS_QUESTIONS.md             # find unanswered questions
```

## Next priorities (when user says "continue where we left off")

1. Resolve the four structural decisions blocking book two (`book_two/notes/STARTING_NOTES.md`).
2. Close out Round Seven of the questions document (Lira's family, Marella's daughter).
3. Settle remaining names (homeworlds, Aurelius and Veliya surnames, Mireille's surname).
4. Begin drafting book two chapter one once structural decisions are made.
