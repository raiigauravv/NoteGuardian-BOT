# NoteGuardian BOT 🛡️

Automated PR review for Data Science & ML repos: flags notebook outputs, data files, and model metrics in a single, recruiter-friendly comment.

---

## Features
- Detects and flags Jupyter notebooks with outputs, non-default kernels, large cells, or out-of-order execution.
- Flags added/changed data files (csv, parquet, json, xlsx, etc).
- Optionally includes model metrics from `metrics.json`.
- Posts a single, well-formatted PR comment with actionable tips.
- Easy to integrate as a GitHub Action.

---

## Quick Start

### 1. Add to your repo
- Copy the following files from this repo:
  - `.github/workflows/pr-bot.yml`
  - `scripts/pr_bot.py`
  - `requirements.txt`

### 2. Enable GitHub Actions
- Make sure GitHub Actions are enabled in your repo settings.

### 3. Open a Pull Request
- The bot will automatically analyze PRs and post a comment with notebook/data file status and metrics.

---

## Usage

- **Notebook checks:**
  - Output cells present
  - Non-default kernel
  - Large code/markdown cells
  - Out-of-order execution counts
- **Data file detection:**
  - Flags files with extensions: `.csv`, `.parquet`, `.json`, `.xlsx`, `.feather`, `.pkl`, `.tsv`, `.h5`, `.yaml`, `.yml`, `.xml`
- **Metrics:**
  - If your workflow generates a `metrics.json`, it will be included in the comment.

---

## Local Testing

```sh
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
pytest tests/
```

---

## Contributing

Pull requests are welcome! Please open an issue to discuss major changes first.

---

## License

MIT License

---

