# The Tartaros Cycle — Workspace

This folder is the canonical workspace for the trilogy. The bible and the questions document are the source of truth; everything else is drafting and reference.

## Folder layout

```
tartaros_workspace/
├── README.md                    (this file)
├── .gitignore                   (git ignores: build artifacts, drafts/scratch)
├── tartaros.code-workspace      (VS Code multi-root workspace config)
│
├── bible/                       ← THE SOURCE OF TRUTH
│   ├── TARTAROS_CYCLE_BIBLE.md           (canonical worldbuilding, characters, structure)
│   ├── TARTAROS_QUESTIONS.md             (character question tracker)
│   └── TARTAROS_CHARACTER_DEVELOPMENT.md (organizational tree)
│
├── book_one/                    ← The Warden of Tartaros (COMPLETE)
│   ├── chapters/                (individual chapter markdown files, ch1–ch11)
│   ├── full/                    (consolidated full-book file)
│   └── covers/                  (SVG covers, front and back)
│
├── book_two/                    ← work in progress
│   ├── notes/                   (plotting notes, scene cards, character beats)
│   └── drafts/                  (chapter drafts as they are written)
│
├── book_three/                  ← future work
│   └── notes/
│
└── reference/                   ← architecture diagrams, family trees, etc.
```

## The canonical files

Two files matter above everything else:

**`bible/TARTAROS_CYCLE_BIBLE.md`** — the trilogy bible. Currently at revision 0.17. Nine parts covering the world, characters, geography, timeline, family trees, social texture, decisions pending, draft-two tasks for book one, and the trilogy's ethical spine. Update this every time a meaningful decision is made.

**`bible/TARTAROS_QUESTIONS.md`** — the character-development question tracker. 152 questions answered, 14 partial, 56 open. Update when a question is resolved.

These two files are the trilogy's memory. Any future writing session, with or without Claude, should start by re-reading them.

## Working with Claude across sessions

You have two patterns available:

### Pattern A — Paste the bible into a new chat
When you start a new conversation with Claude and want continuity:
1. Open `bible/TARTAROS_CYCLE_BIBLE.md` in VS Code
2. Copy the whole file (Cmd+A, Cmd+C / Ctrl+A, Ctrl+C)
3. Paste it as the first message of a new conversation, with a brief instruction such as:
   > This is the canonical bible for the Tartaros Cycle. Please read it before responding. Then I will give you the task.
4. After Claude confirms, give the next task (e.g. "draft chapter one of book two", "answer the remaining Round Seven questions", "review the bible for inconsistencies").

This is the simplest pattern. Claude reads the bible fresh each session, you stay in control of context.

### Pattern B — Attach the file
On claude.ai, you can attach the markdown file directly. Click the attachment icon, choose `TARTAROS_CYCLE_BIBLE.md`, and ask the task. Claude reads the file from the attachment. This is slightly cleaner than pasting and avoids the file-too-long warning for very long bibles.

For either pattern: include both the bible and the questions document when you want comprehensive continuity. Include just the bible when you are working on a specific scene that does not need the question tracker.

## Workflow recommendations

1. **Edit the bible directly in VS Code.** When you make a decision (a name, a character detail, a plot beat), update the bible immediately. The longer you wait, the more likely the decision will be forgotten.

2. **Commit often.** After any meaningful change, commit to git with a short message describing what changed. This builds an edit history that lets you go back to any earlier version.

3. **Use branches for experiments.** If you want to try a different version of a chapter, character, or plot beat, create a branch. If the experiment works, merge it. If it doesn't, switch back to main.

4. **Keep the bible's revision number current.** When you make a substantial change, bump the revision (0.17 → 0.18) and update the footer description.

5. **The questions document is for unanswered questions.** When a question is resolved in the bible, update its status in the questions document to ANSWERED. Keep the two files in sync.

## Setup steps

See `SETUP.md` for detailed setup instructions for git, VS Code, and the recommended extensions.

## Current state of the work

- **Book one:** complete, 11 chapters, ~52,600 words. Cover and back cover SVGs included.
- **Bible:** revision 0.17, ~1,022 lines. The four arms of the Homonoia, the Synedrion's nine seats, the Vendine institutional ethic, the Keris bloodline, the Adjudicate as the lost fifth arm, House Orrel family detail, House Aemilius detail, the apex four (Xerxes, Marella, Bastien, Aelia), and the Synedrion seat-holders are all developed. About thirty named characters with full profiles.
- **Questions:** 152 answered, 14 partial, 56 open. The open items are mostly Round Seven (Lira's family, Marella's daughter), Round Four characters 13-15 (Roan boss, Asham, Ivana), the young woman Hessa placed with Cassian, and remaining names (homeworlds, several surnames).
- **Book two:** not yet drafted. The bible is substantially complete enough to begin drafting.

## Trilogy structural ironies — the things that make this work

These are the load-bearing ironies the trilogy rests on. Preserve them as you continue:

1. The Cleanse is built by Xerxes partly in response to his wife and child dying of black death — which the Keris engineered generations ago and withhold the cure for.
2. Xerxes is preparing for a Keris return that he himself caused by manufacturing the discrediting evidence two centuries ago.
3. The Synedrion has nine chairs; the Keris chair has been empty for 200 years because the seat was never legally reassigned. The empty chair becomes the legal mechanism of the Keris's reinstatement when they return.
4. Mother Hessa's patience is not innocent — she chose for decades not to confirm what she suspected because confirming would damage the Vendine she loves.
5. The Adjudicate (the Keris's lost fifth arm) is restored at the trilogy's end; the Architect role becomes structurally redundant. The trilogy ends with institutional restoration, not just exposure.
6. Marcus mirrors Bastien's withdrawal back at him at the cascade — *you wanted space; now Marcus wants space*.

These are the trilogy. Everything else is texture.
