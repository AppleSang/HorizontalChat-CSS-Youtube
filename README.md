# Horizontal Chat Editor v2.0

A browser-based CSS editor for creating horizontal YouTube live chat overlays. Chat messages appear in a single horizontal line with avatar, name, and message aligned side by side.



## Features

- **Live Preview** — See changes in real-time as you adjust settings
- **Horizontal Layout** — Avatar + Name + Message on one line
- **Per-role Colors** — Custom colors for Default, Mod, Member, and Owner
- **Super Chat Support** — Correct color tiers matching YouTube's official colors
- **Gifted Membership** — Green-to-cyan gradient background
- **Timestamp Toggle** — Show or hide timestamps
- **Hide Top Chat Badge** — Remove rank badges
- **OBS Compatible** — Copy CSS directly into OBS Browser Source
- **Dark UI** — Streamer-friendly dark interface
- **Auto-save** — Settings saved to localStorage
- **Multi-language** — Vietnamese and English (auto-detected by IP)

## Quick Start

1. Open `editor.html` in your browser
2. Adjust settings in the left panel (typography, colors, layout)
3. Use the preview buttons (Viewer, Mod, Member, Owner, Super Chat, Gift, Join) to test different message types
4. Click **Copy CSS** to copy the generated CSS
5. In OBS, add a **Browser Source** pointing to your YouTube live chat popout URL
6. Paste the CSS into the **Custom CSS** field

## Chat Types

| Button | Description |
|--------|-------------|
| Viewer | Regular viewer message |
| Mod | Moderator message (purple shield badge) |
| Member | Channel member message (green member badge) |
| Owner | Channel owner message (red name) |
| Super Chat | Super chat with correct tier colors |
| Gift | Gifted membership (green-cyan gradient) |
| Join | New membership announcement |

## Super Chat Color Tiers

Based on YouTube's official color scheme:

| Tier | Amount | Primary Color | Secondary Color |
|------|--------|---------------|-----------------|
| 1 | $1-$2 | Blue `rgb(30,136,229)` | Dark Blue `rgb(21,101,192)` |
| 2 | $5 | Cyan `rgb(0,229,255)` | Dark Cyan `rgb(0,184,212)` |
| 3 | $10-$20 | Green `rgb(29,233,182)` | Dark Green `rgb(0,191,165)` |
| 4 | $50 | Yellow `rgb(255,202,40)` | Dark Yellow `rgb(255,179,0)` |
| 5 | $100 | Orange `rgb(245,124,0)` | Dark Orange `rgb(230,81,0)` |
| 6 | $200-$500 | Pink `rgb(233,30,99)` | Dark Pink `rgb(194,24,91)` |
| 7 | $1000+ | Red `rgb(230,33,23)` | Dark Red `rgb(208,0,0)` |

## Default Colors

- **Name Color**: `#9a8484` (muted pink-gray)
- **Mod Name**: `#5541da` (purple)
- **Member Name**: `#41da93` (green)
- **Owner Name**: `#dd5050` (red)
- **All Messages**: `#ffffff` (white)

## OBS Setup

1. In OBS, click **+** under Sources → **Browser**
2. Set the URL to your YouTube live chat popout:
   ```
   https://www.youtube.com/live_chat?is_popout=1&v=YOUR_VIDEO_ID
   ```
3. Set Width: `5000`, Height: `200`
4. Check **Shutdown source when not visible** (optional)
5. Click **OK**
6. Right-click the Browser Source → **Properties**
7. Scroll to **Custom CSS** and paste the copied CSS
8. Click **OK**

## Credits

- **[Zaladin5x](https://github.com/Zaladin5x)** — Base horizontal chat CSS layout
- **[Touru Baskara](https://ko-fi.com/s/c1037bb627)** — Editor concept & GUI design
- **[Septapus](https://chatv2.septapus.com/)** — Chat V2 style generator (inspiration for customization features)
- **[Reza (DekReza)](https://github.com/dekreza)** — Chat HTML data & rendering logic

## License

This project is open source. Feel free to use and modify.
