# JoyfulHouse

Open-source [Home Assistant](https://www.home-assistant.io) integrations, ESPHome
device firmware, and the Python libraries that power them — built for reliable,
local-first smart home control.

## Home Assistant integrations

| Project | Integration | Python library |
|---|---|---|
| **EG4 / Luxpower** — solar & battery monitoring | [`eg4_web_monitor`](https://github.com/joyfulhouse/eg4_web_monitor) | [`pylxpweb`](https://github.com/joyfulhouse/pylxpweb) |
| **Pentair IntelliCenter** — pool/spa control | [`intellicenter`](https://github.com/joyfulhouse/intellicenter) | [`pyintellicenter`](https://github.com/joyfulhouse/pyintellicenter) |
| **Pool chemistry** — analysis & dosing | [`ha-poolchem`](https://github.com/joyfulhouse/ha-poolchem) | [`pypoolchem`](https://github.com/joyfulhouse/pypoolchem) |
| **LaMotte Spin Touch** — water testing | [`lamotte-spintouch`](https://github.com/joyfulhouse/lamotte-spintouch) | — |
| **Moogo** — smart mosquito misting | [`moogo`](https://github.com/joyfulhouse/moogo) | [`pymoogo`](https://github.com/joyfulhouse/pymoogo) |
| **Thermacell LIV** — mosquito protection | [`thermacell_liv`](https://github.com/joyfulhouse/thermacell_liv) | [`pythermacell`](https://github.com/joyfulhouse/pythermacell) |
| **Brilliant** — in-wall smart panels | [`brilliant-mqtt`](https://github.com/joyfulhouse/brilliant-mqtt) | — |

## ESPHome firmware & local RF

| Project | What it does |
|---|---|
| [**esphome-quietcool**](https://github.com/joyfulhouse/esphome-quietcool) | QuietCool whole-house & attic fans over their native 433.92 MHz 2-FSK link — reverse-engineered from the OEM remote firmware, with learn-mode pairing |
| [**esphome-rf433-mqtt-bridge**](https://github.com/joyfulhouse/esphome-rf433-mqtt-bridge) | Sonoff RF Bridge R2 (Portisch) MQTT beacon — correlated, scheduled 433.92 MHz transmission |
| [**zemismart-blinds**](https://github.com/joyfulhouse/zemismart-blinds) | AOK/Zemismart 433.92 MHz roller blinds — local RF via MQTT + Sonoff RF Bridge |
| [**AIOsense**](https://github.com/joyfulhouse/AIOsense) | All-in-one ESPHome mmWave presence & environment sensor — cheaper and fully open |

## Standards

All repositories follow a shared set of documentation, licensing, and
contribution conventions. See [STANDARDS.md](https://github.com/joyfulhouse/.github/blob/main/STANDARDS.md).

## Support Development

If these projects are useful to you, please consider supporting their
development:

- [GitHub Sponsors](https://github.com/sponsors/btli)
- [Ko-fi](https://ko-fi.com/bryanli)
