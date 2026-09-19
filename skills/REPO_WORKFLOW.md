# Skill: Repository Workflow

Use this workflow whenever working on one of my GitHub-backed projects.

## 1. Orient

Before changing anything:

- Confirm the canonical repository.
- Read its `START_HERE.md`.
- Read `.agent/STATE.md`.
- Read `.agent/HANDOFF.md` if continuation context matters.
- Read `.agent/DECISIONS.md` only as needed for architectural/product constraints.
- Inspect current Git/repository state.

## 2. Scope narrowly

Do not load the whole repository unless genuinely necessary.

Start with:

- files named by the user
- files linked from `START_HERE.md`
- files changed in recent relevant commits
- direct dependencies/imports of the target code
- tests covering the affected behavior

Expand only when evidence requires it.

## 3. Preserve current work

Before edits:

- check whether the behavior has already been changed
- avoid reverting unrelated changes
- do not replace current code with an older version from chat
- retain established naming, structure, configuration, and tests unless the task requires changing them

When unsure, prefer a minimal patch over a rewrite.

## 4. Make changes

For implementation tasks:

- make the smallest coherent change
- update or add tests when appropriate
- preserve backward compatibility unless explicitly changing it
- document non-obvious behavior close to the code

For non-code projects, apply the same principles to documents/configuration/data.

## 5. Persist state

After meaningful progress, update `.agent/STATE.md`.

Record a decision in `.agent/DECISIONS.md` when it is durable and would matter to a future agent, for example:

- architecture
- data model
- compatibility constraint
- naming convention
- rejected approach with an important reason
- product behavior that should not be re-litigated casually

Update `.agent/HANDOFF.md` when work is incomplete or another agent/session is likely to continue.

## 6. Finish with repository truth

A completed task should leave Git describing reality.

The final state should make it possible for a new agent to continue by reading:

1. `START_HERE.md`
2. `.agent/STATE.md`
3. `.agent/HANDOFF.md`
4. relevant source/test files

Do not require chat history to understand the current project state.
