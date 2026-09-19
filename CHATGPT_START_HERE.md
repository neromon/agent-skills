# CHATGPT_START_HERE

This repository is the bootstrap directory for my AI-assisted work.

## Core rule

**Live repository state is authoritative.**

Do not rely on remembered chat context when it conflicts with, predates, or is not confirmed by the current GitHub repository. Prior conversation context may be used only as a hint until verified against the repository.

## Start every project task this way

1. Identify the project being discussed.
2. Open `PROJECTS.md` in this repository and find the project's canonical repository.
3. Inspect the target repository's current Git state before proposing or making edits:
   - default/current branch
   - latest relevant commits
   - open working changes, PRs, or branches if visible
   - files related to the requested task
4. Read the target project's `START_HERE.md`.
5. Then read, in this order when relevant:
   - `.agent/STATE.md`
   - `.agent/HANDOFF.md`
   - `.agent/DECISIONS.md`
6. Read `skills/REPO_WORKFLOW.md` from this bootstrap repo.
7. Read only the additional files needed for the task. Do **not** ingest the entire repository by default.

## Editing rules

Before editing:

- Preserve existing work.
- Do not overwrite newer repository state with remembered chat state.
- Check whether the requested work already exists.
- Prefer small, reviewable changes.
- Follow project-specific instructions in `START_HERE.md`.
- If repository state and chat instructions conflict, flag the conflict and use repository state unless I explicitly tell you to replace it.

After meaningful work:

- Update `.agent/STATE.md`.
- Record durable architectural/product decisions in `.agent/DECISIONS.md`.
- Update `.agent/HANDOFF.md` when another session or agent may need to continue.
- Keep these files concise and factual.
- Commit or prepare changes together with the implementation when repository write access is available.

## Source-of-truth order

Use this precedence:

1. Current files and Git state in the canonical project repository
2. Project `START_HERE.md`
3. `.agent/STATE.md`, `.agent/HANDOFF.md`, `.agent/DECISIONS.md`
4. Reusable instructions in this `agent-skills` repository
5. Current user instructions in this chat
6. Prior chat context or model memory

A newer explicit user instruction may intentionally change the repository; in that case, make the change in Git so the new state becomes authoritative.

## If repository access is unavailable

Do not pretend remembered context is current.

Ask for the repository URL/file, or state exactly which repository information you cannot verify. Continue only with clearly labeled assumptions when useful.
