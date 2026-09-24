# Idol Gallery

Static card-art gallery for the K-pop card game, hosted with GitHub Pages.

- `index.html` — the page (no build step)
- `cards.json` — card database: `[id, name, group, set, rarity, gender, baseValue, tradeable, imageId]`, plus the sync date
- `img/<SET>.json` — thumbnails for one set, `{imageId: data-URI}`; fetched on demand as you browse

Synced from Roblox Studio via Claude; each sync updates `cards.json` and adds/rewrites only the shards for changed sets.
