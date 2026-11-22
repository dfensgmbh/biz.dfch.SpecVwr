# AGENTS.md

Instructions for AI coding agents working in this repository.

## Git workflow

- `dev` is the integration branch. Never commit or push directly to `dev`
  (and never to `main`).
- Do all work on a topic branch created from `dev`, for example
  `feature/<topic>`, `fix/<topic>` or `docs/<topic>`.
- Commit and push only when the user asks for it.
- Changes reach `dev` and `main` only through a pull request.
- A person other than the developer must approve each pull request.
- Commit messages follow Conventional Commits
  (<https://www.conventionalcommits.org/>). The scope is the specmgr feature
  number, for example `feat(feat-001): add the artifact table`.
- A change to the CI configuration, the `justfile`, the gate scripts or the
  decisions (`docs/dec/`) needs the review of the code owner.
- Do not add AI attribution to commit messages or pull requests: no
  `Co-Authored-By` trailer for an AI tool, no "Generated with" line.

The rules for pull requests, reviews and commit messages come from answer
7.0010 in the stakeholder interview guide
(QA 850d1d09-40af-480b-b716-33295a157159).

Until the maintainer decides otherwise, a commit that belongs to no feature
(setup, documentation, configuration) has no scope, for example
`docs: add the task list`.

## Project conventions

- Write everything in the repository in English: code, comments,
  documentation, specmgr documents and commit messages.
- Manage requirements, decisions and tasks with the specmgr MCP server
  (`.mcp.json`). Do not edit specmgr documents by hand when a specmgr tool
  can do the change.
- Record every AI contribution in the local AI usage log, a specmgr TXT
  document in `docs/txt/` ("AI Usage in the SpecVwr Project"). The log is
  ignored by git and must never be committed. Add new entries at the top of
  its `## Updates` section: state what the AI did, what the user did or
  decided, and which files or artifacts are affected.

## Where to continue

Read the task list first: TSK 99136108-dccf-45ba-a974-ded247d4a2c9
("SpecVwr Project Setup and Requirements Elicitation", `docs/tsk/`). Its
newest update entry describes the current state, the open branch and pull
request, and the next steps.
