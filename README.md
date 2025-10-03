# Notes on Machine Learning (Jupyter Book)

## Technical Overview

The notes are organized in a [Jupyter Book 2](https://next.jupyterbook.org/).
The required Python environment is managed by [uv](https://docs.astral.sh/uv/).
Local development uses [JupyterLab](https://jupyter.org/) with the extensions
[Jupytext](https://jupytext.readthedocs.io/) and
[jupyterlab-myst](https://github.com/jupyter-book/jupyterlab-myst).

The repository's root directory contains the following:

- `.git/` - Git repository for the project
- `.github/` - configuration for publishing to GitHub Pages
- `.venv/` - Python virtual environment for the project, listed in `.gitignore`
- `_build/` - Jupyter Book build output
- `src/` - the contents of the notes
- `.gemini` - configuration for gemini-cli
- `.gitignore`, `.gitmodules` - Git repository configuration
- `.python-version` - `uv` python version requirement
- `AGENTS.md` - instructions for AI coding agents
- `myst.yml` - MyST Markdown Document Engine configuration
- `pyproject.toml` - `uv` workspaces configuration
- `README.md` - this file
- `uv.lock` - `uv` dependencies versions

The book contents is in `.md` files under the `src/` directory. The files follow
the [MyST (Markedly Structured Text)](https://mystmd.org/spec) Markdown dialect.

Jupyter Book 2 is often confused with
[Jupyter Book 1](https://jupyterbook.org/intro.html). When reading guides or
documentation, check the Jupyter Book version that they apply to. Jupyter Book 1
parses MyST Markdown into Sphinx, and delegates to the Sphinx engine, whereas
Jupyter Book 2 uses the [MyST Markdown Document Engine](https://mystmd.org/) to
generate documents directly.

## Common commands

* Build the book: `uv run jupyter book build --all`
* Start a local book server: `uv run jupyter book start`
* Start a Jupyter Lab local server: `uv run jupyter lab`
* Add a Python dependency, such as Jupyter extension: `uv add jupyter-extension`
