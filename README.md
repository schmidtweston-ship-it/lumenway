# Lumenway

Family music steering system. **Not** ISO Principle.

| | ISO Principle | Lumenway |
|---|---|---|
| Input | mood → target mood | mood + body (blood sugar, sleep, stress) + spoken context |
| Output | seven songs | three-song arc: **entry → bridge → landing** |
| After | (playlist) | log what shifted; arcs compound over time |

## What this scaffold is

- `PROMPT.md` — navigator core + input schema notes
- `schema/state.input.json` — state you feed in
- `schema/arc.output.json` — arc shape you get out
- `logs/arcs.jsonl` — append-only arc + feedback log
- `index.html` — offline runner: fill state → copy filled prompt → paste arc / feedback into the log viewer (saved in this browser)

## How to run (local)

1. Open `index.html` in a browser (file:// is fine), or serve the folder:
   `python3 -m http.server 8841 --directory /home/box/library/made/lumenway`
2. Fill the state form. Copy the filled navigator prompt into any chat that can run the prompt.
3. Paste the returned arc back into the page. Optionally add what shifted after listening.
4. Export / append lines into `logs/arcs.jsonl` so the next run can read history.

## Intentionally unwired

- No Spotify (or other) streaming API.
- No automatic track catalog or “play now” button.
- No claim that an arc was heard until Weston reports back.
- No medical advice; low-sugar / crisis → prefer Steady and house safety tools.

## Honesty

Ada (Family CTO) keeps this honest: scaffold = prompt + log structure + offline runner. Live ship URL only after GitHub Pages verify returns HTTP 200.
