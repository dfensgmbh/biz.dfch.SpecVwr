---
classification: null
created: '2026-11-22T17:12:51.304+01:00'
id: 850d1d09-40af-480b-b716-33295a157159
status: draft
type: qa
updated: '2026-11-22T17:18:19.103+01:00'
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

Each question has an HTML comment that names its audience (M, U or both). The
answers are still open and will be recorded during the interviews.
Interviewer: Irene Hofstetter. Dates: TODO.

### Raw Requirements

Taken from the README: SpecVwr is an MCP server that shows specmgr artifacts
(GOL, REQ, UC, ADR, DEC, RSK, TSK …) as a clickable diagram. Nodes are
artifacts, edges are references. A click on a node opens the artifact with
links to the connected artifacts. The first version is read-only. No other
raw requirements exist yet.

## Elicitation Context

<!-- Audience: M and U -->

> **0.0010**: What is your role in the specmgr environment, and how often do
> you work with specmgr artifacts?

TODO: answer pending

<!-- Audience: M and U -->

> **0.0020**: Which problem should SpecVwr solve for you, and how will you
> know that the project is a success (goals)?

TODO: answer pending

<!-- Audience: M and U -->

> **0.0030**: Which constraints apply (deadlines, budget, licence, required
> technologies, operating systems)?

TODO: answer pending

<!-- Audience: M -->

> **0.0040**: Which other people or groups should we interview or inform?

TODO: answer pending

<!-- Audience: U; personas -->

> **0.0050**: Describe a typical situation in which you would open SpecVwr:
> who are you in that situation, what do you want to know, and how much time
> do you have?

TODO: answer pending

<!-- Audience: M and U; goal conflicts -->

> **0.0060**: Which goals are in conflict from your point of view (for
> example scope against deadline, overview against level of detail)? Which
> one has priority?

TODO: answer pending

## Functional Suitability

<!-- Audience: U -->

> **1.0010**: Which artifact types and which reference types must be visible
> in the diagram, and which can be left out?

TODO: answer pending

<!-- Audience: U -->

> **1.0020**: Which functions do you need in the diagram (filter, search,
> zoom, colour by status, subgraph starting from one artifact)?

TODO: answer pending

<!-- Audience: U -->

> **1.0030**: What should be shown after a click on a node (the full
> artifact, a summary, only the frontmatter)?

TODO: answer pending

<!-- Audience: M and U -->

> **1.0040**: Is "read-only" correct for the first version? Which write
> functions would be necessary later?

TODO: answer pending

## Performance Efficiency

<!-- Audience: M -->

> **2.0010**: How many artifacts and references does a large specmgr
> repository have today, and how many do you expect in two years?

TODO: answer pending

<!-- Audience: U -->

> **2.0020**: How long can it take until the diagram is shown?

TODO: answer pending

## Compatibility

<!-- Audience: M; interfaces, system context -->

> **3.0010**: Through which interface should SpecVwr read the artifacts:
> directly from the Markdown files, through the specmgr Python API or through
> the specmgr MCP server?

TODO: answer pending

<!-- Audience: M -->

> **3.0020**: How stable is the specmgr artifact and reference format, and
> how will we learn about changes?

TODO: answer pending

<!-- Audience: U; system context -->

> **3.0030**: In which tools should SpecVwr run (Opencode, Claude Code,
> browser, other MCP clients)?

TODO: answer pending

<!-- Audience: M and U -->

> **3.0040**: Must translated artifacts (for example docs/req/de/) be shown,
> and how?

TODO: answer pending

## Interaction Capability

<!-- Audience: U -->

> **4.0010**: Which language should the user interface have, and which
> accessibility requirements apply (keyboard, contrast, colour blindness)?

TODO: answer pending

<!-- Audience: U -->

> **4.0020**: Which existing tools show graphs the way you want? What do you
> dislike about these tools?

TODO: answer pending

## Reliability

<!-- Audience: M and U -->

> **5.0010**: What should happen when an artifact is invalid or a reference
> points to a missing artifact?

TODO: answer pending

## Security

<!-- Audience: M -->

> **6.0010**: Do the artifacts contain confidential content (classification)?
> Must SpecVwr show the classification or hide content?

TODO: answer pending

<!-- Audience: M -->

> **6.0020**: Can SpecVwr send data outside the local computer, for example
> to a diagram service?

TODO: answer pending

## Maintainability

<!-- Audience: M -->

> **7.0010**: Who maintains SpecVwr after the project, and which rules apply
> to code, tests and documentation?

TODO: answer pending

<!-- Audience: M -->

> **7.0020**: How should SpecVwr be delivered (PyPI package, uvx, Opencode
> plugin)?

TODO: answer pending

## Flexibility

<!-- Audience: M -->

> **8.0010**: Will new artifact types be added in the future, and should
> SpecVwr show them without code changes?

TODO: answer pending

## Safety

<!-- Audience: M and U -->

> **9.0010**: Can an incorrect or incomplete view cause wrong decisions? How
> should SpecVwr show that data is missing?

TODO: answer pending

## More Information

Acceptance criteria: at the end of each interview, ask: "How will you know at
acceptance that SpecVwr meets your requirements?" The answers are added here
and later transferred into REQ and UC artifacts.

- Acceptance criteria maintainer: TODO
- Acceptance criteria users: TODO
