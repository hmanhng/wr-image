# wr-image

Generated thumbnails for the Wild Rift overlay mod (skin / champion / skill images), pre-fitted for the client:

- `s/<skinId>.jpg` - skin, max side 192 px, JPEG
- `h/<heroId>.png` - champion icon, 64x64 PNG
- `k/<skillId>.png` - skill icon (skillId = heroId*4 + slot, slot 0..3 = Q,W,E,R), 48x48 PNG
- `index.json` - lists of ids per kind

Source: [League of Legends Wiki](https://wiki.leagueoflegends.com/en-us/) (Wild Rift pages); all images are property of Riot Games.
Regenerate with `scripts/publish-image-mirror.sh` in the mod repository. Do not edit by hand.
