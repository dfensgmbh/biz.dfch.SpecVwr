---
classification: null
created: '2026-11-22T17:12:51.304+01:00'
id: 850d1d09-40af-480b-b716-33295a157159
status: draft
type: qa
updated: '2026-11-22T18:47:02.756+01:00'
version: 1.0.0
---

# Stakeholder Interview Guide SpecVwr

## General

### Introduction

This guide prepares the stakeholder interviews for SpecVwr (competencies a1
and g1: clarify goals, constraints, system context, interfaces, goal
conflicts, personas and acceptance criteria).

Two stakeholder groups are interviewed:

- **M**: the specmgr maintainer (supplies the artifacts and the data format);
- **U**: the people who will work with SpecVwr (users).

Each question has an HTML comment that names its audience (M or U). A
question for both groups is split into one question per group: the M
question keeps its number, the U question gets the next number. Questions
with the comment "follow-up from the review" were added after the review of
the maintainer answers.

Interviewer: Irene Hofstetter. Dates:

- Maintainer: 2026-11-22 (answers recorded); follow-up questions open.
- Users: TODO (the answers are still open).

### Raw Requirements

Taken from the README: SpecVwr is an MCP server that shows specmgr artifacts
(GOL, REQ, UC, ADR, DEC, RSK, TSK …) as a clickable diagram. Nodes are
artifacts, edges are references. A click on a node opens the artifact with
links to the connected artifacts. The first version is read-only. No other
raw requirements exist yet.

Correction after the maintainer interview (0.0020, 1.0040, 3.0010):
SpecVwr is an OpenCode plugin, not an MCP server. It shows the artifacts in
a spreadsheet-like table, not in a diagram. A cell is clickable when an
artifact refers to another artifact.

## Elicitation Context

<!-- Audience: M -->

> **0.0010**: Maintainer: What is your role in the specmgr environment, and
> how often do you work with specmgr artifacts?

Daily. I define the functionality of the biz.dfch.SpecMgr MCP server, and
SpecVwr helps to visualise these artifacts. So I have a great say in what
SpecVwr must do.

<!-- Audience: U -->

> **0.0011**: User: What is your role in the specmgr environment, and how
> often do you work with specmgr artifacts?

TODO: answer pending

<!-- Audience: M -->

> **0.0020**: Maintainer: Which problem should SpecVwr solve for you, and how
> will you know that the project is a success (goals)?

At this time, SpecMgr writes artifacts to a docs folder (configured in the
.env file). We use a code editor to show the docs. SpecVwr must make it much
easier to show the docs and their references and relationships in OpenCode.
SpecVwr shows the docs in a spreadsheet-like table, not in a diagram. A cell
is clickable when a doc refers to another doc. The project is a success when
I can search, filter, sort and track references in SpecMgr docs.

<!-- Audience: U -->

> **0.0021**: User: Which problem should SpecVwr solve for you, and how will
> you know that the project is a success (goals)?

TODO: answer pending

<!-- Audience: M -->

> **0.0030**: Maintainer: Which constraints apply (deadlines, budget, licence,
> required technologies, operating systems)?

