# Chapter 2 — personal workspace

**Status:** prepared for Alex's first attempt; no personal implementation has been added.

The original Chapter 2 reference is at [`resources/books/llm/ch02/01_main-chapter-code/ch02.ipynb`](../../../resources/books/llm/ch02/01_main-chapter-code/ch02.ipynb). Write the personal attempt in [ch02.ipynb](ch02.ipynb). The book's exercise statement is the authority for any numbered exercise.

## Local environment

The environment is `work/llm/.venv` (Python 3.12.14). It was created with `uv venv --python 3.12 work/llm/.venv` and, for the opening Chapter 2 sections, installed with `uv pip install --python work/llm/.venv/bin/python ipykernel requests tiktoken`. Observed versions: ipykernel 7.4.0, requests 2.34.2, tiktoken 0.14.0. The environment is ignored by Git.

From the repository root, activate it with `source work/llm/.venv/bin/activate`. In VS Code, select the same Python executable for the interpreter and notebook kernel.
