# Sandstone Engine

A from-scratch game engine for the **Sony PSP**.

The engine binary (`EBOOT.PBP`) is here. Its data is not - you build that
yourself from a PS2 disc image you own, using the
[**Quarry** converter](https://github.com/SandstoneDev/quarry). No game assets
are included in this repository.

---

## Installing

**1 - build your data** with [Quarry](https://github.com/SandstoneDev/quarry):
point it at your own extracted PS2 disc image and it writes a `data/` folder.

**2 - put it on the PSP.** On the memory card create `PSP/GAME/SANDSTONE/` and
copy into it:

- `EBOOT.PBP` (from this repo / the Release)
- the `data/` folder Quarry produced

Launch **Sandstone Engine** from the PSP Game menu.

> The engine will not start without a `data/` folder present.

---

## This build

Streamed audio now comes straight off the disc. The radio, the venue ambience
and the cutscene voice track are stored there as SPU ADPCM, which the engine
decodes directly - no transcoding step, and the result is smaller than the
compressed audio it replaces.

- **Radio** plays your disc's own stations, with names read from the disc.
- **Venue ambience** works again: the zone table shipped for a while with no
  audio behind it, so bars and shops were silent.
- **Cutscene audio** plays.
- **Interiors** are whole. A stream decoder kept only the first batch of a
  multi-batch model, which cost some rooms most of their geometry.
- **Water, grass, breakable props, map lights, money pickups, the save icon,
  the mission scripts and the door markers** are all produced by the converter
  now; several of them had never been.
- **Hero mods** work in the stock build: drop a pack in `data/mods/` and the
  character appears in the picker.

---

## Troubleshooting

If you're having issues, try the following:

- **Online mode isn't working?** Try connecting to a Wi-Fi network without a
  password (an open network).
- **The game won't start?** Disable all PSP plugins and try again.

---

## Recommended setup

- **Custom firmware:** ARK-4 or ARK-5
- **Official firmware:** PSP 6.61 (latest version)
- **Hardware:** PSP-3000

The engine should also work on other PSP models, but the PSP-3000 gives the best
experience.

---

## Credits

- **SandstoneDev** - engine and converter. Developed with the help of
 [Claude Code](https://www.anthropic.com/claude-code).
- Special thanks to **DenielX** for help with the engine's graphics work -
 [GitHub](https://github.com/DenielX/) ·
 [YouTube](https://www.youtube.com/@sp-pteam-indev6976)

---

## Disclaimer

Provided for interoperability, preservation, and homebrew use with a copy of the
source game you legally own. This project ships **no copyrighted game data** -
the converter operates only on a disc image you supply. Trademarks and game
content belong to their respective owners; this project is not affiliated with or
endorsed by any game publisher. Rightsholders may reach the maintainer at
`sandstonedevpsp@gmail.com`.
