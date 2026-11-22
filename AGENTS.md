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
