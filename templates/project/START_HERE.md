# START_HERE

This is the entry point for AI agents and new contributors working on this project.

## Project

**Name:** <PROJECT NAME>

**Repository:** <CANONICAL GITHUB URL>

**Purpose:**  
<One or two sentences describing what this project does.>

## Source of truth

The live files and Git history in this repository are authoritative.

Do not restore older behavior merely because it appeared in a prior chat. Verify current implementation first.

## Read first

For most tasks, read only:

1. this file
2. `.agent/STATE.md`
3. `.agent/HANDOFF.md` if work is in progress
4. the specific source/config/test files relevant to the task

Consult `.agent/DECISIONS.md` when a task touches an existing architectural or product decision.

## Important paths

- `<path>` — <what it contains>
- `<path>` — <what it contains>
- `<path>` — <what it contains>

Keep this list short. It should route an agent, not describe the whole repository.

## How to verify changes

Use the smallest relevant verification first.

Examples:

- `<test command>`
- `<lint command>`
- `<build command>`
- `<manual verification step>`

If no executable environment is available, inspect the relevant tests/configuration and clearly state what was not executed.

## Project rules

- Preserve unrelated working behavior.
- Prefer targeted edits over broad rewrites.
- Do not delete or rename public interfaces without explicit reason.
- Keep `.agent/STATE.md` current after meaningful changes.
- Record durable decisions in `.agent/DECISIONS.md`.
- Leave a concise `.agent/HANDOFF.md` when work remains.

## Additional project-specific constraints

- <constraint>
- <constraint>
