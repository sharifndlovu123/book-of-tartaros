# The Tartaros Cycle — Workspace

This is a book being written with Claude Code — Anthropic's CLI coding agent, repurposed here as a long-running collaborator for prose, worldbuilding, and continuity across sessions. The repo itself is the collaboration: `CLAUDE.md` gives Claude the standing context for the project, the bible and reference files are what it reads before touching any scene, and git history is the edit trail.

This folder is the canonical workspace for **the Tartaros Cycle**, a science-fiction **tetralogy**. The bible and the questions document are the source of truth; everything else is drafting and reference.

## Folder layout

```
tartaros_workspace/
├── README.md                    (this file)
├── CLAUDE.md                    (project brief for Claude Code)
├── .gitignore                   (git ignores: build artifacts, drafts/scratch)
├── tartaros.code-workspace      (VS Code multi-root workspace config)
│
├── bible/                       ← THE SOURCE OF TRUTH
│   ├── TARTAROS_CYCLE_BIBLE.md           (canonical worldbuilding, characters, structure)
│   ├── TARTAROS_QUESTIONS.md             (character question tracker — closed)
│   ├── DIALOGUE_STYLE.md                 (voice cards + dialogue mechanics)
│   └── TARTAROS_CHARACTER_DEVELOPMENT.md (organizational tree)
│
├── book_one/                    ← The Warden of Tartaros (COMPLETE)
│   ├── chapters/                (individual chapter markdown files, ch1–ch11)
│   ├── full/                    (consolidated full-book file)
│   └── covers/                  (SVG covers, front and back)
│
├── book_two/                    ← The Quiet Flag (the gap book) — designed, not drafted
│   ├── notes/                   (GAP_BOOK_DESIGN.md and other plotting notes)
│   ├── drafts/                  (chapter drafts as they are written)
│   └── covers/
│
├── book_three/                  ← The Ward of Korya — not drafted
│   ├── notes/                   (STARTING_NOTES.md, pending re-scope)
│   ├── drafts/
│   └── covers/
│
├── book_four/                   ← The Empty Chair — not drafted
│   ├── notes/                   (LOCKED_BEATS.md)
│   └── covers/
│
└── reference/                   ← quick-orientation and support material
    ├── CHARACTER_MAP.md         (who's who, family trees)
    ├── geography.md             (the authoritative map)
    └── sigils.html              (faction/house sigils and colour palette)
```

## The canonical files

Two files matter above everything else:

**`bible/TARTAROS_CYCLE_BIBLE.md`** — the cycle bible. Currently at revision 0.29, ~1,280 lines. Nine parts covering the world, characters, geography, timeline, family trees, social texture, and the cycle's ethical spine. Update this every time a meaningful decision is made.

**`bible/TARTAROS_QUESTIONS.md`** — the character-development question tracker. **Fully closed: 222/222 answered.** Many late answers are tagged `[Author-decided, pending review]` — treat those as provisional canon until confirmed.

For faster orientation than the full bible, see `bible/TRILOGY_SYNOPSIS.md` (what happens across all four books and how it ends, with a locked "never alter" list — filename kept for stability even though the work is now a tetralogy) and the `reference/` files above.

These files are the cycle's memory. Any future writing session, with or without Claude, should start by re-reading them.

## Working with Claude across sessions

`CLAUDE.md` in the repo root is read automatically by Claude Code at the start of every session in this folder — it points Claude at the bible, the current state of each book, and the workflow rules below, so there is no need to manually paste context in that case.

For claude.ai (no repo access) or any other assistant, you have two patterns available:

### Pattern A — Paste the bible into a new chat
1. Open `bible/TARTAROS_CYCLE_BIBLE.md` in VS Code
2. Copy the whole file (Cmd+A, Cmd+C / Ctrl+A, Ctrl+C)
3. Paste it as the first message of a new conversation, with a brief instruction such as:
   > This is the canonical bible for the Tartaros Cycle. Please read it before responding. Then I will give you the task.
4. After Claude confirms, give the next task (e.g. "draft chapter one of book two", "review the bible for inconsistencies").

This is the simplest pattern. Claude reads the bible fresh each session, you stay in control of context.

### Pattern B — Attach the file
On claude.ai, attach the markdown file directly. Click the attachment icon, choose `TARTAROS_CYCLE_BIBLE.md`, and ask the task. This is slightly cleaner than pasting and avoids the file-too-long warning for very long bibles.

For either pattern: include both the bible and the questions document when you want comprehensive continuity. Include just the bible when you are working on a specific scene that does not need the question tracker.

## Workflow recommendations

1. **Edit the bible directly.** When a decision is made (a name, a character detail, a plot beat), update the bible immediately. The longer you wait, the more likely the decision will be forgotten.

2. **Commit often.** After any meaningful change, commit to git with a short message describing what changed. This builds an edit history that lets you go back to any earlier version.

3. **Use branches for experiments.** If you want to try a different version of a chapter, character, or plot beat, create a branch. If the experiment works, merge it. If it doesn't, switch back to main.

4. **Keep the bible's revision number current.** When you make a substantial change, bump the revision (e.g. 0.28 → 0.29) and update the footer description.

5. **The questions document is closed but not immutable.** If new questions arise during drafting, add them to the tracker rather than leaving the decision undocumented. Keep the bible and the tracker in sync.

## Setup steps

See `SETUP.md` for detailed setup instructions for git, VS Code, and the recommended extensions.

## Current state of the work

- **Book one** — *The Warden of Tartaros*: complete, 11 chapters, ~52,600 words. Cover and back cover SVGs included.
- **Book two** — *The Quiet Flag* (the gap book): not drafted, but designed — see `book_two/notes/GAP_BOOK_DESIGN.md`. Dramatizes the two-year custody→Korya gap. Parked: the escape mechanism, and whether Kester tells Sable.
- **Book three** — *The Ward of Korya*: not drafted — see `book_three/notes/STARTING_NOTES.md` (predates the gap-book split; pending re-scope).
- **Book four** — *The Empty Chair*: not drafted. Substantial beats locked — see `book_four/notes/LOCKED_BEATS.md`.
- **Bible:** revision 0.29, ~1,280 lines, nine parts. The four arms of the Homonoia, the Synedrion's nine seats, the Vendine institutional ethic, the Keris bloodline, the Adjudicate as the lost fifth arm, and the apex figures are all developed.
- **Questions:** fully closed, 222/222 answered. Many late answers tagged `[Author-decided, pending review]`.

## Cycle structural ironies — the things that make this work

These are the load-bearing ironies the cycle rests on. Preserve them as you continue:

1. The Cleanse is built by Xerxes partly in response to his wife and child dying of black death — which the Keris engineered and withhold the cure for. Xerxes does not know this.
2. Xerxes is preparing for a Keris return that he himself caused by manufacturing the discrediting evidence two centuries ago. He does not know this either.
3. The Synedrion has nine chairs; the Keris chair has been empty for 200 years because the seat was never legally reassigned. The empty chair is the legal mechanism of the Keris's reinstatement when they return.
4. Mother Hessa's patience is not innocent — she chose for decades not to confirm what she suspected because confirming would damage the Vendine she loves.
5. The Adjudicate (the Keris's lost fifth arm) is restored at the cycle's end; the Architect role becomes structurally redundant. The cycle ends with institutional restoration, not just exposure.
6. Marcus mirrors Bastien's withdrawal back at him at the cascade — *you wanted space; now Marcus wants space*.

These are the cycle. Everything else is texture.
