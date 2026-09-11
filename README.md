# vanshika.dev

Personal portfolio. A single self-contained HTML file: an interactive 3D tower
built with Three.js, where scrolling spirals the camera down and around six
project cards.

Live: https://vanshika-portfolio-gilt.vercel.app

## Running it

No build step, no dependencies to install. Serve the folder:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000

Three.js and the fonts load from CDNs, so opening `index.html` directly over
`file://` also works.

## Layout

- `index.html` is the whole site: markup, styles, and the Three.js scene.
- `index.original.html` is a snapshot of an earlier version, kept for reference.

## Editing

Projects are defined once, in the `PROJECTS` array near the top of the script.
Each entry drives both the label rendered onto its 3D card and the contents of
the side panel that opens when the card is clicked. Adding or removing an entry
restacks the tower automatically.

The prose sections (short version, open source, paid work, about, stack,
contact) live in the `#outro` markup.

## Built with

C++ is the day job, but this one is HTML, CSS, and Three.js r128.
