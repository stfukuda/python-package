# python-package Copier Template

`python-package` is a Copier template that bootstraps a modern Python package with a single command. It ships with `uv` for dependency management, Ruff + mypy + Bandit for static analysis, pytest, Dev Container support, and PreK hooks so you can go from `copier copy` to CI-ready code immediately.

## Prerequisites

- Copier CLI (`pipx install copier`, `brew install copier`, etc.)

## Usage

1. Change into the parent directory where you want the new project to live.
2. Run the command below (replace `my-new-project` with any folder name you prefer):

   ```bash
   copier copy gh:stfukuda/python-package my-new-project
   ```

3. Answer the prompts. Copier creates a directory named after `{{ project_slug }}` and fills it with the full project layout. After generation, open the repo in the Dev Container and run `just setup` manually to sync dependencies (see the generated README for details).

## What’s Included

- Src layout with `pyproject.toml`, README, sample tests, docs scaffolding, `.env`, and `py.typed`
- Justfile workflows (`just setup`, `just check`, `just test`, etc.) powered by `uv` + `PreK`
- Ruff + mypy + Bandit + pytest (coverage + xdist) wired into both Justfile and CI
- Dev Container image bootstrapped with `uv`, `just`, `prek`, and all template tooling pre-installed
- GitHub Actions for lint/test/release plus `hatch-vcs` tag-driven versioning

## Updating an Existing Project

When the template evolves, run the following inside a generated project to pull in changes:

```bash
copier update
```

Review and merge the suggested diff.

## License

This template is distributed under the [MIT License](LICENSE).
