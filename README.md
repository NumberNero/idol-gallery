# Idol Census

Card database + art gallery for the K-pop card game, hosted with GitHub Pages.

- `index.html` — the page (no build step): Overview, Groups, Members, Idols, Gallery, Packs
- `cards.json` — card database: `{"synced": "<date>", "cards": [[id, name, group, set, rarity, gender, baseValue, tradeable, imageId], …]}`
- `packs.json` — pack definitions keyed by pack id (name, robux/free, price, allowed sets, current start/leaving dates, rebirth requirement, shop image id)
- `pack_history.json` — every premium run per pack id as `[["YYYY-MM-DD","YYYY-MM-DD"], …]` (first run + reruns); a sync appends the current window when it is new
- `img/packs.json` — pack shop images, `{imageId: data-URI}`
- `img/<SET>.json` — thumbnails for one set, `{imageId: data-URI}`; fetched on demand by the Gallery tab

Synced from Roblox Studio via Claude; each sync rewrites `cards.json` and `packs.json` and adds/rewrites only the image shards for changed sets. Pack Active/Retired status is computed live from dates.
