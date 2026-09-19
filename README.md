# agent-skills

A tiny GitHub-backed bootstrap repo for AI coding/work agents.

The goal is simple: **Git is the source of truth; chat memory is not.**

## What this repo contains

- `CHATGPT_START_HERE.md` — the first file every agent should read.
- `PROJECTS.md` — maps project names to their repositories.
- `skills/REPO_WORKFLOW.md` — reusable operating rules for working safely in a repo.
- `templates/project/` — copy these files into each project repository.
- `CUSTOM_INSTRUCTIONS.txt` — small instruction block you can paste into ChatGPT Custom Instructions.

## First-time setup

1. Create a GitHub repository named `agent-skills` (private is fine).
2. Upload the contents of this folder to its default branch.
3. Edit `PROJECTS.md` and add your real project repositories.
4. For each project, copy the contents of `templates/project/` into that project's repository root.
5. Edit that project's `START_HERE.md`.
6. Paste `CUSTOM_INSTRUCTIONS.txt` into ChatGPT Custom Instructions.
7. When available, connect ChatGPT to GitHub so it can read private repositories directly.

Do not duplicate detailed project state in this repo. The project repository itself owns its current state.
