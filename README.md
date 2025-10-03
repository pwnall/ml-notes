# Notes on Machine Learning (Jupyter Book)

## Technical Overview

The notes are organized in a [Jupyter Book 2](https://next.jupyterbook.org/).
The required Python environment is managed by [uv](https://docs.astral.sh/uv/).

Jupyter Book 2 is often confused with
[Jupyter Book 1](https://jupyterbook.org/intro.html). When reading guides or
documentation, check the Jupyter Book version that they apply to. Jupyter Book 2
is built on the [MyST Markdown Document Engine](https://mystmd.org/), whereas
Jupyter Book 1 is buily on the Sphinx engine. Both versions use the MyST
Markdown (Markedly Structured Text Markdown) dialect.

The repository's root directory contains the following:

- `.git/` - Git repository for the project
- `.github/` - configuration for publishing to GitHub Pages
- `.venv/` - Python virtual environment for the project, listed in `.gitignore`
- `_build/` - Jupyter Book build output
- `src/` - the contents of the notes
- `.gitignore`, `.gitmodules` - Git repository configuration
- `.python-version` - `uv` python version requirement
- `myst.yml` - MyST Markdown Document Engine configuration
- `pyproject.toml` - `uv` workspaces configuration
- `uv.lock` - `uv` dependencies versions

The book contents is in `.md` files under the `src/` directory. The files follow
the [MyST (Markedly Structured Text)](https://mystmd.org/spec) format.

## Common commands

* Build the book: `uv run jupyter book build --all`
* Start a local server: `uv run jupyter book start`
