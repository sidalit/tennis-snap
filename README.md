<div align="center">

<img src="snap/gui/tennis.png" alt="tennis logo" width="128" />

# tennis

**Print stylish CSV, JSON and SQLite tables in your terminal.**

[![tennis](https://snapcraft.io/tennis/badge.svg)](https://snapcraft.io/tennis)
[![Base: core26](https://img.shields.io/badge/Base-core26-2C8C3C?logo=canonical&logoColor=white)](https://snapcraft.io/core26)
![Confinement: strict](https://img.shields.io/badge/Confinement-strict-2C8C3C)
[![Maintainer: sidaliteir](https://img.shields.io/badge/Maintainer-sidaliteir-2C8C3C?logo=snapcraft&logoColor=white)](https://snapcraft.io/publisher/sidaliteir)
![Architectures: amd64, arm64](https://img.shields.io/badge/Architectures-amd64%20%7C%20arm64-2C8C3C?logo=linux&logoColor=white)

[Getting Started](#getting-started) · [Configure](#configure) · [Limitations](#limitations) · [Build](#build) · [Support](#support) · [License](#license)

Unofficial snap packaging for [tennis](https://github.com/gurgeous/tennis), a small CLI that prints CSV, JSON and SQLite data as colorful tables sized to your terminal.

</div>

---

## Getting Started

<a href="https://snapcraft.io/tennis"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install tennis
tennis data.csv --zebra --row-numbers
```

Pipe data in with `cat data.json | tennis`, read SQLite databases with `tennis app.db --table users`, or get a quick summary with `tennis data.csv --peek`. The snap includes the `sqlite3` command that tennis uses; `less` comes from the core26 base.

## Configure

There are no `snap set` options or configuration files. Choose the theme, borders, colors and layout with command-line options such as `--theme`, `--border` and `--color`; tennis also honors `NO_COLOR=1`.

For files on removable storage:

```bash
sudo snap connect tennis:removable-media
```

## Limitations

- Files must be in a normal folder under your home directory, on connected removable storage, or piped through standard input. Hidden folders directly under your home directory are not accessible.
- `--pager` uses `less` from the core26 base. A `$PAGER` that points to another host program is not available inside the snap.

## Build

```bash
git clone https://github.com/sidalit/tennis-snap.git
cd tennis-snap
sudo snap install snapcraft --classic
snapcraft pack
```

## Support

- **Installation or snap issues:** [open a packaging issue](https://github.com/sidalit/tennis-snap/issues).
- **Application bugs:** [report them upstream](https://github.com/gurgeous/tennis/issues).

## License

Snap packaging: [MIT](LICENSE).
