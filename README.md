# OrcaSlicerPortable

[![Platform](https://img.shields.io/badge/platform-Windows-0078D6?logo=windows&logoColor=white)](#)
[![OrcaSlicer](https://img.shields.io/badge/for-OrcaSlicer-orange)](https://github.com/SoftFever/OrcaSlicer)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Donate with PayPal](https://img.shields.io/badge/Donate-PayPal-00457C?logo=paypal&logoColor=white)](https://www.paypal.com/donate/?hosted_button_id=6CDEVZGJWTNQQ)

A tiny launcher that runs **OrcaSlicer in portable mode**.

By default, OrcaSlicer stores its configuration in the Windows user profile (`%AppData%`). This launcher starts OrcaSlicer with a local data directory instead, so all settings, printer profiles and filament presets are saved in a `profile` folder **next to the executable** — your complete configuration travels with the installation, e.g. on a USB drive or in a synced folder.

## Features

- ✅ Fully portable — no installation, no registry entries
- 💾 All settings live in a local `profile` folder next to the app
- 🔌 Perfect for USB drives, shared machines or multiple side-by-side configurations
- 🪶 Minimal footprint — a single small `.exe`, nothing else

## Installation

1. Download and unzip OrcaSlicer: [OrcaSlicer Releases](https://github.com/SoftFever/OrcaSlicer/releases)
2. Download `OrcaSlicerPortableStarter.exe` from the [Releases](../../releases) page of this repository
3. Copy `OrcaSlicerPortableStarter.exe` into your OrcaSlicer folder (next to the original `orca-slicer.exe`)
4. Run `OrcaSlicerPortableStarter.exe`

That's it — a `profile` folder is created on first start and holds all your settings from then on.

## Updating OrcaSlicer

Unzip the new OrcaSlicer version, copy `OrcaSlicerPortableStarter.exe` into the new folder and move your existing `profile` folder next to it. All your settings are preserved.

## How it works

The launcher simply starts OrcaSlicer with a local data directory:

```
orca-slicer.exe --datadir profile
```

## Building from source

The project is a minimal C# console application (.NET Framework 4.7.2). Open `OrcaSlicerPortable.sln` in Visual Studio and build — no external dependencies.

> The build output is named `OrcaSlicerPortable.exe`, while the file on the
> [Releases](../../releases) page is named `OrcaSlicerPortableStarter.exe`.
> It is the same program — the name works either way, since the launcher is
> located by you, not by OrcaSlicer.

## Support / Donate

If you find this project useful, you can support the development with a donation — thank you! ❤️

[![Donate with PayPal](https://img.shields.io/badge/Donate-PayPal-00457C?logo=paypal&logoColor=white&style=for-the-badge)](https://www.paypal.com/donate/?hosted_button_id=6CDEVZGJWTNQQ)

## Credits

Based on [PrusaSlicerPortable](https://github.com/entrhopi/PrusaSlicerPortable), adapted for OrcaSlicer.

## License

[MIT](LICENSE)

## Disclaimer

This project is not affiliated with or endorsed by SoftFever or the OrcaSlicer project. OrcaSlicer is developed by [SoftFever](https://github.com/SoftFever/OrcaSlicer).
