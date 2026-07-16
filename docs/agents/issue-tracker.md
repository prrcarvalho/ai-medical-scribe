# Issue tracker: Linear

Issues, projects, specifications, and Wayfinder maps for this repository live in Linear. Use the installed Linear app and its OAuth connection for tracker operations.

GitHub has a separate role: it hosts the repository and supports branches, commits, pull requests, reviews, CI, and releases. Do not duplicate routine planning tickets in GitHub Issues.

## Before tracker operations

- Confirm access to the intended Linear workspace.
- Confirm the team and project before creating or changing issues.
- Read existing issues and labels before writing.
- Confirm priority, cycle, assignee, labels, and due date when they matter.
- Explain the grouping before performing bulk changes.

## General operations

- Create one Linear issue per independently trackable question or unit of work.
- Use issue comments for decisions, evidence, progress, and resolution context.
- Use Linear's native parent/sub-issue and blocking relationships when available.
- Assign an issue before starting work when assignment represents a claim.
- Close or move an issue to the team's completed state only when its outcome is recorded.
- Refer to issues by their linked titles in user-facing text, not only by identifiers.

## When a skill says “publish to the issue tracker”

Create the artifact in the confirmed Linear team and project. Preserve the structure, labels, relationships, and status required by that skill.

## When a skill says “fetch the relevant ticket”

Read the Linear issue, its comments, labels, status, assignee, parent, sub-issues, and blocking relationships as needed.

## Wayfinding operations

- **Map:** one Linear issue labelled `wayfinder:map`. Its description contains only Destination, Notes, Decisions so far, Not yet specified, and Out of scope.
- **Ticket:** one child issue of the map, labelled exactly one of `wayfinder:research`, `wayfinder:prototype`, `wayfinder:grilling`, or `wayfinder:task`.
- **Blocking:** represent dependencies with Linear's native blocked/blocking relationship. If the connected app cannot write that relationship, stop and ask the user to add it in Linear; do not silently replace it with an invisible convention.
- **Frontier:** open child issues whose blockers are complete and which have no assignee.
- **Claim:** assign the selected frontier ticket to the driving developer before doing any work.
- **Resolve:** add the answer as a resolution comment, move the ticket to the completed state, and append a linked one-line gist to the map's Decisions so far.
- **Fog:** keep questions that cannot yet be precisely stated in the map's Not yet specified section. Graduate them into child issues only when the question becomes precise.

## Learning objective

Use the tracker as a practical software-lifecycle case study. Briefly explain consequential choices involving issue structure, prioritisation, dependencies, cycles, project organisation, and status transitions while applying them.
