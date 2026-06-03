# JoyfulHouse Open-Source Standards

The conventions every `joyfulhouse` open-source repository follows. This is the
source of truth; the files in [`templates/`](templates/) and
[`licenses/`](licenses/) implement it. New repositories should be set up to match
this document (see [TEMPLATE.md](TEMPLATE.md) for the quick procedure).

## Project Pairing

Most projects ship as a pair: a **Home Assistant integration** and the
**Python library** it is built on. They cross-link each other in their READMEs.

| Project | Home Assistant integration | Python library |
|---|---|---|
| Moogo | [`moogo`](https://github.com/joyfulhouse/moogo) | [`pymoogo`](https://github.com/joyfulhouse/pymoogo) |
| IntelliCenter | [`intellicenter`](https://github.com/joyfulhouse/intellicenter) | [`pyintellicenter`](https://github.com/joyfulhouse/pyintellicenter) |
| Thermacell | [`thermacell_liv`](https://github.com/joyfulhouse/thermacell_liv) | [`pythermacell`](https://github.com/joyfulhouse/pythermacell) |
| EG4 | [`eg4_web_monitor`](https://github.com/joyfulhouse/eg4_web_monitor) | [`pylxpweb`](https://github.com/joyfulhouse/pylxpweb) |

## Licensing

- **Default license is MIT** for originally-authored projects.
- **Derived works preserve their upstream license.** `intellicenter` is
  **GPL-3.0** because it derives from
  [@jlvaillant's integration](https://github.com/jlvaillant/intellicenter); its
  copyleft must be preserved and upstream authors must stay credited in the
  README. Do not relicense derived code without permission from all copyright
  holders.
- **Copyright holder is always `JoyfulHouse Real Estate LLC`.**
- **Copyright line format:** `Copyright (c) <first-year>-<current-year> JoyfulHouse Real Estate LLC`,
  where `<first-year>` is the repo's first-publication year.
- Canonical license texts live in [`licenses/`](licenses/). The MIT text uses
  `{{YEARS}}` and `{{HOLDER}}` placeholders.
- Keep the license consistent across metadata: `LICENSE`, the `pyproject.toml`
  `license` field (SPDX: `MIT` or `GPL-3.0-only`), and HA `manifest.json`.

## README

- **Clean and professional. No emoji in section headers.**
- Title is the human-readable project name, followed by a one-sentence tagline,
  then a single badge row, then the body.
- **Home Assistant badge row:** Release · License · HACS · CI · Quality Scale ·
  Project Maintenance · GitHub Sponsors · Ko-fi.
- **Python badge row:** PyPI Version · Python Versions · License · CI · GitHub
  Sponsors · Ko-fi.
- **HA section order:** What It Does → Features → Prerequisites → Installation
  (brief, links `INSTALL.md`) → Configuration → Supported Equipment →
  Automation Examples → Troubleshooting → Development → Support → Support
  Development → License → Credits.
- **Library section order:** What It Does → Features → Installation (brief, links
  `INSTALL.md`) → Quick Start → Usage → API Reference → Development → Support →
  Support Development → License → Related Projects.
- The README is a scannable overview. Deep reference material belongs in
  [`docs/`](#docs-folder), not the README.
- Each integration links its Python library and vice versa.

## INSTALL.md

Every repo has an `INSTALL.md` with the full installation guide; the README keeps
only a short snippet that links to it.

- **HA:** HACS (with a `my.home-assistant.io` one-click link) and manual
  installation, restart, add-integration, verify, update, troubleshooting.
- **Library:** `pip install` and `uv add`, from-source install, verify import,
  next steps. Requires Python 3.13+.

## CHANGELOG.md

- Every repo has a `CHANGELOG.md` following
  [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and
  [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
- An `## [Unreleased]` section is always present at the top.
- Use `### Added` / `### Changed` / `### Fixed` / `### Removed` subsections.

## docs/ Folder

A consistent taxonomy. User-facing docs in the canonical set; everything internal
in `docs/claude/`.

- `docs/README.md` — index of the folder.
- `docs/ARCHITECTURE.md` — design and structure.
- `docs/CONFIGURATION.md` *(HA)* or `docs/USAGE.md` *(library)* — full guide.
- `docs/TROUBLESHOOTING.md` — problems and fixes.
- `docs/DEVELOPMENT.md` — contributor setup and quality checks.
- `docs/api/` *(library, where an API reference exists)*.
- `docs/claude/` — internal design notes, session logs, and process artifacts
  (CI analyses, verification reports, release notes, plans, exploratory
  scripts). Not user-facing.
- Project-specific reference docs (data mappings, protocol notes) are retained
  and linked from `docs/README.md`.

## Community Health & Metadata

- **`FUNDING.yml` in every repo** (`github: btli`, `ko_fi: bryanli`); donation
  links must be visible per repo. The org-level `FUNDING.yml` here is a backstop.
- **`CONTRIBUTING.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md` are org-wide
  defaults** in this repo and apply to every project automatically. A repo adds
  its own only when it needs project-specific content (parameterized templates
  are in `templates/`).
- **CODEOWNERS is `@btli` everywhere.** `.github/CODEOWNERS` is `* @btli`; HA
  `manifest.json` uses `"codeowners": ["@btli"]`.
- Preserve existing `dependabot.yml`, `ISSUE_TEMPLATE`, and workflows.

## Toolchain

- **Python** projects use [`uv`](https://docs.astral.sh/uv/) and target Python
  3.13+.
- **JavaScript/TypeScript** projects use [`bun`](https://bun.sh).
- Linters and type checks are never disabled to silence a finding; fix the root
  cause.
