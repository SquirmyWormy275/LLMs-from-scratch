# Book resources — upstream reference material

This directory contains the books' companion repositories, preserved as reference snapshots. Their code, exercise solutions, tests, documentation, and recorded results were supplied by Sebastian Raschka and the respective contributors.

**Personal implementation work belongs in [work/](../work/README.md).**

## Choose a book

| Book | Overview | Setup | Personal work |
| --- | --- | --- | --- |
| Build a Large Language Model (From Scratch) | [Book README and chapter index](books/llm/README.md) | [Environment setup](books/llm/setup/README.md) | [work/llm/](../work/llm/README.md) |
| Build a Reasoning Model (From Scratch) | [Book README and chapter index](books/reasoning/README.md) | [Setup tips](books/reasoning/ch02/02_setup-tips/README.md) | [work/reasoning/](../work/reasoning/README.md) |

## How to use these copies

1. Open the relevant book README and follow its chapter links.
2. To run a reference example, change into that book's directory and follow its own setup instructions.
3. Create your own attempt in the matching work/ area, keeping notes and experiment evidence with that attempt.
4. If you reuse source code, identify its origin and your changes in the personal work's README.

The READMEs inside the book folders are the original upstream documents. Their first-person descriptions, badges, citations, and example measurements refer to the upstream projects.

The book folders retain their own package metadata, requirements, and workflow files. Their nested workflow files are reference copies; they are not the workspace's active GitHub Actions workflows.

## Provenance and updates

See [SOURCE_NOTES.md](../SOURCE_NOTES.md) for exact source revisions, licenses, and the two structural omissions from the LLM snapshot. Source updates are deliberate imports, kept separate from personal implementation commits.

[Back to the workspace](../README.md)
