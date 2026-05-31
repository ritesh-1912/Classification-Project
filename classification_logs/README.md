**Project Overview**

This folder contains the primary application code for a small text log classification project. It demonstrates preprocessing, model inference, and a minimal server for classifying log entries. It includes utilities for rule-based, BERT-based, and LLM-based processing as well as a trained model artifact for quick evaluation.

**Prerequisites**
- **Python**: 3.8+ recommended.
- **Virtual environment**: it's recommended to use `venv` or a similar tool to isolate dependencies.

**Quick Setup**
1. Create and activate a virtual environment (from the repository root):

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Verify the environment and run a quick script (examples below).

**Folder Layout (inside this directory)**
- `classify.py`: High-level classification entrypoint utilities.
- `main.py`: CLI or example runner to exercise classification flows.
- `server.py`: Minimal server exposing classification endpoints (if present).
- `processor_regex.py`: Rule-based preprocessing utility.
- `processor_bert.py`: BERT-based processing (feature extraction / tokenization helpers).
- `processor_llm.py`: LLM-based processing helper functions.
- `requirements.txt`: Python dependencies for the project.
- `.venv/`: Optional virtualenv directory (not committed usually).

**Usage**

- Run a quick classification script (example):

  ```bash
  # from repository root with venv activated
  python classification_logs/main.py
  ```

- Run the server (if implemented):

  ```bash
  python classification_logs/server.py
  ```

- Use the `classify.py` utilities to run classification on a CSV input and write results to `resources/output.csv`:

  ```bash
  python classification_logs/classify.py --input resources/test.csv --output resources/output.csv
  ```

  (Adjust CLI flags as implemented in the script; open the file to confirm available options.)

**Model & Data Notes**
- The project includes a pre-trained model at `../models/log_classifier.joblib`. Replace this file with your own trained model if you retrain using the notebook in `../training/`.
- Training experiments and data preparation are located in `../training/training.ipynb` and `../training/dataset/`.

**Development Tips**
- Keep your virtual environment inside `classification_logs/.venv` or at repository root `.venv` and add it to `.gitignore` to avoid committing large environment files.
- When adding or updating dependencies, pin versions in `requirements.txt` and run `pip freeze > requirements.txt` from the activated environment.

**Testing / Validation**
- There are no automated tests included by default. To validate changes:
  - Run `python main.py` with sample inputs.
  - Inspect `resources/output.csv` and `resources/test.csv` for expected results.

**Extending the Project**
- Replace processing modules or add new processors in this folder (for example, add a new `processor_custom.py`).
- Add a training pipeline that exports an updated model under `../models/` and include a small reproducible script in `../training/`.

If you want the README expanded with examples, API signatures, or sample outputs, tell me what to include.
