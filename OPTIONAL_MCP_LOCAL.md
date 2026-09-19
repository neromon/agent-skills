# Optional MCP / Local Execution Upgrade

The repository convention does not change when you add automation later.

## Stage 1 — GitHub integration

Connect an AI client directly to GitHub.

This allows the agent to discover repositories, inspect branches/commits/files, create branches or pull requests, and write changes without you copying files into chat.

Keep the same bootstrap process:

`CHATGPT_START_HERE.md` -> `PROJECTS.md` -> project `START_HERE.md` -> narrow relevant files.

## Stage 2 — GitHub MCP

An MCP-compatible agent can connect to GitHub's MCP server.

Recommended principle:

- begin with repository/read capabilities
- enable write tools only when you want the agent to create or modify repository content
- keep toolsets narrow
- continue treating repository files as the persistence layer

MCP improves discovery and actions; it does not replace the Git-based state convention.

## Stage 3 — Local/cloud execution environment

Later, give the agent a checked-out working tree in a local VM, dev container, Codespace, cloud computer, or similar environment.

Then the startup sequence becomes:

1. `git status`
2. identify branch and upstream
3. inspect recent relevant commits/diff
4. read `START_HERE.md`
5. read relevant `.agent` files
6. inspect only needed source/tests
7. edit
8. run relevant tests/build
9. inspect `git diff`
10. update `.agent` state
11. commit/push/open PR as permitted

## Optional local helper

If you later want automatic project discovery, a tiny script can:

1. clone/pull `agent-skills`
2. parse `PROJECTS.md`
3. clone or locate the requested repo
4. print the paths to the startup files

Do not add this until you actually need it. The GitHub-only convention should remain usable without it.
