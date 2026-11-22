---
classification: null
created: '2026-11-22T18:45:17.755+01:00'
id: 99136108-dccf-45ba-a974-ded247d4a2c9
status: draft
type: tsk
updated: '2026-11-22T18:55:52.803+01:00'
version: 1.0.0
---

# SpecVwr Project Setup and Requirements Elicitation

<!-- Open and done tasks from the repository setup and the stakeholder
interviews (QA 850d1d09-40af-480b-b716-33295a157159). Numbered so that they
are easier to track. The newest entry under "Recent Updates" describes the
current state and where to continue. -->

- [x] Task 1: Interview the specmgr maintainer and record the answers in the QA

- [x] Task 2: Delete the old GitHub token with organisation admin rights

- [x] Task 3: Turn off AI attribution in commits and pull requests

- [ ] Task 4: Get approval from a second person and merge PR #1 (setup/specmgr into dev)

- [x] Task 5: Add the follow-up questions from the QA review to the QA (contradictions, technical risks, open points)

- [x] Task 6: Set the interview date and update the introduction of the QA

- [ ] Task 7: Name the users to interview (business analysts, architects, testers; QA 0.0040)

- [ ] Task 8: Interview the users and record the answers in the QA

- [x] Task 9: Add the commit and review rules from QA 7.0010 to AGENTS.md

- [x] Task 10: Add the missing entries to the local AI usage log

- [ ] Task 11: Get the maintainer's answers to the follow-up questions in the QA (1.0060, 1.0070, 2.0030, 3.0050, 3.0060, 4.0030, 5.0020, 5.0030, 6.0030)

- [x] Task 12: Confirm whether an OpenCode plugin can call MCP tools, in the OpenCode source code or with the OpenCode maintainers (TODO in QA 1.0040)

- [ ] Task 13: Select the SpecMgrDemo CI gates that apply to SpecVwr (TODO in QA 7.0010)

- [ ] Task 14: Confirm the delivery as an npm package built with the OpenCode plugin API (TODO in QA 7.0020)

- [ ] Task 15: Confirm with the maintainer the commit scope for commits that belong to no feature (AGENTS.md uses no scope until then)

- [ ] Task 16: Record how SpecVwr reads the docs (Markdown files or SpecMgr MCP server) as a decision (DEC), after tasks 11 and 12

- [ ] Task 17: Turn the answered QA questions into goals, requirements and use cases (GOL, REQ, UC)

## Recent Updates

<!-- Newest entry first -- prepend new entries directly below this comment. -->

### 2026-11-22 17:55:42.322Z - Task 12 done: plugins cannot call MCP tools

Checked in the OpenCode source code (branch `dev`, commit 6d978e2): the
plugin API has no function that calls an MCP tool. The result is in the note
of QA 1.0040. Not tested: whether a plugin can start the SpecMgr MCP server
itself; follow-up question 3.0060 now asks the maintainer about this.

Where to continue: task 11 (maintainer answers, now including the changed
3.0060), then task 16 (decision on how SpecVwr reads the docs). Tasks 7 and
8 can run in parallel.

### 2026-11-22 17:50:58.910Z - Handover: current state and where to continue

State: the repository setup is done. All work is on the branch
`setup/specmgr`, which is pushed; PR #1 (setup/specmgr into dev) is open and
waits for the approval of a second person. No code exists yet; the project
is in requirements elicitation.

Done so far: the maintainer interview (2026-11-22) and its review; nine
follow-up questions are in the QA. The user interviews have not started.

Where to continue: first get the maintainer's answers to the follow-up
questions (task 11) and confirm the OpenCode MCP question (task 12),
because the decision about how SpecVwr reads the docs (task 16) depends on
both. In parallel, name the users and interview them (tasks 7 and 8). Then
turn the answers into GOL, REQ and UC artifacts (task 17).

Conventions for the next agent are in AGENTS.md (branches, pull requests,
commit messages, English only, no AI attribution, the local AI usage log).

### 2026-11-22 17:47:20.724Z - Tasks 5, 6, 9 and 10 done

Added nine follow-up questions to the QA, set the maintainer interview date,
added the commit and review rules to AGENTS.md, and updated the local AI
usage log. Added task 11 for the answers to the follow-up questions.

### 2026-11-22 17:45:12.672Z - Task list created

Created from the open items after the maintainer interview and the review of
its answers. Tasks 1 to 3 are already done.
