<!--
  TEMPLATE: Python library README.
  Copy to a repo's README.md and replace every {{TOKEN}}. Keep section headers
  plain (no emoji). Migrate the repo's existing accurate content into these
  sections — preserve substance, move deep reference material into docs/.

  Tokens:
    {{DISPLAY_NAME}}     Package name, e.g. "pyintellicenter"
    {{TAGLINE}}          One sentence describing the library
    {{REPO}}             GitHub repo slug (usually same as package)
    {{PYPI}}             PyPI distribution name, e.g. "pyintellicenter"
    {{CI_WORKFLOW}}      Primary CI workflow filename, e.g. "ci.yml" (or remove the CI badge)
    {{LICENSE_NAME}}     "MIT" or "GPL-3.0"
    {{CROSSLINK_REPO}}   Companion Home Assistant integration repo slug
    {{CROSSLINK_NAME}}   Companion Home Assistant integration name
-->
# {{DISPLAY_NAME}}

{{TAGLINE}}

[![PyPI Version][pypi-shield]][pypi]
[![Python Versions][pyversions-shield]][pypi]
[![License][license-shield]](LICENSE)
[![CI][ci-shield]][ci]
[![GitHub Sponsors][sponsors-shield]][sponsors]
[![Ko-fi][kofi-shield]][kofi]

## What It Does

<!-- 2-4 sentences: what the library does and who it is for. -->

## Features

<!-- Bulleted list of concrete capabilities. -->

## Installation

See **[INSTALL.md](INSTALL.md)** for the complete guide.

```bash
pip install {{PYPI}}
# or
uv add {{PYPI}}
```

Requires Python 3.13+.

## Quick Start

<!-- A minimal, runnable example (authenticate -> do one useful thing). -->

```python
# minimal example
```

## Usage

<!-- The common workflows, with short code snippets. Link to docs/ for depth. -->

## API Reference

Full API reference lives in [docs/](docs/). Key entry points:

<!-- Brief table or list of the main classes/functions. -->

## Development

See [docs/DEVELOPMENT.md](docs/DEVELOPMENT.md). In short:

```bash
git clone https://github.com/joyfulhouse/{{REPO}}.git
cd {{REPO}}
uv sync
uv run pytest
uv run ruff check
uv run mypy
```

## Support

- **Issues:** <https://github.com/joyfulhouse/{{REPO}}/issues>
- **PyPI:** <https://pypi.org/project/{{PYPI}}/>

## Support Development

If this library is useful to you, please consider supporting its development:

- [GitHub Sponsors][sponsors]
- [Ko-fi][kofi]

## License

This project is licensed under the **{{LICENSE_NAME}}** License — see
[LICENSE](LICENSE) for details.

## Related Projects

- [{{CROSSLINK_NAME}}](https://github.com/joyfulhouse/{{CROSSLINK_REPO}}) — the
  Home Assistant integration built on this library.

<!-- Badge links -->
[pypi-shield]: https://img.shields.io/pypi/v/{{PYPI}}.svg?style=for-the-badge
[pypi]: https://pypi.org/project/{{PYPI}}/
[pyversions-shield]: https://img.shields.io/pypi/pyversions/{{PYPI}}.svg?style=for-the-badge
[license-shield]: https://img.shields.io/github/license/joyfulhouse/{{REPO}}.svg?style=for-the-badge
[ci-shield]: https://img.shields.io/github/actions/workflow/status/joyfulhouse/{{REPO}}/{{CI_WORKFLOW}}?style=for-the-badge&label=CI
[ci]: https://github.com/joyfulhouse/{{REPO}}/actions
[sponsors-shield]: https://img.shields.io/badge/sponsor-GitHub-EA4AAA.svg?style=for-the-badge&logo=githubsponsors&logoColor=white
[sponsors]: https://github.com/sponsors/btli
[kofi-shield]: https://img.shields.io/badge/Ko--fi-donate-FF5E5B.svg?style=for-the-badge&logo=ko-fi&logoColor=white
[kofi]: https://ko-fi.com/bryanli
