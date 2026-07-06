# MC Daylight

A **SJMCL** extension that bridges your Minecraft server time and real time — right on your launcher dock.

Each server card displays the current in-game time, moon phase, day count, and daylight progress, with a background that **smoothly transitions** through dawn, day, dusk, and night colors as the Minecraft sun moves across the sky.

## Features

- **Real-time clock** — Current local time displayed alongside server time
- **Per-server game time** — Each server independently tracks its in‑game clock (tick 0 = dawn, tick 6000 = noon, …)
- **Moon phase** — 8-phase lunar cycle (🌕 Full Moon → 🌑 New Moon)
- **Daylight progress bar** — Visual indicator of where the sun is in the sky
- **Color-shifting cards** — Card backgrounds smoothly interpolate through 8 distinct day/night palettes (CSS transitions)
- **Server icon support** — Auto-fetches server icon via `api.mcsrvstat.us`
- **Multiple servers** — Add as many servers as you like, each with independent time settings
- **Persistent state** — Server list and time offsets saved to `localStorage`

## Installation

1. Download the latest `.sjmclx` from [Releases](https://github.com/YoshinoHdq/SJMCL-MC-Daylight/releases)
2. Drag the file into your SJMCL launcher window
3. Open **Settings → MC Daylight** to add servers and set their current in‑game time

## Usage

### Adding a server

1. Go to **MC Daylight** in the extension settings
2. Enter a server name (optional) and IP address (e.g. `mc.hypixel.net`)
3. Click **Add**
4. Adjust the slider or tap a preset button (Dawn / Morning / Noon / Dusk / Night) to set the current in‑game time

### Home card

The home widget shows all your configured servers. Each card:

- Displays the server icon (auto-fetched)
- Shows the **in-game time** (🎮 06:30 → 18:30)
- Shows the **moon phase** and day count
- Has a **progress bar** indicating the daylight cycle
- Changes **background color** smoothly as the in-game time progresses

### Preset times

| Button    | Tick | Description |
|-----------|------|-------------|
| Dawn      | 0    | 06:00 – sunrise |
| Morning   | 2000 | 08:00 – golden hour |
| Noon      | 6000 | 12:00 – sun overhead |
| Dusk      | 12000| 18:00 – sunset |
| Night     | 18000| 00:00 – midnight |

## Technical Notes

- Minecraft runs at **20 ticks/second**; one in‑game day = 24000 ticks = 20 minutes real time
- The moon cycle lasts 8 Minecraft days (~160 minutes real time)
- Colors are **interpolated in RGB** between 8 key frames of the day/night cycle
- All state is persisted in `localStorage` under the `mct-` prefix

## Author

**hemekewayoshino**

Built with [SJMCL Extension API](https://github.com/SJMC-Dev/awesome-SJMCL-extensions)
