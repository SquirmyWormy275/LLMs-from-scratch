# LLM book setup

```bash
uv venv --python 3.12 work/llm/.venv
source work/llm/.venv/bin/activate
uv pip install --torch-backend cpu 'torch>=2.2.2'
uv pip install ipykernel requests tiktoken numpy matplotlib tqdm pandas tensorflow
```

Tested with Python 3.12.14, torch 2.15.0, tiktoken 0.14.0, and tensorflow 2.21.0.

Select `work/llm/.venv` as the notebook kernel and run the setup cell at the top of each notebook first.

- Chapter 5 trains its model on the first run, about 10 minutes on CPU, then reuses the saved file.
- GPT-2 weights download to `work/llm/gpt2/`.
- Chapters 6 and 7 train when you call `run_finetuning()`.

Exercise prompts are paraphrased, so check the book for the exact wording.
