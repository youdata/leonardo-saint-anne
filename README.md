# Leonardo da Vinci · The Virgin and Child with Saint Anne

Leonardo da Vinci's The Virgin and Child with Saint Anne (Louvre, INV 776) — a narrated deep-zoom tour (in English), as a static page.

The painting at full resolution beside callouts on its details — the landscape, Saint Anne, Mary's drapery, the pebbles, the tree, Mary's unfinished head, the Child and the lamb — and three panels: the commission and cartoons, the other versions and the drawings on the back, and the 2011–12 cleaning.

Live: https://youdata.github.io/leonardo-saint-anne/

The image pyramid is a tile folder (`stanne/`: `header.idx` + `{z}/{x}/{y}.png`), so any static host serves it. Its fonts
are in `fonts/`, trimmed to the page's characters. The narrated video is not included.

## How it is made

From `infographic-examples/leonardo-saint-anne/build.mjs` (the page; its facts and quotations in `sources.md` there) with rx (`~/rx-cli`):

```sh
node build.mjs                                                     # → leonardo-saint-anne.json
rx export leonardo-saint-anne.json --out site --app /rx-graphic-editor/web/index.html --canvas --theme dark --lock-layers --tiles dir
rx publish site --to github:youdata/leonardo-saint-anne --yes
```
