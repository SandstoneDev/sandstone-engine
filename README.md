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
