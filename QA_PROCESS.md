# The Q&A Process — closing the open character questions

> **Status (2026-06-10): COMPLETE.** The question tracker is fully closed
> (222/222 answered) and the interactive tool `open_questions.html` has been
> retired. This document is kept as the *method*: if new questions arise during
> drafting, add them to `bible/TARTAROS_QUESTIONS.md` and regenerate a page from
> the steps below.

This document describes how Sharif and Claude work through the open questions in
`bible/TARTAROS_QUESTIONS.md`. It is the agreed, repeatable workflow.

## The two artifacts

1. **`open_questions.html`** — a single self-contained web page (no server, no
   install). Double-click it to open in a browser. It contains:
   - a **houses & factions overview** at the very top — every house, arm, order,
     and faction with a brief of its people's stance, beliefs, and visual
     register, so the world's commitments stay in view while answering,
   - every **open** and **partial** question, grouped by *collective* (the
     Rounds in the questions document),
   - a **character brief** above each character's questions — who they are,
     their house, and their personality/trait/stance,
   - an answer box under each question,
   - a **ripples panel** showing what answering that question affects
     (downstream characters, plot threads, the four book-two blocking
     decisions, and the trilogy's load-bearing ironies),
   - autosave to the browser (closing the tab loses nothing),
   - a **Copy answers** button that copies *all* questions answered so far.

   The houses overview, character briefs, and ripple notes are summarized from
   the bible (revision 0.17). If the bible changes materially, refresh the
   `FACTIONS`, `BRIEFS`, and `DATA` blocks in the HTML to match.

2. **`bible/TARTAROS_QUESTIONS.md`** — the canonical tracker. The HTML page is a
   working surface; this file remains the source of truth. Answers only become
   real once written back here (and into the bible).

## The loop

1. **Sharif answers** — open `open_questions.html`, fill in any number of
   questions in any order, across any collectives. Progress autosaves.
2. **Copy** — click **Copy answers**. This copies every answered question as a
   block, each tagged with its **ID** (e.g. `R7-C25-Q5`) and the question text,
   plus a header listing how many answers and which IDs are included. Example:

   ```
   TARTAROS — Q&A SUBMISSION
   3 answers · IDs: R7-C25-Q1, R7-C25-Q5, R8-4

   [R7-C25-Q1] (Round 7 · Lira Vaile) Lira's mother — name
   → Maren Vaile

   [R7-C25-Q5] (Round 7 · Lira Vaile) Lira's politics — ...
   → anti-conglomerate, leans naive
   ...
   ```

3. **Paste into chat** — Sharif pastes the block to Claude.
4. **Claude responds**, per answer:
   - **Feedback** — does the answer fit the bible? Does it strengthen or
     threaten any load-bearing irony? Any consequence Sharif may not have seen?
   - **Follow-up questions** — only where the answer opens a genuine new
     decision (kept minimal; no busywork).
   - **Gap-fills** — where an answer is left blank or says "you decide", Claude
     *may* propose one, marked `[Author-decided, pending review]`, for Sharif to
     accept or reject. Claude never silently invents canon.
5. **Write-back** — once an answer is settled, Claude updates **both**
   `bible/TARTAROS_QUESTIONS.md` (status → `[ANSWERED]` / `[CONFIRMED]`, answer
   noted) **and** the relevant section of `bible/TARTAROS_CYCLE_BIBLE.md`. Bump
   the bible revision number and footer description. Suggest a commit.
6. **Repeat** until a collective is closed.

## Question IDs

IDs encode location so both sides always agree on what is being discussed:

- `R7-C25-Q5` = Round 7, Character 25 (Lira Vaile), Question 5.
- `R8-4` = Round 8 (structural decisions), item 4.
- `R9-7` = Round 9 (visual identity), item 7.

When Claude asks a follow-up, it cites the ID. When Sharif answers, the copied
block carries the ID. Nothing gets matched by guesswork.

## Priority order (when unsure what to answer next)

The four **book-two blockers** come first — these gate drafting entirely (see
`book_two/notes/STARTING_NOTES.md`). They are flagged in red on the page:

1. `R8-4` — Thread B (what the Compact-side cast does for two years).
2. `R8-7` — The Successor (cipher only, or one moment of presence).
3. `R8-3` — Mouse's interiority (POV scene, or pure horror-object).
4. `R7-C25-Q5` — Lira's politics.

After those: Round 7 personal threads, then remaining names (Round 8 item 5,
plus scattered surname TBDs), then Round 9 visual refinements.

## Rules that do not change

- The bible is the source of truth; the HTML is scratch until written back.
- Claude proposes, Sharif decides. Structural decisions are never resolved for
  him — options yes, picks no.
- Answers that fill a gap are marked provisional until Sharif confirms.
- Keep the page and the questions document in sync: an answer is not "done"
  until it is in `bible/TARTAROS_QUESTIONS.md`.
