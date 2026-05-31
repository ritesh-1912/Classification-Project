# Classification Project

This repository stores the log classification application inside the `classification_logs/` folder. To keep the code folder visible on GitHub's main page, this root README provides quick links to code files and the folder structure.

Quick links
- Classification folder: [classification_logs](classification_logs/)
- Classify script: [classification_logs/classify.py](classification_logs/classify.py)
- Main runner: [classification_logs/main.py](classification_logs/main.py)
- Server: [classification_logs/server.py](classification_logs/server.py)
- Processors:
  - [classification_logs/processor_regex.py](classification_logs/processor_regex.py)
  - [classification_logs/processor_bert.py](classification_logs/processor_bert.py)
  - [classification_logs/processor_llm.py](classification_logs/processor_llm.py)
- Requirements: [classification_logs/requirements.txt](classification_logs/requirements.txt)

Folder structure (top-level)

- `classification_logs/` — application code, README, and local `.gitignore`
- `models/` — serialized model artifacts (e.g., `log_classifier.joblib`)
- `resources/` — example inputs and outputs
- `training/` — training notebooks and datasets

Notes
- GitHub displays files in the repository root. If you want the `.py` files shown directly on the repository front page file list, move them to the repo root. I can do that for you, but keeping them inside `classification_logs/` maintains a tidy layout.
- The `classification_logs/README.md` contains detailed setup and usage instructions.
