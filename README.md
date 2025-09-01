# MongoDB GenAI Developer Day – Notebooks

This repository contains the Jupyter notebooks and supporting assets used in MongoDB’s GenAI Developer Day workshops. Use this repo to explore vector search, Retrieval-Augmented Generation (RAG), and AI Agents workflows locally at your own pace.

## Workshops (Self-Paced)
- Vector Search: Beginner to Pro — https://mongodb-developer.github.io/vector-search-lab/
- Building RAG Applications with MongoDB — https://mongodb-developer.github.io/ai-rag-lab/
- The A to Z of Building AI Agents — https://mongodb-developer.github.io/ai-agents-lab/

## Repository Contents
- `notebooks/`: Jupyter notebooks for each lab
- `data/`: Sample datasets used by notebooks (do not commit secrets)
- `requirements.txt`: Python dependencies for local runs
- `.devcontainer/`: Dev Container definition for a repeatable environment
- `.github/`: CI and configuration for GitHub workflows (if applicable)

## Prerequisites
- Python 3.10+ (3.11 recommended)
- pip (or uv/pipx/poetry if preferred)
- A MongoDB Atlas cluster or local MongoDB if you want to run end‑to‑end examples
- Optional: Docker + VS Code Dev Containers extension for one‑click setup

## Quick Start
1) Create and activate a virtual environment

   macOS/Linux:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

   Windows (PowerShell):
   ```powershell
   py -3 -m venv .venv
   .venv\\Scripts\\Activate.ps1
   ```

2) Install dependencies
```bash
pip install -r requirements.txt
```

3) (Optional) Set environment variables in a local `.env` file
```bash
cp .env .env.example || true
```
Edit `.env` and provide any keys or connection strings needed by notebooks. The `.env` file is ignored by git.

4) Launch Jupyter
```bash
jupyter lab
```
Open the notebooks under `notebooks/` and follow the instructions in each workshop.

## Using Dev Containers (Optional)
If you use VS Code with the Dev Containers extension:
- Open this folder in VS Code
- When prompted, “Reopen in Container”
- The container will install dependencies and start a ready‑to‑use environment

## Sensitive Files and Data
- `.env`, API keys, and credentials are ignored via `.gitignore`
- Avoid committing large datasets or private data. Place large files under `data/` and consider adding patterns to `.gitignore` if needed

## Troubleshooting
- Kernel or dependency issues: recreate the virtual environment and reinstall requirements
- Connection issues: verify your MongoDB URI and network access
- Notebook checkpoints: these are ignored via `.gitignore` (`.ipynb_checkpoints`)

## License and Attribution
These materials are adapted from MongoDB Developer workshops. Refer to the individual workshop pages for additional context and attributions.

## Upstream
Primary source repository: https://github.com/mongodb-developer/genai-devday-notebooks
This fork tracks upstream via the `upstream` remote. To sync latest changes:
```bash
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```
