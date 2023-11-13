# Repository Template

Checklist after creating a new repository from this template:

- Go through `pyproject.toml` and fill in the `PLACEHOLDER`'s. Note that:
  - `GH_TOKEN` is only needed if you want to trigger a semantic release locally. It is not needed for doing a release on GitHub Actions (as per `semantic_release.yaml`).
  - If you wish to publish to Test PyPI, ensure that `name` under `[project]` is available on Test PyPI. 
- If you wish to publish to Test PyPI, as specified in the `semantic_release.yaml` GitHub Action workflow, you must:
  - Create an account on Test PyPI (you only need to do this once).
  - In your Test PyPI account, create an API token under "Account Settings". This will start with `pypi-`. Copy it. 
  - In your GitHub repository, paste the above API token into an **action secret** named `TESTPYPI_API_TOKEN` (this secret is used in `semantic_release.yaml`). This is done in "Settings" -> "Secrets and variables" -> "Actions". 
- Update the `name:` field in `environment.yaml`.
- Update dependencies in `environment.yaml` and `requirements.txt`.
- Update the "Setup" section below.

## Setup

Clone the repository:

```shell
git clone <UPDATE THIS>
```

Create a conda environment:

```shell
conda env create --file environment.yaml
```

Activate the conda environment:

```shell
conda <UPDATE THIS>
```

Install the local package in editable mode:

```shell
pip install --editable .
```

## References

