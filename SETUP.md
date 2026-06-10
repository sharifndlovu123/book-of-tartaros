# Setup — moving the Tartaros workspace into VS Code

This walks through getting the workspace running locally with git and VS Code. Once it is done, you have a durable, version-controlled writing environment that travels with you.

## Step 1 — Place the workspace folder somewhere durable

Pick a location on your machine for long-term writing projects. On Linux/macOS:

```bash
mv ~/Downloads/tartaros_workspace ~/Documents/
cd ~/Documents/tartaros_workspace
```

On Windows the equivalent would be `C:\Users\<you>\Documents\tartaros_workspace`. Choose a path that is regularly backed up (iCloud Documents, Google Drive Desktop, OneDrive, Dropbox, or a cloud-synced folder of your choice). The trilogy is too valuable to lose to a single disk failure.

## Step 2 — Initialize git

From inside the workspace folder:

```bash
git init
git add .
git commit -m "Initial commit: book one complete, bible revision 0.17"
```

That establishes the workspace as a git repository with the current state as the first commit.

### Optional but recommended: push to GitHub for off-site backup

1. Create a new private repository on GitHub named `tartaros-cycle` (or whatever you prefer)
2. Do not initialize it with a README — your local folder already has one
3. Connect your local repo and push:

```bash
git remote add origin git@github.com:<your-username>/tartaros-cycle.git
git branch -M main
git push -u origin main
```

The repository should be **private**. The trilogy is your work; you control who sees it.

## Step 3 — Install VS Code

If you do not already have it: https://code.visualstudio.com/

Once installed, open the workspace folder:

```bash
code ~/Documents/tartaros_workspace
```

Or use **File → Open Folder** from inside VS Code and navigate to it.

## Step 4 — Install the recommended extensions

Open the Extensions panel (Cmd+Shift+X / Ctrl+Shift+X) and install:

1. **Markdown All in One** (publisher: Yu Zhang)
   - Provides keyboard shortcuts for bold/italic, table-of-contents auto-generation, list management, and a live markdown preview side-by-side with the editor.
   - This is the single most useful extension for writing markdown in VS Code.

2. **Markdown Preview Enhanced** (publisher: Yiyi Wang)
   - Higher-quality preview pane that handles mermaid diagrams, math, and custom themes. Use Cmd+K V / Ctrl+K V to open the preview alongside the editor.

3. **Word Count** (publisher: Microsoft)
   - Adds a word count to the status bar for any markdown file. Useful for tracking chapter length.

4. **Code Spell Checker** (publisher: Street Side Software)
   - Catches typos in markdown files. Add the trilogy's proper nouns (Bastien, Vendine, Aemilius, etc.) to the workspace dictionary as you encounter them and the spell checker stops flagging them.

5. **GitLens** (publisher: GitKraken)
   - Optional but recommended once you are committing regularly. Shows the git history inline, lets you compare versions of any file, and makes the version history feel like a first-class part of the writing process.

Suggested optional:

6. **Markdown Mermaid** (publisher: bierner) — if you want diagrams in markdown files (e.g. a family tree rendered inline in the bible).

## Step 5 — Configure the workspace

Open `tartaros.code-workspace` in VS Code (it is in the workspace root). This file pre-configures the workspace with the right folder layout and editor settings for writing prose. Choose **File → Open Workspace from File** and select it. Going forward, open the workspace via this file rather than the folder directly — that keeps the settings and folder layout consistent.

## Step 6 — Daily writing workflow

Once everything is set up, the workflow is:

1. Open the workspace via `tartaros.code-workspace`
2. Open `bible/TARTAROS_CYCLE_BIBLE.md` in one tab and the chapter you are working on (e.g. `book_two/drafts/chapter_one.md`) in another
3. Write. Save frequently — VS Code auto-saves if you enable `files.autoSave: afterDelay` in settings.
4. When you finish a writing session, commit:
   ```bash
   git add .
   git commit -m "Book two, chapter one: first half"
   ```
5. If you have a GitHub remote configured: `git push`

That is the whole workflow. Open, write, commit, push. Repeat.

## Step 7 — When you want to continue with Claude

See `README.md` for the two patterns (paste the bible, or attach the file). Both work; pick the one that fits the task.

## Troubleshooting

**The bible is too long to paste comfortably.** Use Pattern B (attach the file) on claude.ai. Or, for a focused task, paste only the relevant section (a character profile, a particular Part of the bible) rather than the whole document.

**VS Code is slow on the large bible file.** Disable Markdown All in One's auto-update of the table of contents if it is enabled. Or split the bible into multiple files (one per Part) and keep them in a `bible/parts/` subfolder. The single-file version is easier to share with Claude, so keep one consolidated version even if you split for editing.

**You want to track changes more granularly.** Use git tags to mark significant milestones: `git tag bible-0.17` or `git tag book-one-complete`. Tags make it easy to revisit specific versions later.

**You want to write somewhere other than VS Code occasionally.** Markdown files are plain text; any editor opens them. Obsidian, iA Writer, Typora, Mark Text, or just a text editor all work. The git repo follows you regardless of editor choice.
