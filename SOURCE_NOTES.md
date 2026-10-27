# Source provenance and maintenance

This repository is one working copy for the companion resources from Sebastian Raschka's LLM and reasoning books. GitHub records its fork relationship with the LLM repository. The reasoning repository is incorporated as ordinary tracked files in a directory of this same repository.

## Imported sources

| Material | Location here | Source revision | License |
| --- | --- | --- | --- |
| LLM book | Repository root | [rasbt/LLMs-from-scratch at cdbd33e6d57a71e20ea31434841095fac50cecd8](https://github.com/rasbt/LLMs-from-scratch/tree/cdbd33e6d57a71e20ea31434841095fac50cecd8) | [LICENSE.txt](LICENSE.txt) |
| Reasoning book | `reasoning-from-scratch/` | [rasbt/reasoning-from-scratch at a788466dc85cfe8617b6c0b809ed4ab9084485de](https://github.com/rasbt/reasoning-from-scratch/tree/a788466dc85cfe8617b6c0b809ed4ab9084485de) | [reasoning-from-scratch/LICENSE](reasoning-from-scratch/LICENSE) |

The initial consolidation preserves both repositories' existing Git histories, model code, license files, and author notices. Its new changes are repository administration: replacing the original reasoning submodule with its complete source tree, adding navigation, recording provenance, and keeping root pytest discovery scoped to the LLM workspace. The imported solutions and results were produced upstream; they do not document work completed by the owner of this workspace.

## Working locally

Clone this repository normally. The reasoning resources are included without an additional clone or submodule initialization. Follow the [LLM setup instructions](setup/README.md) and the [reasoning book README](reasoning-from-scratch/README.md) for the respective environments and examples.

## Maintaining the combined layout

- The reasoning directory intentionally contains real tracked files. Its entire tree matches the recorded reasoning revision at the initial import.
- Update each book from its corresponding official upstream repository and record the new revision here. Import reasoning changes under the same directory, preserving any later personal changes through review.
- The official LLM repository still uses a submodule at `reasoning-from-scratch`. Future LLM updates can conflict with this combined layout; preserve the tracked directory when resolving such conflicts.
- The reasoning book's nested `.github/workflows` files are included as upstream resources. Root pytest checks, including the root link collector, exclude the reasoning directory; run reasoning tests from that directory using its own environment and pytest configuration. This consolidation does not configure a shared CI or Python environment for the two books.
- Keep personal implementations, experiments, notes, and conclusions clearly attributable to their author. AI assistance on this project is for repository administration and help with stuck points unless the owner explicitly asks for a bounded code contribution.
