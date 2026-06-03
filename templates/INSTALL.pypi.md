<!--
  TEMPLATE: Python library INSTALL guide.
  Copy to a repo's INSTALL.md and replace every {{TOKEN}}.
  Tokens: {{DISPLAY_NAME}}, {{REPO}}, {{PYPI}}
-->
# Installing {{DISPLAY_NAME}}

## Requirements

- Python 3.13 or newer.

## Install from PyPI

```bash
pip install {{PYPI}}
```

Or with [uv](https://docs.astral.sh/uv/):

```bash
uv add {{PYPI}}
```

## Install from Source

```bash
git clone https://github.com/joyfulhouse/{{REPO}}.git
cd {{REPO}}
uv sync
```

This installs the package with its development dependencies into a local virtual
environment.

## Verify the Installation

```bash
python -c "import {{PYPI}}; print({{PYPI}}.__version__)"
```

You should see the installed version printed with no import errors. (If the
distribution name contains a hyphen, the import name uses an underscore instead.)

## Next Steps

See the [README](README.md#quick-start) for a quick-start example and usage
guide.
