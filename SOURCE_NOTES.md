# Source provenance and maintenance

This is one working repository containing two attributed book-resource snapshots and a separate area for personal work. GitHub records the repository's fork relationship with the original LLM repository; both books' files are included directly in a normal clone.

## Source snapshots

| Material | Location here | Recorded source revision | License |
| --- | --- | --- | --- |
| LLM book | [resources/books/llm/](resources/books/llm/README.md) | [rasbt/LLMs-from-scratch at cdbd33e6d57a71e20ea31434841095fac50cecd8](https://github.com/rasbt/LLMs-from-scratch/tree/cdbd33e6d57a71e20ea31434841095fac50cecd8) | [LLM license](resources/books/llm/LICENSE.txt) |
| Reasoning book | [resources/books/reasoning/](resources/books/reasoning/README.md) | [rasbt/reasoning-from-scratch at a788466dc85cfe8617b6c0b809ed4ab9084485de](https://github.com/rasbt/reasoning-from-scratch/tree/a788466dc85cfe8617b6c0b809ed4ab9084485de) | [Reasoning license](resources/books/reasoning/LICENSE) |

The companion code, exercises, solutions, tests, documentation, and recorded results belong to Sebastian Raschka and the respective contributors. Their original Git histories and notices are retained. An imported commit or result is not a personal contribution or learning milestone of this workspace's owner.

## Snapshot integrity and import exceptions

The reasoning snapshot is a complete copy of the recorded source tree, including its original project configuration, README, and license.

The LLM snapshot preserves the recorded source files and their original contents, with two structural omissions:

1. The original reasoning-from-scratch submodule entry is omitted.
2. The corresponding .gitmodules file is omitted.

Both are unnecessary because the complete reasoning snapshot is included beside the LLM snapshot under resources/books/. There are no submodules to initialize.

Earlier workspace navigation and pytest-discovery changes were removed from the LLM README and project configuration before relocation. Those resource files have been restored to their recorded upstream versions.

## Personal work and administrative scaffolding

[work/](work/README.md) is reserved for the owner's implementations, attempts, tests, experiments, and technical explanations. Each item identifies reproduced or adapted material and the owner's actual contribution.

The root navigation, work-area navigation pages, workflow guide, source notes, ignore rules, and [working agreement](AGENTS.md) were prepared with AI assistance as repository administration. They do not contain completed exercise solutions, personal model implementations, experimental findings, or accounts of learning.

The root .gitattributes marks resources/ as vendored material for GitHub Linguist. This distinguishes the imported code from personal work in language statistics; see [GitHub Linguist's attribute documentation](https://github.com/github-linguist/linguist/blob/main/docs/overrides.md).

## Environments and workflows

Each book remains a complete project in its own directory. Its requirements, package configuration, setup documentation, and source files stay together. Follow the [resource index](resources/README.md) to choose the relevant environment.

Upstream .github directories are preserved inside the resource snapshots. These nested workflow files are reference material, not active root GitHub Actions workflows. Workspace CI can be added when there are actual personal checks to run.

## Updating a book snapshot

1. Fetch the selected revision from that book's official upstream repository.
2. Review the changes and import them into the matching resources/books/ directory.
3. Preserve the complete project layout, applicable licenses, author notices, and the two intentional LLM omissions.
4. Verify the imported files against the selected source revision and check the workspace navigation.
5. Update the source revision in the table above and make a separate administrative commit.

The workspace root now has a different layout from either upstream repository. Do not use an unreviewed root-level upstream merge or GitHub's generic Sync fork action as a substitute for importing updates into the resource folders.

[Back to the workspace](README.md)
