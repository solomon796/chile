# Patagonia Interactive Map

This is a super‑simple site you can host on GitHub Pages. It shows a Leaflet map with emoji markers and a path. All content lives in `stops.json` so you can edit the itinerary without touching code.

## Files
- `index.html` – loads Leaflet and fetches `stops.json`, draws markers + route + popups.
- `stops.json` – your itinerary stops (order = route order).
- `README.md` – these instructions.

## How to use
1. Upload **index.html**, **stops.json**, and **README.md** to your GitHub repo (root).
2. In repo **Settings → Pages**, set Source = **Deploy from branch**, Branch = **main**, Folder = **/**.
3. Visit `https://<your-username>.github.io/<repo-name>/`.

## Update the itinerary
- Edit `stops.json` (add/remove or reorder items). Commit to `main`. Refresh the site.
- Each stop must include: `key`, `name`, `emoji`, `lat`, `lng`. Optional: `dates`, `desc`.

## Example schema
```json
[
  { "key": "atacama", "name": "Atacama Desert", "emoji": "🌵", "lat": -22.91, "lng": -68.20, "dates": "19–22 Jan", "desc": "Highlights..." }
]
```

## Troubleshooting
- Blank page? Ensure `index.html` references the Leaflet CDN *and* that `stops.json` exists in the same folder.
- Map shows but no markers? Check that `stops.json` is valid JSON and not empty.
- Route line missing? Click **Toggle Path** or ensure there are at least two stops.
