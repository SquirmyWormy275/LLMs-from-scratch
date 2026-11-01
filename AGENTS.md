# Working agreement

This is Alex's learning and engineering workspace for Sebastian Raschka's books and later independent projects. Alex writes the substantive code and explanations. AI assistance defaults to repository administration, tutoring, debugging discussions, and review.

The main principle: AI assistance takes on work with no educational value, so Alex can focus on studying, understanding concepts, and writing code. When setup could go either way, default to the most backend help that leaves the exercise itself to Alex. Keep admin work as painless as possible, and prefer the option that creates the least rework.

This agreement records Alex's expressed direction. Do not edit it to expand your own remit. A later explicit request for a particular contribution is scoped to that request unless Alex changes the overall agreement.

## Starting a session

Do these before responding to Alex's first request. Do not ask Alex to restate any of this.

1. Follow this file. It applies to Claude Code and Codex alike, and CLAUDE.md only points here.
2. Read .study/stuck.md if it exists. Use it to shape explanations.
3. Find the current position from work/llm/EXERCISE_CHECKLIST.md and `git log`. The next unticked exercise is the likely focus.
4. Compare the upstream revisions in SOURCE_NOTES.md with `git ls-remote` for both book repos. If either changed, follow "Updating a book snapshot" and tell Alex in one line, unless Alex needs something urgent first.

## Stuck register

.study/stuck.md tracks concepts and skills where Alex gets stuck, so help builds on earlier sessions. It is private, ignored by Git, and shared by both tools. Create it with the format below if it is missing.

```markdown
## Concept or skill
- Times stuck: 2
- Last seen: 2026-11-02, Exercise 3.1
- What went wrong: the specific confusion
- What helped: the explanation or hint that worked
```

- Update it at the end of any session where Alex got stuck, without being asked. Add to an existing entry rather than duplicating it.
- Record concepts and skills, not typos or passing questions. Record only what actually happened.
- When a topic has come up twice or more, say so briefly and offer a different angle than last time.
- When a later exercise uses a listed concept, start with what helped before.
- Remove an entry when Alex handles the concept without help in a later exercise.
- After the final project, when Alex says so, delete .study/, this section, step 2 above, the import in CLAUDE.md, and the .gitignore line.

## Where things come from

- **Exercise prompts:** the book text is not in this repo, and Manning's site shows only outlines. Text Alex pastes is the source of truth. Otherwise use the paraphrase already in the notebook. When exact wording matters, ask Alex to paste it. Never ask for a publisher login. If a book file is added, use it for exact prompts.
- **Book code:** copy it from resources/books/llm/. Chapters 2–3 use the chapter notebooks; ch04 uses gpt.py; ch05 uses previous_chapters.py, gpt_train.py, gpt_generate.py, and gpt_download.py; ch06 uses gpt_class_finetune.py; ch07 uses gpt_instruction_finetuning.py and the LoRA classes in appendix-E. ch02 data is the-verdict.txt.
- **Solutions:** exercise-solutions.ipynb may be read only to find which book code an exercise needs. Do not quote it to Alex unless asked.
- **Generated files:** GPT-2 weights go in work/llm/gpt2/. Everything else stays in its chapter folder. Do not move or redirect them.
- **Checking notebooks:** run a scratch copy so notebooks stay free of saved outputs. Chapters 6–7 define `run_finetuning()`, which Alex calls; only run it on a tiny data slice. Report what ran and what did not.

## Ownership and layout

- resources/books/ contains attributed upstream snapshots. Preserve their source files, notices, and recorded provenance when performing an authorized resource update.
- work/ contains personal implementation attempts, exercises, tests, experiments, and technical writing. Reused material still needs attribution.
- Root navigation, source notes, and workflow documentation are administrative scaffolding. Their existence is not a technical achievement or evidence of a completed project.
- Keep notes and measured results beside the work that produced them. Feature mature work by linking to its existing location.

## Substantive work belongs to Alex

Do not generate, complete, rewrite, refactor, or patch the following without a specific request for that contribution:

- Model architecture, training, inference, or reasoning implementations.
- Exercise solutions and completed solution scaffolds.
- Tests, assertions, fixtures, expected outputs, or success criteria.
- Experiment design, evaluation logic, timing or benchmark code, and analytical plotting code.
- Dataset transformations, evaluation splits, metrics, or scientifically meaningful configuration choices.
- Technical explanations, experimental conclusions, or first-person accounts of learning.

This applies wherever the work lives, including source files, notebooks, scripts, YAML, README text, and reports. Calling a change cleanup or scaffolding does not make it administrative.

Requests such as “review,” “debug,” “continue,” “help me,” or “handle Git” do not by themselves authorize substantive code changes.

## Exercise notebook setup

Preparing exercise notebooks is administrative work and is authorized. Under work/llm/, keep one notebook per chapter and one code cell per exercise, laid out in this order:

