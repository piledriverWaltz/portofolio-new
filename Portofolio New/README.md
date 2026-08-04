# Bobber — Interactive 3D Motorcycle Portfolio

A single-file, offline-capable portfolio site built with Three.js. The motorcycle
you uploaded is embedded directly in `index.html` (as base64), so this **one file
is the entire website** — there's no separate `assets` folder to lose track of.

## Opening it

Just double-click `index.html`, or drag it into any browser. No local server
needed — the 3D model, textures, and geometry are all embedded in the file itself.
You do need an internet connection once, since Three.js and the fonts load from
a CDN (jsDelivr + Google Fonts).

## What's in it

- **Garage view (default):** the bike on a turntable platform. Drag to orbit,
  scroll to zoom. Five glowing hotspots sit on real points of the mesh —
  **speedometer** (About), **engine** (Skills), **seat** (Experience),
  **front wheel** (Projects), **rear wheel** (Contact) — click any of them to
  open the info panel.
- **Test Drive:** switches to a third-person chase camera on a straight desert
  highway at sunset. WASD / arrow keys to steer and throttle, dodge rocks and
  tumbleweed, distance = score. Difficulty ramps up the longer you survive.

## Making it yours

Open `index.html` in any text/code editor and search for:

```
0. PORTFOLIO CONTENT — EDIT THIS SECTION WITH YOUR OWN INFO
```

Everything you'd want to change lives in that one `PORTFOLIO` object right
after it — your name, role, and the text/links/timeline behind each of the
five hotspots. It's plain JavaScript object literal, so just edit the strings;
you don't need to touch anything below it.

A few other things worth knowing:

- The hotspot 3D coordinates (`HOTSPOT_POSITIONS`, just below `PORTFOLIO`) were
  hand-measured from your specific model's geometry. If you ever swap in a
  different `.glb`/`.gltf` model, those will need to be re-measured — they
  won't line up with a different mesh.
- Colors, fonts, and spacing are all CSS custom properties at the very top of
  the `<style>` block (`--sunset-burn`, `--sand-gold`, etc.) if you want to
  shift the palette.

## Deploying it

Because it's one static HTML file, you can drop it straight onto GitHub Pages,
Netlify, Vercel, or any static host — no build step required.

## License note

The motorcycle model ("Bobber Indian" by windupbird, CC BY 4.0) is credited
in-page under your name in the top bar, and the full license terms are in
`license.txt`. Keep that credit line if you publish this — that's the one
condition of the license.
