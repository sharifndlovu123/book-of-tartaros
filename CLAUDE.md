# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this project is

The workspace for **the Tartaros Cycle**, a science-fiction **tetralogy** by Sharif. Book one (*The Warden of Tartaros*) is complete at ~52,600 words across 11 chapters. Book two (*The Quiet Flag* — the gap book), book three (*The Ward of Korya*), and book four (*The Empty Chair*) are undrafted. This is a writing project — the deliverables are markdown prose files. There is no build system, no tests, no application.

## Source of truth — read before acting on any substantive task

Two files are the canonical source of truth for everything in the cycle:

1. **`bible/TARTAROS_CYCLE_BIBLE.md`** — worldbuilding, characters, geography, timeline, family trees, institutional structure. Revision 0.28, ~1,260 lines, nine parts. Do not write or edit cycle content without reading this first.
2. **`bible/TARTAROS_QUESTIONS.md`** — character development question tracker: **fully closed (222/222 answered)**. Read when resolving character detail.

If a task is purely mechanical (rename a file, fix a typo), the bible is optional. For anything touching plot, character, worldbuilding, or voice — read the bible first.

**For quick orientation** (faster than the full bible):
- **`bible/TRILOGY_SYNOPSIS.md`** — what happens across books 1–4 and how it ends, with a `LOCKED` / "never alter" list. Read this before any plot work to avoid contradicting the ending. *(Filename keeps "TRILOGY" for stability; the work is now a tetralogy.)*
- **`reference/CHARACTER_MAP.md`** — who's who, grouped by house/faction, with family trees (Mermaid diagrams).
- **`reference/geography.md`** — the authoritative map: the five-world core (Andra Prime, Tartaros, Verdaine, Elysse, Korya), the carceral system (Tartaros = prison + the Harvester enclave + the Undersiders beneath), the Federation, and trade/currency. Read before any worldbuilding or geography work.
- **`reference/sigils.html`** — a device (sigil) and colour palette for every faction, house, arm, Synedrion seat, the Keris, and the Roan. Colours for the four arms / Sisters / Keris are bible-locked; sigils and the other palettes are proposals (tagged in the page).

## The cycle's load-bearing ironies

Do not contradict these. If new work seems to, flag it and ask before proceeding.