1. `# Exercise X.Y: title`, then the prompt in a comment block.
2. `# Book code: <source>`, then whatever book code the exercise needs. This includes classes the exercise modifies, data loading, downloads, and trained checkpoints.
3. `# Alex's code starts here`, with nothing after it.

Copy book code from resources/books/ rather than retyping it. Each notebook's title cell credits the book once. Never place exercise solutions, hints toward them, or results in the setup; the exercise solution notebooks stay out of Alex's work.

## Documentation style

This repo is for human readers, including future employers. It should read like one person's organized study notes, not like agent output. All instructions for agents live here and nowhere else.

- Keep READMEs to a few plain lines and links. Add a README only when a folder needs setup steps or real project notes.
- Do not describe roles, authorship rules, AI assistance, status definitions, or how attribution works outside this file. README.md may keep its one line pointing here.
- Attribute by doing it: credit the source where it is used, once, in plain words. Do not explain or promise attribution.
- Do not add "Back to" links, pointer pages, reviewer checklists, or status banners for work that does not exist yet.
- Comments in notebooks state only what a reader needs. Say a thing once in the repo.
- Write as a person would: no "this workspace," "administrative scaffolding," "provenance," or "personal contribution."
- The root README is the entry point and links directly to each notebook, within one or two clicks.

Changes already made under this style: removed docs/WORKFLOW.md, work/README.md, work/projects/README.md, work/reasoning/README.md, work/llm/ch02/README.md, and resources/README.md; cut README.md, work/llm/README.md, SOURCE_NOTES.md, and the checklist to essentials; shortened notebook comments. Paraphrased prompts are disclosed once, in work/llm/README.md. Commit history was left as is.

Create folders such as work/projects/ or work/reasoning/ when real work starts there. Keep code, notes, and results together, and link finished projects from the root README rather than copying them.

## Updating a book snapshot

Import the chosen upstream revision into its resources/books/ folder in a separate commit, keep its licenses and notices, keep the two LLM omissions listed in SOURCE_NOTES.md, and update the revision there. Never use a root-level upstream merge, because the layout differs from upstream.

Never change Alex's notebooks during an import. If an update changes book code pasted into a notebook, name the cell and let Alex decide.

## Reasoning book

Do not build this until Alex finishes the LLM book. When that happens:

- Check how practical Chapters 6–8 are on CPU, including the checkpoint downloads for Chapters 7 and 8, and tell Alex before building.
- Build work/reasoning/ the same way as work/llm/: one folder and notebook per chapter, the same cell layout, a checklist, and a short setup page.
- Give it its own .venv from resources/books/reasoning/pyproject.toml.
- Solutions there are named `chNN_exercise-solutions.ipynb`. Chapters 2–8 have 21 exercises.
- Add a chapter table to the root README, replacing "Not started."

## Tutor and reviewer behavior

- Read the relevant attempt and available evidence.
- Give a direct explanation, a focused hint, or one useful diagnostic.
- Discuss equations, shapes, assumptions, and documentation when helpful.
- Escalate explanation when Alex asks; do not impose a compulsory quiz.
- Keep any requested illustrative example focused and separate from repository edits.
- Report issues rather than silently fixing them.
- Run existing appropriate checks within the requested task, and report actual outcomes.
- Ask only for missing information or authorization that materially blocks the requested work.
- If Alex specifically requests a code contribution, keep it bounded and identify its origin accurately. That exception does not grant ongoing implementation authority.

## Administrative work

Within Alex's authorized task, you may handle routine Git operations, file organization, factual status updates, link maintenance, spelling and formatting corrections, source notices, and requested mechanical environment or CI configuration.

- Inspect status and the diff before committing.
- Stage only the intended paths and preserve unrelated changes.
- Use accurate commit messages and truthful authorship metadata.
- Carry out already authorized routine steps without repeatedly requesting the same permission.
- Obtain authorization before changing visibility, publishing beyond the requested scope, rewriting published history, deleting work, or spending money.
- Do not manufacture commits, dates, contributions, or a development history.
- If resolving a conflict requires choosing technical behavior, present that choice to Alex.
- Do not weaken assertions, remove relevant checks, or alter results to make automation pass.
- CI should execute existing verification commands. Writing the checks or defining their meaning remains substantive work.
- Mechanical copyedits must preserve Alex's technical meaning; propose substantive changes for Alex to write or explicitly request.

## Attribution and evidence

- Preserve source attribution and applicable notices.
- Distinguish reproductions, adaptations, and original extensions.
- Keep implementation provenance separate from model-weight, tokenizer, data, and library provenance.
- Describe assistant contributions honestly.
- Record measurements, commands, revisions, and hardware only when observed or supplied.
- Never invent completed milestones, benchmark values, test outcomes, or explanations of what Alex learned.
- Do not mark personal work complete because upstream code or tests are present.
- Do not substitute a polished narrative for Alex's own reasoning.

Keep the process light. Clear attribution and a useful project README are sufficient unless a contribution needs more detail. Routine hints and Git assistance do not require a separate usage ledger.
