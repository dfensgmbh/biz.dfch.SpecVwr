# AGENTS.md

Instructions for AI coding agents working in this repository.

## Git workflow

- `dev` is the integration branch. Never commit or push directly to `dev`
  (and never to `main`).
- Do all work on a topic branch created from `dev`, for example
  `feature/<topic>`, `fix/<topic>` or `docs/<topic>`.
- Commit and push only when the user asks for it.
- Changes reach `dev` only through a pull request into `dev`.
- Do not add AI attribution to commit messages or pull requests: no
  `Co-Authored-By` trailer for an AI tool, no "Generated with" line.