1. The Cleanse is built partly in response to Xerxes's wife and child dying of black death — which the Keris engineered and withhold the cure for. Xerxes does not know this.
2. Xerxes is preparing for a Keris return that he caused by manufacturing the discrediting evidence two centuries ago. He does not know this either.
3. The Synedrion has nine chairs; the Keris chair has been empty 200 years because the seat was never legally reassigned. The empty chair is the legal mechanism of reinstatement.
4. Mother Hessa's patience is not innocent — she chose for decades not to confirm what she suspected because confirming would damage the Vendine she loves.
5. The Adjudicate (the Keris's lost fifth arm) is restored at the cycle's end; the Architect role becomes structurally redundant. The cycle ends with institutional restoration, not just exposure.
6. Marcus mirrors Bastien's withdrawal back at him at the cascade — *you wanted space; now Marcus wants space*.

## Prose voice

Interior, slightly cool, attentive to institutional textures and character interiority. Avoid melodrama. Hold complications open rather than resolving them too cleanly. Do not reach for heroic gestures, assassin-daughter tropes, or neat redemption arcs — the bible documents the harder, truer choices.

**Dialogue:** follow **`bible/DIALOGUE_STYLE.md`** before drafting or revising any scene with people in it. It anchors on the Martin model (class/culture-marked idiolect, POV-colored close-third narration, wit-as-armor) with a no-phonetic-spelling rule, and includes per-character **voice cards** — the ten principal voices in full (Xerxes, Marella, Bastien, Quintus, Sable, Kester, Hessa, Cassian, Kazimir, Roan), plus condensed cards for the wider cast (Orrel/Aemilius/Caradec Vendine, the Asclepi & Limine figures, the Synedrion, the Keris, the resistance) — with mechanics and before/after examples. The cover-the-tags test: if you can't tell who's speaking with the tags removed, the line is wrong.

**Naming registers:**
- Latinate-Greek: senior aristocracy and institutional figures (Bastien, Aemilius, Aurelius, Quintus, Marcus)
- Persian/pre-Hegemony: figures outside the aristocratic stratum (Xerxes, Cyrus, Soraya)
- Norman-French: Vendine houses (Orrel, Aldric, Roderic, Mireille)
- Slavic-leaning: the Keris (Imir, Kazimir, Milana, Ivana)
- Plainer Anglo-Norman: serving families (Beatrice Carnay)

**Honorifics:** Summum (the Architect), Dux (arm directors — Dux Vren for Marella), Mother/Sister (Sisters of the Long Patience), Mistress (older Healer tradition), Professor (medical academic), Director (medical arm head).

## Current state of the work

- **Bible**: revision 0.28.
- **Book one** — *The Warden of Tartaros*: complete, 11 chapters, `book_one/chapters/`, consolidated at `book_one/full/`.
- **Book two** — *The Quiet Flag* (the gap book): not drafted, but **designed** — see `book_two/notes/GAP_BOOK_DESIGN.md`. Dramatizes the two-year custody→Korya gap. Parked: the escape mechanism, and whether Kester tells Sable.
- **Book three** — *The Ward of Korya*: not drafted — see `book_three/notes/STARTING_NOTES.md` (predates the gap-book split; pending re-scope).
- **Book four** — *The Empty Chair*: not drafted. Substantial beats locked — see `book_four/notes/LOCKED_BEATS.md`.
- **Questions**: fully closed (222/222 answered); many late answers tagged `[Author-decided, pending review]`.

## Workflow principles

1. **The bible is the source of truth.** If the bible is silent on a detail, propose it explicitly and mark it `[TBD]` or `[Author-decided, pending review]`.
2. **Update the bible when decisions are made.** If a session resolves a question, update both `bible/TARTAROS_CYCLE_BIBLE.md` and `bible/TARTAROS_QUESTIONS.md`. Bump the revision number (e.g., 0.28 → 0.29) and update the footer description.
3. **Suggest a commit after meaningful changes.** Git history is the cycle's edit memory.

## Question tracker — closed

The character-question tracker (`bible/TARTAROS_QUESTIONS.md`) is **fully closed
(222/222 answered)**. The interactive answering tool (`open_questions.html`) has
been retired. The repeatable method is preserved in `QA_PROCESS.md`; if new
questions arise during drafting, add them to the tracker and regenerate a page
from that method.

Many late answers are tagged `[Author-decided, pending review]` in the bible —
treat those as provisional canon until the author confirms. When writing back any
new decision, update **both** the bible and the questions tracker, bump the bible
revision, and keep `reference/CHARACTER_MAP.md`, `bible/TRILOGY_SYNOPSIS.md`, and
`reference/sigils.html` in sync.

## Common task patterns

**"Help me draft chapter X of book two (*The Quiet Flag*, the gap book)."**
1. Read the bible (at least Part II for characters, Part III + `reference/geography.md` for geography, Part IX for ethical spine).
2. Read `book_two/notes/GAP_BOOK_DESIGN.md` for the structure (M1–M4), knowledge map, setting (Scupper), and cast.
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

1. Formalize the gap book (*The Quiet Flag*) into the bible — redistribute Thread B's early movements (search → false grief, crushed exposure → archive, the discovery, the wreck) from book three into book two (Part I §8–10), per `book_two/notes/GAP_BOOK_DESIGN.md`.
2. Resolve book two's parked decisions: the escape mechanism (M1), and whether Kester tells Sable (the M4 hinge).
3. Re-scope `book_three/notes/STARTING_NOTES.md` (*The Ward of Korya*) now that the gap material lives in book two.
4. Begin drafting book two (*The Quiet Flag*) chapter one once the formalization and parked decisions are settled.
