# 🏅 Olympics Race Simulator

A browser-based animated race simulator where you pick countries to compete head-to-head on a virtual track, complete with flags, live timers, and a medal leaderboard.

---

## Features

- **Country Selection** — Choose 2–10 countries from a multi-select list (USA, Canada, Jamaica, Japan, Germany, Brazil, Kenya, China, France, Italy)
- **Animated Runners** — Each country gets a lane with its flag and an animated running GIF
- **Countdown Timer** — A 3-2-1-GO! countdown kicks off every race
- **Randomized Speeds** — Each runner is assigned a random speed (5–8 m/s) so every race has a different outcome
- **Live Lane Timers** — Each runner's elapsed time updates in real time during the race
- **Finish Detection** — Runners stop and their GIF hides when they cross the finish line
- **Medal Leaderboard** — Gold 🥇, Silver 🥈, and Bronze 🥉 medals are awarded to the top three finishers, with final times and speeds displayed
- **Rainbow Title** — The page title cycles through colors using HSL animation

---

## How to Use

1. Open `index.html` in any modern web browser — no installation or server required.
2. **Select countries** from the list (hold `Ctrl` / `Cmd` to pick multiple).
3. Click **Create Race** to set up the track and lanes.
4. Click **Start Race** to begin the countdown and launch the race.
5. Watch runners compete and see the leaderboard update as each finisher crosses the line.
6. Click **Reset Race** to clear everything and start fresh.

---

## File Structure

```
olympics-race-simulator/
├── index.html       # Main application (HTML, CSS, and JS all in one file)
├── flag.gif         # Animated flag used as the Start Race button background
├── flag2.gif        # Flag icons displayed in the page title
└── README.md        # This file
```

> **Note:** `flag.gif` and `flag2.gif` are local assets referenced by the HTML. Make sure they are in the same directory as `index.html` for them to display correctly.

---

## External Resources Used

| Resource | Purpose |
|---|---|
| [flagcdn.com](https://flagcdn.com) | Country flag images |
| [Tenor GIF](https://media.tenor.com) | Animated running figure |
| [Flaticon](https://flaticon.com) | Gold, silver, and bronze medal icons |

---

## Browser Compatibility

Works in all modern browsers (Chrome, Firefox, Edge, Safari). No frameworks or dependencies required.

---

## Customization Tips

- **Add more countries** — Extend the `flagMap` object and add `<option>` entries to the select list using any country code from [flagcdn.com](https://flagcdn.com).
- **Adjust race speed** — Change `Math.random()*3+5` in `setupRace()` to tweak the speed range.
- **Change track length** — The finish line is at `850px`; adjust the `r.position >= 850` threshold and the `#track` width together.
- **Race distance label** — Add a `<select>` for race type (100m, 400m, marathon) and map it to different speed/threshold values for variety.