- OpenCode: SpecVwr must work with OpenCode v2 (NOT v1).
- Operating systems: Linux and Windows (where OpenCode runs too).
- Maintainability: SpecVwr must be easy to maintain.
- Deadline: 2027-02-20 (90 days from 2026-11-22).
- Licence: AGPL v3.0 ONLY (SPDX: `AGPL-3.0-only`).
- Technology: given by OpenCode, that is Node.js with JavaScript/TypeScript.
- SpecMgr: SpecVwr must work with our
  [SpecMgr MCP server](https://github.com/dfch/biz.dfch.SpecMgr).

<!-- Audience: U -->

> **0.0031**: User: Which constraints apply (deadlines, budget, licence,
> required technologies, operating systems)?

TODO: answer pending

<!-- Audience: M -->

> **0.0040**: Which other people or groups should we interview or inform?

Users are mainly business analysts, architects and testers. They can
contribute to this QA. TODO: Irene Hofstetter names the people and groups to
interview or inform.

<!-- Audience: U; personas -->

> **0.0050**: Describe a typical situation in which you would open SpecVwr:
> who are you in that situation, what do you want to know, and how much time
> do you have?

TODO: answer pending

<!-- Audience: M; goal conflicts -->

> **0.0060**: Maintainer: Which goals are in conflict from your point of view
> (for example scope against deadline, overview against level of detail)?
> Which one has priority?

Scope against deadline. The deadline is fixed and has priority 1. Reduced
functionality is acceptable.

<!-- Audience: U; goal conflicts -->

> **0.0061**: User: Which goals are in conflict from your point of view (for
> example scope against deadline, overview against level of detail)? Which
> one has priority?

TODO: answer pending

## Functional Suitability

<!-- Audience: U -->

> **1.0010**: Which artifact types and which reference types must be visible
> in the table, and which can be left out?

TODO: answer pending

<!-- Audience: U -->

> **1.0020**: Which functions do you need in the table (filter, search, sort,
> colour by status, only the artifacts that one artifact refers to)?

TODO: answer pending

<!-- Audience: U -->

> **1.0030**: What should be shown after a click on an artifact or a
> reference cell (the full artifact, a summary, only the frontmatter)?

TODO: answer pending

<!-- Audience: M -->

> **1.0040**: Maintainer: Is "read-only" correct for the first version? Which
> write functions would be necessary later?

SpecVwr will stay read-only for the foreseeable future. This is because the
OpenCode plugin framework cannot make tool calls into MCP servers, and the
SpecMgr MCP server is the only system that is permitted to change SpecMgr
docs.

Note: the reason "cannot make tool calls into MCP servers" is not confirmed.
The OpenCode documentation ([plugins](https://opencode.ai/docs/plugins/),
[MCP servers](https://opencode.ai/docs/mcp-servers/),
[SDK](https://opencode.ai/docs/sdk/)) and the
[plugin API README](https://github.com/anomalyco/opencode/blob/dev/packages/plugin/src/README.md)
do not say whether a plugin can call MCP tools. For MCP, the plugin API
documents only how to change and reload the configuration (`ctx.mcp.transform`,
`ctx.mcp.reload()`). TODO: confirm in the OpenCode source code or with the
OpenCode maintainers.

<!-- Audience: U -->

> **1.0041**: User: Is "read-only" correct for the first version? Which write
> functions would be necessary later?

TODO: answer pending

<!-- Audience: M -->

> **1.0050**: Maintainer: Which functions does SpecVwr need in addition to
> the table (for example copy to the clipboard)?

SpecVwr supports the clipboard, so that a user can copy the UUID of a
document.

<!-- Audience: M; follow-up from the review of the maintainer answers -->

> **1.0060**: Maintainer: 7.0010 names both the terminal interface
> (`@opencode/plugin/tui`) and the desktop app (`./gui-experimental`). Which
> one must the first version support? Is the other one needed before the
> deadline?

TODO: answer pending

<!-- Audience: M; follow-up from the review of the maintainer answers -->

> **1.0070**: Maintainer: Which acceptance criteria must the first version
> meet? Draft from 0.0020: a user can search, filter and sort the docs, and
> follow the references between them.

TODO: answer pending

## Performance Efficiency

<!-- Audience: M -->

> **2.0010**: How many artifacts and references does a large specmgr
> repository have today, and how many do you expect in two years?

Several hundreds to some thousands of docs. Each doc can have multiple
references (about 20 on average). Tables must support paging.

<!-- Audience: U -->

> **2.0020**: How long can it take until the table is shown?

TODO: answer pending

<!-- Audience: M; follow-up from the review of the maintainer answers -->

> **2.0030**: Maintainer: Search, filter and sort must cover all docs, not
> only the page that is shown (see 2.0010). How long can a search, a filter
> or a sort take with some thousands of docs?

TODO: answer pending

## Compatibility

<!-- Audience: M; interfaces, system context -->

> **3.0010**: Through which interface should SpecVwr read the artifacts:
> directly from the Markdown files, through the specmgr Python API or through
> the specmgr MCP server?

Directly from the Markdown files on disk. SpecVwr cannot call the SpecMgr MCP
server (see 1.0040). It gets the docs path from the `SPECMGR_DOCS_DIR`
variable in the .env file, or it uses the same default path as SpecMgr
(`docs`).

<!-- Audience: M -->

> **3.0020**: How stable is the specmgr artifact and reference format, and
> how will we learn about changes?

The format is stable. Every type is an AST. The field `version` in the
frontmatter is the meta version (the version of the document format), NOT
the version of the document. SpecMgr changes are listed in its
[changelog](https://github.com/dfch/biz.dfch.SpecMgr/blob/main/CHANGELOG.md).

<!-- Audience: U; system context -->

> **3.0030**: In which tools should SpecVwr run (Opencode, Claude Code,
> browser, other MCP clients)?

Only in OpenCode v2. (Answered by the maintainer as a user: an architect.)

<!-- Audience: M -->

> **3.0040**: Maintainer: Must translated artifacts (for example docs/req/de/)
> be shown, and how?

Yes. The user sees only the docs of one selected language. The default
language is EN. For each doc shown, SpecVwr shows the other languages that
are available.

<!-- Audience: U -->

> **3.0041**: User: Must translated artifacts (for example docs/req/de/) be
> shown, and how?

TODO: answer pending

<!-- Audience: M; follow-up from the review of the maintainer answers -->

> **3.0050**: Maintainer: `SPECMGR_DOCS_DIR` does not apply to all types:
> ADRs use `SPECMGR_ADR_DIR` (default `docs/adr`) and FEATs use
> `SPECMGR_FEAT_DIR` (default `.specmgr/feat`). Must SpecVwr show ADRs and
> FEATs, and must it read these variables too?

TODO: answer pending

<!-- Audience: M; follow-up from the review of the maintainer answers -->

> **3.0060**: Maintainer: If an OpenCode plugin can call MCP tools after all
> (see the note in 1.0040), should SpecVwr read the docs through the SpecMgr
> MCP server instead of parsing the Markdown files itself?

TODO: answer pending

## Interaction Capability

<!-- Audience: U -->

> **4.0010**: Which language should the user interface have, and which
> accessibility requirements apply (keyboard, contrast, colour blindness)?

The main user interface is EN ONLY. (Answered by the maintainer as a user:
an architect.)

<!-- Audience: U -->

> **4.0020**: Which existing tools show tables the way you want? What do you
> dislike about these tools?

TODO: answer pending

<!-- Audience: M; follow-up from the review of the maintainer answers -->

> **4.0030**: Maintainer: 4.0010 answers only the language. 7.0010 asks for
> end-to-end tests with an accessibility check. Which accessibility
> requirements apply (for example keyboard-only use, contrast, colour
> blindness, screen readers, a standard such as WCAG)?

TODO: answer pending

## Reliability

<!-- Audience: M -->

> **5.0010**: Maintainer: What should happen when an artifact is invalid or a
> reference points to a missing artifact?

Show a warning. If SpecMgr gives an error, show the error.

<!-- Audience: U -->

> **5.0011**: User: What should happen when an artifact is invalid or a
> reference points to a missing artifact?

TODO: answer pending

<!-- Audience: M; follow-up from the review of the maintainer answers -->

> **5.0020**: Maintainer: 5.0010 says "If SpecMgr gives an error, show the
> error". SpecVwr reads the files directly and does not call SpecMgr (see
> 3.0010). Which errors do you mean?

TODO: answer pending

<!-- Audience: M; follow-up from the review of the maintainer answers -->

> **5.0030**: Maintainer: 5.0010 says that an invalid artifact or a missing
> reference shows a warning, and 9.0010 says that missing data shows an
> error. When does SpecVwr show a warning, and when an error?

TODO: answer pending

## Security

<!-- Audience: M -->

> **6.0010**: Do the artifacts contain confidential content (classification)?
> Must SpecVwr show the classification or hide content?

Yes, docs can contain classified information. The field `classification` in
the frontmatter shows the level. SpecVwr shows all docs, regardless of their
classification, because SpecMgr and SpecVwr operate in classified
environments.

<!-- Audience: M -->

> **6.0020**: Can SpecVwr send data outside the local computer, for example
> to a diagram service?

No. No data leaves the local computer. There is no exception.

<!-- Audience: M; follow-up from the review of the maintainer answers -->

> **6.0030**: Maintainer: OpenCode sends the content of the chat to an AI
> model provider. Must SpecVwr make sure that the content of the docs never
> gets into the chat (for example as a tool result), so that classified
> content does not leave the computer?

TODO: answer pending

## Maintainability

<!-- Audience: M -->

> **7.0010**: Who maintains SpecVwr after the project, and which rules apply
> to code, tests and documentation?

Employees of the d-fens organisation maintain SpecVwr.

Code: SpecVwr follows the OpenCode V2 plugin conventions:

- TypeScript with ES modules.
- The entry file exports `Plugin.define({ id, setup })` from
  `@opencode/plugin`. `setup` can return a cleanup function.
- The plugin configuration comes from `ctx.options`.
- `effect` (`^4.0.0`) is a `peerDependency` and a `devDependency`, never a
  bundled dependency. Schemas use `Schema` from `effect`.
- The user interface uses `@opencode/plugin/tui` (terminal) or the
  `./gui-experimental` export (OpenCode Desktop).

Sources: [OpenCode plugins](https://opencode.ai/docs/plugins/) and
[plugin API README](https://github.com/anomalyco/opencode/blob/dev/packages/plugin/src/README.md).
OpenCode gives no rules for tests or linting.

Process and CI: the same rules as biz.dfch.SpecMgrDemo
(`.github/workflows/ci.yml`, `justfile`, `.github/CODEOWNERS`):

- All work is done on a topic branch. Changes go to `dev` and `main` only
  through a pull request.
- A person other than the developer must approve each pull request.
- CI runs for each pull request to `dev` and `main`. Each job runs one
  `just` recipe, and each action is pinned to a full commit SHA.
- Gates: valid specmgr docs, Conventional Commits with the feature number as
  scope, permitted licences (SBOM), lint, unit tests, end-to-end tests with
  an accessibility check, mutation tests, architecture tests, traceability,
  and scans for vulnerabilities, secrets and workflows.
- CODEOWNERS: a change to the CI configuration, the `justfile`, the gate
  scripts or the decisions (`docs/dec/`) needs the review of the owner.

TODO: select the SpecMgrDemo gates that apply to SpecVwr (SpecMgrDemo also
has gates for its Java backend).

<!-- Audience: M -->

> **7.0020**: How should SpecVwr be delivered (PyPI package, uvx, Opencode
> plugin)?

As an OpenCode plugin, in the way that OpenCode recommends.

TODO: confirm this suggestion. Publish SpecVwr as an npm package that is
built with the OpenCode plugin API (`@opencode/plugin`, see 7.0010). Users
add it to the `plugins` list in `opencode.json(c)` with a pinned version
(for example `<package>@1.0.0`), or they install it with
`opencode plugin add`. OpenCode can also load a plugin from a Git repository
or from a local folder (`.opencode/plugins/`); this can help in classified
environments without internet access. Source:
[OpenCode plugins](https://opencode.ai/docs/plugins/).

## Flexibility

<!-- Audience: M -->

> **8.0010**: Will new artifact types be added in the future, and should
> SpecVwr show them without code changes?

Yes. We will then update SpecVwr. No automatic discovery.

## Safety

<!-- Audience: M -->

> **9.0010**: Maintainer: Can an incorrect or incomplete view cause wrong
> decisions? How should SpecVwr show that data is missing?

Not known at this time. Missing data will show an error.

<!-- Audience: U -->

> **9.0011**: User: Can an incorrect or incomplete view cause wrong decisions?
> How should SpecVwr show that data is missing?

TODO: answer pending

## More Information

Acceptance criteria: at the end of each interview, ask: "How will you know at
acceptance that SpecVwr meets your requirements?" The answers are added here
and later transferred into REQ and UC artifacts.

- Acceptance criteria maintainer: TODO
- Acceptance criteria users: TODO
