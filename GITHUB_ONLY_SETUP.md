# GitHub-Only Setup

You do not need a local computer, shell, MCP server, database, or CI system to start.

## Bootstrap repo

Create a GitHub repository named:

`agent-skills`

Upload these files to its default branch:

- `CHATGPT_START_HERE.md`
- `PROJECTS.md`
- `skills/REPO_WORKFLOW.md`

You may also keep this README and the templates in the repo.

## Each project repo

Copy:

- `templates/project/START_HERE.md` -> `/START_HERE.md`
- `templates/project/.agent/STATE.md` -> `/.agent/STATE.md`
- `templates/project/.agent/DECISIONS.md` -> `/.agent/DECISIONS.md`
- `templates/project/.agent/HANDOFF.md` -> `/.agent/HANDOFF.md`

Then customize them and commit them.

## Day-to-day usage

At the start of a new ChatGPT conversation, your Custom Instructions should point ChatGPT to the bootstrap repo.

For a public repo, an agent with web/GitHub access can inspect the live repository.

For a private repo, connect an authenticated GitHub integration in the AI client. Without authenticated access, provide the needed files manually rather than relying on old chat memory.

## Recommended update behavior

After a substantial change, the same PR/commit should ideally include:

- implementation/document changes
- updated tests if relevant
- `.agent/STATE.md`
- `.agent/HANDOFF.md` if unfinished
- `.agent/DECISIONS.md` only when a durable decision was made

This keeps implementation and agent context synchronized.
