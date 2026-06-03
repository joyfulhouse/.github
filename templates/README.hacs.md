<!--
  TEMPLATE: Home Assistant integration README.
  Copy to a repo's README.md and replace every {{TOKEN}}. Keep section headers
  plain (no emoji). Migrate the repo's existing accurate content into these
  sections — preserve substance, drop emoji headers and duplication.

  Tokens:
    {{DISPLAY_NAME}}     Human name, e.g. "Pentair IntelliCenter"
    {{TAGLINE}}          One sentence describing what it does
    {{REPO}}             GitHub repo slug, e.g. "intellicenter"
    {{DOMAIN}}           HA integration domain, e.g. "intellicenter"
    {{CI_WORKFLOW}}      Primary CI workflow filename, e.g. "ci.yml" (or remove the CI badge)
    {{QUALITY_TIER}}     HA quality scale tier, e.g. "Platinum" (or remove the badge)
    {{LICENSE_NAME}}     "MIT" or "GPL-3.0"
    {{CROSSLINK_REPO}}   Companion Python library repo slug, e.g. "pyintellicenter"
    {{CROSSLINK_NAME}}   Companion Python library name, e.g. "pyintellicenter"
-->
# {{DISPLAY_NAME}}

{{TAGLINE}}

[![GitHub Release][releases-shield]][releases]
[![License][license-shield]](LICENSE)
[![HACS][hacs-shield]][hacs]
[![CI][ci-shield]][ci]
[![Quality Scale][quality-shield]][quality]
[![Project Maintenance][maintenance-shield]][maintenance]
[![GitHub Sponsors][sponsors-shield]][sponsors]
[![Ko-fi][kofi-shield]][kofi]

## What It Does

<!-- 2-4 sentences: what the integration connects to and the value it delivers. -->

## Features

<!-- Bulleted list of concrete capabilities. -->

## Prerequisites

<!-- Hardware/firmware/account requirements, supported HA version. -->

## Installation

See **[INSTALL.md](INSTALL.md)** for the complete guide.

**Quick version (HACS):** add this repository as a custom repository in HACS,
install **{{DISPLAY_NAME}}**, restart Home Assistant, then add the integration
from **Settings → Devices & Services**.

[![Open in HACS][hacs-repo-shield]][hacs-repo]

## Configuration

<!-- How to add and configure the integration; options flow; reconfiguration. -->

## Supported Equipment

<!-- Devices/models/entities the integration exposes. -->

## Automation Examples

<!-- A couple of realistic YAML automation snippets. -->

## Troubleshooting

<!-- Common issues and fixes; how to enable debug logging. -->

## Development

This integration is built on the
[{{CROSSLINK_NAME}}](https://github.com/joyfulhouse/{{CROSSLINK_REPO}}) Python
library. See [docs/DEVELOPMENT.md](docs/DEVELOPMENT.md) to set up a development
environment.

## Support

- **Issues:** <https://github.com/joyfulhouse/{{REPO}}/issues>
- **Discussions / questions:** open an issue with the `question` label.

## Support Development

If this project is useful to you, please consider supporting its development:

- [GitHub Sponsors][sponsors]
- [Ko-fi][kofi]

## License

This project is licensed under the **{{LICENSE_NAME}}** License — see
[LICENSE](LICENSE) for details.

## Credits

Built and maintained by [JoyfulHouse](https://github.com/joyfulhouse) with the
[{{CROSSLINK_NAME}}](https://github.com/joyfulhouse/{{CROSSLINK_REPO}}) library.

<!-- Badge links -->
[releases-shield]: https://img.shields.io/github/release/joyfulhouse/{{REPO}}.svg?style=for-the-badge
[releases]: https://github.com/joyfulhouse/{{REPO}}/releases
[license-shield]: https://img.shields.io/github/license/joyfulhouse/{{REPO}}.svg?style=for-the-badge
[hacs-shield]: https://img.shields.io/badge/HACS-Custom-41BDF5.svg?style=for-the-badge
[hacs]: https://github.com/hacs/integration
[hacs-repo-shield]: https://my.home-assistant.io/badges/hacs_repository.svg
[hacs-repo]: https://my.home-assistant.io/redirect/hacs_repository/?owner=joyfulhouse&repository={{REPO}}&category=integration
[ci-shield]: https://img.shields.io/github/actions/workflow/status/joyfulhouse/{{REPO}}/{{CI_WORKFLOW}}?style=for-the-badge&label=CI
[ci]: https://github.com/joyfulhouse/{{REPO}}/actions
[quality-shield]: https://img.shields.io/badge/Quality%20Scale-{{QUALITY_TIER}}-5c2d91.svg?style=for-the-badge
[quality]: https://developers.home-assistant.io/docs/core/integration-quality-scale/
[maintenance-shield]: https://img.shields.io/badge/maintainer-%40btli-blue.svg?style=for-the-badge
[maintenance]: https://github.com/btli
[sponsors-shield]: https://img.shields.io/badge/sponsor-GitHub-EA4AAA.svg?style=for-the-badge&logo=githubsponsors&logoColor=white
[sponsors]: https://github.com/sponsors/btli
[kofi-shield]: https://img.shields.io/badge/Ko--fi-donate-FF5E5B.svg?style=for-the-badge&logo=ko-fi&logoColor=white
[kofi]: https://ko-fi.com/bryanli
