# Workspace workflow

## The long-term shape

This repository should let a reviewer trace a clear line from a problem, through the owner's implementation and decisions, to reproducible evidence. The books provide learning material; personal work demonstrates what the owner can explain, build, and evaluate.

The root README is the entry point. Book snapshots stay in [resources/](../resources/README.md). Personal work develops in [work/](../work/README.md). Mature projects are linked from the root without being copied to a separate showcase directory.

## A normal working session

1. Read the relevant chapter and inspect or run its reference material in the appropriate book directory.
2. Start or continue your own attempt in the matching work/ area.
3. Keep code, tests, notes, and experiment evidence with that attempt.
4. Record actual commands and observations while working. Separate observations from explanations and open questions.
5. Review the diff and commit a coherent step with a message that describes what actually changed.

If you are stuck, AI assistance can help inspect the problem and discuss a focused explanation or diagnostic. You remain the default author of technical fixes.

## Organizing an individual item

Start with a README and the files the work actually needs. Add structure as it becomes useful:

| Content | Keep it with the project |
| --- | --- |
| Implementations and notebooks | Source files or a source directory |
| Tests and fixtures | The project's test directory |
| Small measured outputs and plots | A results/ directory, with the generating command or run reference |
| Technical notes and decisions | The project README or notes/ directory |
| Environment and run instructions | The project README and its actual dependency files |
| Large datasets and model checkpoints | External or ignored storage, with their source and retrieval instructions recorded |

Do not scatter one project's evidence across global notes, experiments, and showcase folders. Do not invent measurements, hardware details, or conclusions to fill a template.

The root ignore rules keep local environments, caches, credentials, and common large model files out of commits. They do not blanket-ignore reports, small CSV/JSON results, plots, logs, or dependency lockfiles under work/. Review artifacts before committing them.

## Honest status

| Status | Meaning |
| --- | --- |
| Planned | A goal has been selected; implementation or evaluation has not begun |
| In progress | There is a real attempt, with unfinished work identified |
| Ready to review | The owner has reviewed the contribution, runnable instructions, checks, evidence, and limitations |

Keep the detailed status in the work item's README. A passing upstream example or imported test suite does not complete a personal milestone.

## Preparing a selected project

Before featuring an item in the root README, the owner should be able to:

1. Explain the problem and identify exactly what they implemented.
2. Distinguish original work from reproduced or adapted material.
3. Provide commands that match the committed code and environment.
4. Show relevant checks and evidence for the results claimed.
5. Discuss design decisions, tradeoffs, limitations, and remaining questions.

Link to the existing project folder when it is ready. Keep working history and unsuccessful attempts honestly; do not manufacture a cleaner development story.

## Environments and CI

Each book remains an independent project under resources/books/. Change into that book's directory and follow its own setup guide when running reference code.

Personal work should document its own environment as it is built. There is no root Python package or shared environment to install. Upstream workflow files are preserved inside the resource snapshots and are not active workspace CI.

Add focused workspace CI once there are owner-written checks to run. Mechanical CI wiring can be delegated; defining test assertions, evaluation logic, or scientific success criteria remains substantive work.

## Source maintenance and Git administration

Keep resource updates in separate administrative commits and update [SOURCE_NOTES.md](../SOURCE_NOTES.md) with the imported revision. Preserve licenses and do not silently patch reference solutions.

Administrative commits should describe organization, provenance, or tooling changes. Personal implementation commits should describe actual technical work. The [working agreement](../AGENTS.md) governs assistant contributions.

[Back to the workspace](../README.md)
