# ANEMOI UV ENVIRONMENT
This is a simple Python UV environment setup for anemoi workframe. 


## 📦 Requirements

- Python >= 3.10
- [UV package manager](https://docs.astral.sh/uv/)

---

## ⚡ Install UV (if not already installed)
```bash
# Linux / macOS
curl -LsSf https://astral.sh/uv/install.sh | sh
# or, if using pip:
pip install uv
```
Verify installation:
```bash
uv --version
```
---

## 🌱 Create and set up a new environment

1. Clone the repository:
```bash
git clone <repo-url>
cd <repo-folder>
```
2. Sync the project environment using the lockfile:
```bash
uv sync
```
3. Activate the environment:
```bash
uv activate .venv
# or
source <repo-folder>/.venv/bin/activate
```

---

## 🔧 Making changes to the environment
1. Add a new package:
```bash
uv pip install <package-name>   # Installs a package into your current environment only 
uv add <package-name>   # Installs a package and adds it to your project dependencies
uv lock   # update lockfile
uv sync   # apply changes to environment
```
2. Remove a package:
```bash
uv remove <package-name>
uv lock
uv sync
```
3. Update a package:
```bash
uv pip install -U <package-name>
uv lock
uv sync
```
#### ⚠️ Always run uv lock after adding/updating/removing packages to keep uv.lock consistent.

---
📄 Notes

- The pyproject.toml file contains direct dependencies.
- The uv.lock file contains resolved versions for all dependencies.
- Do not commit local virtual environments (.venv/ or uv-envs/) to Git.

