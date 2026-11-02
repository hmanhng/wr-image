# wr-image

Generated thumbnails + manifest for the Wild Rift overlay mod (skin / champion / skill images), pre-fitted for the client:

- `manifest.json` - `{"v":1,"generated":ISO,"heroes":[{"id","name","icon","skills":[slot],"skins":[{"id","name"}]}]}`;
  heroes and skins sorted by id; `icon` is true iff `h/<id>.png` and `h2/<id>.png` exist, `skills` lists the slots whose `k/<id*4+slot>.png` exists,
  a skin is listed iff `s/<skinId>.jpg` and `s2/<skinId>.jpg` exist
- `s/<skinId>.jpg` - skin, max side 192 px, JPEG (older clients)
- `s2/<skinId>.jpg` - skin, max side 384 px, JPEG
- `h/<heroId>.png` - champion icon, 64x64 PNG (older clients)
- `h2/<heroId>.png` - champion icon, 128x128 PNG
- `k/<skillId>.png` - skill icon (skillId = heroId*4 + slot, slot 0..3 = Q,W,E,R), 48x48 PNG

Source: [League of Legends Wiki](https://wiki.leagueoflegends.com/en-us/) (Wild Rift pages); all images are property of Riot Games.
Regenerate with `scripts/publish-image-mirror.sh` in the mod repository. Do not edit by hand.
