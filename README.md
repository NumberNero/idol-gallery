# Idol Census

Card database + art gallery for the K-pop card game, hosted with GitHub Pages.

- `index.html` — the page (no build step): Overview, Groups, Members, Idols, Gallery, Packs
- `cards.json` — card database: `{"synced": "<date>", "cards": [[id, name, group, set, rarity, gender, baseValue, tradeable, imageId], …]}`
- `packs.json` — pack definitions keyed by pack id (name, robux/free, price, allowed sets, start/leaving dates, rebirth requirement)
- `img/<SET>.json` — thumbnails for one set, `{imageId: data-URI}`; fetched on demand by the Gallery tab

Synced from Roblox Studio via Claude; each sync rewrites `cards.json` and `packs.json` and adds/rewrites only the image shards for changed sets. Pack Active/Retired status is computed live from dates.
