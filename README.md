# python-package Copier Template

`python-package` is a Copier template that bootstraps a modern Python package with a single command. It ships with `uv` for dependency management, Ruff + mypy + Bandit for static analysis, pytest, Dev Container support, and pre-commit hooks so you can go from `copier copy` to CI-ready code immediately.

## Prerequisites

- Python 3.10+
- Copier CLI (`brew install copier`, etc.)

## Usage

1. Change into the parent directory where you want the new project to live.
2. Run the command below (replace `my-new-project` with any folder name you prefer):

   ```bash
   copier copy gh:stfukuda/python-package my-new-project
   ```

3. Answer the prompts. Copier creates a directory named after `{{ project_slug }}` and fills it with the full project layout. After generation, follow the new project’s `README.md` to finish setup.

## What’s Included

- `uv` + `Justfile` workflows (`just setup`, `just check`, `just test`, `just build`, etc.)
- Ruff formatting/linting, mypy type checking, Bandit security scans, pytest with coverage + xdist
- Dev Container configuration (VS Code + Dev Container CLI) and pre-commit hooks
- GitHub Actions workflows for linting, testing, and releasing to PyPI / TestPyPI via tags
- `hatch-vcs`-powered versioning so package versions come directly from your Git tags
- `src/{{ module_name }}` package layout, `py.typed`, `.env` example, and other best-practice defaults

## Updating an Existing Project

When the template evolves, run the following inside a generated project to pull in changes:

```bash
copier update
```

Review and merge the suggested diff.

## License

This template is distributed under the [MIT License](LICENSE).
