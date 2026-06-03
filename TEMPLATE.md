# Templates Index

Every document template for JoyfulHouse open-source repositories. Read
[STANDARDS.md](STANDARDS.md) for the conventions these implement.

## Template Files

| Template | Applies to | Becomes (in target repo) |
|---|---|---|
| [`templates/README.hacs.md`](templates/README.hacs.md) | HA integration | `README.md` |
| [`templates/README.pypi.md`](templates/README.pypi.md) | Python library | `README.md` |
| [`templates/INSTALL.hacs.md`](templates/INSTALL.hacs.md) | HA integration | `INSTALL.md` |
| [`templates/INSTALL.pypi.md`](templates/INSTALL.pypi.md) | Python library | `INSTALL.md` |
| [`templates/CHANGELOG.md`](templates/CHANGELOG.md) | both | `CHANGELOG.md` |
| [`templates/CONTRIBUTING.md`](templates/CONTRIBUTING.md) | both *(override only)* | `CONTRIBUTING.md` |
| [`templates/SECURITY.md`](templates/SECURITY.md) | both *(override only)* | `SECURITY.md` |
| [`templates/docs/`](templates/docs/) | both | `docs/` |
| [`licenses/MIT.txt`](licenses/MIT.txt) | MIT projects | `LICENSE` |
| [`licenses/GPL-3.0.txt`](licenses/GPL-3.0.txt) | derived (GPL) projects | `LICENSE` |
| [`FUNDING.yml`](FUNDING.yml) | every repo | `.github/FUNDING.yml` |

`CONTRIBUTING.md`, `SECURITY.md`, and `CODE_OF_CONDUCT.md` apply org-wide from
this repo; only add the per-repo template versions when a project needs its own.

## Placeholder Legend

Replace every token when instantiating a template.

| Token | Meaning | Example |
|---|---|---|
| `{{DISPLAY_NAME}}` | Human-readable project name | `Pentair IntelliCenter` |
| `{{TAGLINE}}` | One-sentence description | `Local control of Pentair IntelliCenter pools.` |
| `{{REPO}}` | GitHub repo slug | `intellicenter` |
| `{{DOMAIN}}` | HA integration domain | `intellicenter` |
| `{{PYPI}}` | PyPI distribution name | `pyintellicenter` |
| `{{LICENSE_NAME}}` | License identifier | `MIT` / `GPL-3.0` |
| `{{YEARS}}` | Copyright year range | `2024-2026` |
| `{{HOLDER}}` | Copyright holder | `JoyfulHouse Real Estate LLC` |
| `{{CI_WORKFLOW}}` | Primary CI workflow filename | `ci.yml` |
| `{{QUALITY_TIER}}` | HA quality scale tier | `Platinum` |
| `{{MIN_HA_VERSION}}` | Minimum Home Assistant version | `2024.1.0` |
| `{{CROSSLINK_REPO}}` | Companion repo slug | `pyintellicenter` (from `intellicenter`) |
| `{{CROSSLINK_NAME}}` | Companion repo display name | `pyintellicenter`; reverse direction is `Pentair IntelliCenter` |

> `{{YEARS}}` and `{{HOLDER}}` appear only in `licenses/MIT.txt`; the Markdown
> templates do not use them.

## Applying to a Repository

1. **LICENSE** — copy the right text from `licenses/`. For MIT, set the copyright
   line to `Copyright (c) {{YEARS}} {{HOLDER}}` (i.e. the year range and
   `JoyfulHouse Real Estate LLC`). Keep GPL repos GPL. Align the
   `pyproject.toml` `license` SPDX and HA `manifest.json`.
2. **`.github/FUNDING.yml`** — copy `FUNDING.yml`.
3. **`.github/CODEOWNERS`** — `* @btli`. For HA repos also set
   `manifest.json` `"codeowners": ["@btli"]`.
4. **README.md** — instantiate the matching README template; migrate the repo's
   existing accurate content into the standard sections; fill all tokens; add the
   cross-link to the paired repo.
5. **INSTALL.md** — instantiate the matching INSTALL template; move long install
   detail out of the README.
6. **CHANGELOG.md** — normalize the header to the `templates/CHANGELOG.md` form;
   ensure `## [Unreleased]` exists. Create it if missing.
7. **docs/** — ensure the canonical files exist (`docs/README.md` index linking
   the rest); move internal artifacts into `docs/claude/`; keep and link
   project-specific reference docs.
8. **Verify** — `README.md`, `INSTALL.md`, `CHANGELOG.md`, `LICENSE`,
   `.github/FUNDING.yml`, `.github/CODEOWNERS` all present; copyright holder is
   `JoyfulHouse Real Estate LLC`; no emoji in headers; badge links resolve.
