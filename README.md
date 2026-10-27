# LLM & Reasoning Lab

A personal engineering workspace for studying Sebastian Raschka's books, building original implementations, and developing projects that can be inspected and reproduced.

**Current status:** the workspace and reference resources are organized. No personal model implementations or measured experiment results have been added to this repository yet.

## Start here

| What you want to see | Where to go |
| --- | --- |
| Personal implementations, exercises, and projects | [Personal work index](work/README.md) |
| The two books' original code and learning resources | [Book resource index](resources/README.md) |
| How work moves from an exercise to a reviewable project | [Workspace workflow](docs/WORKFLOW.md) |
| Source revisions, licenses, and import history | [Source provenance](SOURCE_NOTES.md) |

## Selected work

No completed projects are featured yet. As projects become ready to review, this section will link directly to their existing folders under [work/](work/README.md).

Each featured project should explain the problem, personal contribution, source material, how to run it, evidence for its results, and its limitations. The repository owner writes those technical explanations and chooses when a project is ready.

## What belongs where

| Area | Ownership and purpose |
| --- | --- |
| [work/llm/](work/llm/README.md) | Personal LLM-book implementations, exercise attempts, tests, and notes |
| [work/reasoning/](work/reasoning/README.md) | Personal reasoning-book implementations, evaluations, tests, and notes |
| [work/projects/](work/projects/README.md) | Independent projects and extensions developed from the learning work |
| [resources/books/llm/](resources/books/llm/README.md) | Upstream LLM-book reference snapshot |
| [resources/books/reasoning/](resources/books/reasoning/README.md) | Upstream reasoning-book reference snapshot |
| [docs/](docs/WORKFLOW.md), this README, and [AGENTS.md](AGENTS.md) | Workspace administration and contribution rules |

**Resources are attributed to their original authors.** Imported solutions, tests, commit history, and example results are reference material. They do not represent personal implementations or completed learning milestones.

Personal work identifies whether it was implemented from an explanation, reproduced, adapted from code, or developed as an extension. Reused material is cited where it is used.

## Get the workspace

    git clone https://github.com/SquirmyWormy275/LLMs-from-scratch.git
    cd LLMs-from-scratch

That single clone includes both books. Each book retains its own setup instructions and environment:

- [LLM-book setup](resources/books/llm/setup/README.md)
- [Reasoning-book setup](resources/books/reasoning/ch02/02_setup-tips/README.md)

Run reference examples from the relevant book directory. Personal projects under work/ will document their own setup as they are built; there is no shared root Python environment.

## Authorship and assistance

The repository owner writes the substantive implementations, tests, experiments, and technical conclusions. AI assistance is used for requested Git administration, organization, and help with stuck points. The [working agreement](AGENTS.md) records that boundary. Any specifically requested AI code contribution must be identified honestly.

Source licenses and notices remain with the corresponding [book resources](SOURCE_NOTES.md).
