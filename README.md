# 82 Duel

Unofficial fan draft game — build a five-man peak lineup across random franchise/decade pools, project an 82-game record, and 1v1 a friend.

**Not affiliated with the NBA or 82-0.** Stats are illustrative peaks for entertainment.

## How to open

1. Open `index.html` in any modern browser (Chrome, Firefox, Safari, Edge).
2. Double-click the file, or drag it into a browser window, or host the folder on any static server.
3. No install, no build step, no backend. Works offline after first load (Google Fonts may need network).

```bash
# optional local server
cd 82-duel && python3 -m http.server 8080
# then visit http://localhost:8080
```

## Pass & Play (same device) — default

1. Enter names for Player 1 and Player 2.
2. Tap **Start Pass & Play**.
3. Each round spins a franchise + decade (1960s–2020s). Both players draft from the **same five pools**, one round at a time (P1 then P2).
4. Optional: use your **TEAM** or **ERA** re-roll (one each per match).
5. Pick a player (filter ALL / G / F / C, sorted by PPG), then tap an eligible empty court slot (PG / SG / SF / PF / C).
6. After five rounds, compare projected W–L. Higher wins wins; ties break on strength rating.

## Challenge Code (remote friend)

1. On Home → **Challenge Code** → **Create Challenge**. Draft all five rounds.
2. Copy the shareable code and send it to a friend (text, email, chat).
3. Friend opens the game → **Challenge Code** → **Enter Challenge Code**, pastes the code, and drafts against the **same five pools**.
4. Final screen shows both rosters, both records, and the winner.

Codes are compact base64 JSON (spins + P1 roster/record). The same seed always regenerates the same pools.

## Rules summary

| Piece | Detail |
|--------|--------|
| Rounds | 5 |
| Pool | Random franchise + decade with real historical depth |
| Re-rolls | 1 TEAM + 1 ERA per player per match |
| Positions | One player per PG / SG / SF / PF / C; eligible slots highlighted |
| Projection | Sum peak PTS+REB+AST+2×STL+2×BLK → non-linear win curve (0–82) |
| Grades | Letter grade + label (e.g. B+ SOLID) from projected wins |

## Dataset

Embedded in the single HTML file: **30 franchises**, **1400+ player entries**, decades **1960s–2020s** (empty eras skipped). Historical names included (e.g. Seattle SuperSonics, Vancouver Grizzlies, Baltimore Bullets).

## Files

- `index.html` — entire game (CSS + JS + data)
- `README.md` — this file
