<div align=center>

# MC Daylight

Real-time Minecraft day/night tracker inside your launcher ☀️🌙

**English · [简体中文](README.md)**

</div>

---

## 简介

MC Daylight is a SJMCL extension that displays real-time Minecraft server time and day/night status on the launcher home page, with card backgrounds smoothly transitioning based on the in-game sun position.

## Features

- 🕐 Real-time clock — real and in-game time side by side
- 🌍 Per-server time tracking — each server tracks its own game ticks independently
- 🌙 Moon phase display — 8-phase moon cycle
- 📊 Progress bar — visualize the sun position in the sky
- 🎨 Color-shifting cards — smooth interpolation across 8 day/night color palettes
- 🖼️ Server icons — auto-fetched
- ➕ Multi-server support — add unlimited servers with independent settings

## Installation

1. Download the .sjmclx file from Releases
2. Open SJMCL → Settings → Extension Management → Import
3. Add servers and set the current in-game time in the extension settings

### Time Presets

| Button | Tick | Description |
|--------|------|-------------|
| Dawn | 0 | 06:00 – Sunrise |
| Morning | 2000 | 08:00 – Golden hour |
| Noon | 6000 | 12:00 – Sun overhead |
| Dusk | 12000 | 18:00 – Sunset |
| Night | 18000 | 00:00 – Midnight |

### Technical Notes

- Minecraft runs at 20 ticks/second; one game day = 24000 ticks = 20 minutes real time
- Moon phase cycle = 8 game days
- Colors interpolate across 8 day/night keyframes using RGB interpolation

## Compatibility

- Minimum launcher version: 1.1.3

## License

MIT
