<!-- TEMPLATE: docs/DEVELOPMENT.md -->
# Development

How to set up a development environment for {{DISPLAY_NAME}}.

## Prerequisites

- Python 3.13+ and [`uv`](https://docs.astral.sh/uv/).

## Setup

```bash
git clone https://github.com/joyfulhouse/{{REPO}}.git
cd {{REPO}}
uv sync
```

## Quality Checks

```bash
uv run pytest          # tests
uv run ruff check      # lint
uv run ruff format     # format
uv run mypy            # type check
```

Run all of these before opening a pull request. See
[CONTRIBUTING](https://github.com/joyfulhouse/.github/blob/main/CONTRIBUTING.md)
for the contribution workflow.

## Releasing

<!-- Tag/version bump and publish steps (PyPI for libraries, release for HA). -->
