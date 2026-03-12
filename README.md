# 🏒 NHL Stats Tracker

A live NHL player stats lookup tool built with vanilla JavaScript, pulling real-time data from the official NHL public API — no API key required.

**[Live Demo →](https://jdmortson.github.io/nhl-stats-tracker)**

---

## Features

- **Live player search** — search any active NHL player by name with auto-complete suggestions
- **Real-time stats** — pulls current season data directly from the NHL API
- **Skater & goalie support** — displays relevant stats for both positions
- **Quick search** — one-click buttons for popular players
- **Responsive design** — works on desktop and mobile

## Stats Displayed

| Skaters | Goalies |
|---|---|
| Points | Wins / Losses |
| Goals | Goals Against Average |
| Assists | Save Percentage |
| Plus/Minus | Shutouts |
| Games Played | Games Played |
| Avg Ice Time | — |

## Tech Stack

- **Vanilla JavaScript** — no frameworks or dependencies
- **NHL Public API** — `api-web.nhle.com` for player stats, `suggest.svc.nhl.com` for search
- **CSS Grid & Custom Properties** — responsive layout with a dark ice aesthetic
- **GitHub Pages** — static hosting, zero backend

## How It Works

1. User types a player name → hits the NHL suggest API for autocomplete
2. User selects or confirms a player → hits the NHL landing API for full stats
3. Stats are parsed and rendered into a dynamic card component
4. Position (skater vs goalie) is detected and the appropriate stat layout is shown

## Run Locally

No build step needed — just open the file:

```bash
git clone https://github.com/jdmortson/nhl-stats-tracker
cd nhl-stats-tracker
open index.html
```

## API Reference

- Player suggestions: `https://suggest.svc.nhl.com/svc/suggest/v1/minactiveplayers/{query}/{limit}`
- Player stats: `https://api-web.nhle.com/v1/player/{id}/landing`

Both endpoints are public and require no authentication.
---
Part of my personal portfolio
