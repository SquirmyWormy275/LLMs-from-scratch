# Chapter 2 — personal workspace

**Status:** workspace prepared; no personal implementation has been committed.

Read [Chapter 2 in the book](https://livebook.manning.com/book/build-a-large-language-model-from-scratch/chapter-2) for the numbered exercise prompts. Exercise 2.1 appears in section 2.5, "Byte pair encoding." The [original Chapter 2 companion notebook](../../../resources/books/llm/ch02/01_main-chapter-code/ch02.ipynb) contains chapter code, but not the exercise statement. Write the personal attempt in [ch02.ipynb](ch02.ipynb).

## Local environment

The environment is `work/llm/.venv` (Python 3.12.14). It was created with `uv venv --python 3.12 work/llm/.venv` and, for the opening Chapter 2 sections, installed with `uv pip install --python work/llm/.venv/bin/python ipykernel requests tiktoken`. Observed versions: ipykernel 7.4.0, requests 2.34.2, tiktoken 0.14.0. The environment is ignored by Git.

From the repository root, activate it with `source work/llm/.venv/bin/activate`. In VS Code, select the same Python executable for the interpreter and notebook kernel.
