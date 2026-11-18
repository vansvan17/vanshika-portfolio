# vanshika.dev

Personal portfolio: an interactive 3D tower built with Three.js, where
scrolling spirals the camera down and around five floors, one per domain (low
level, competitive programming, research, cybersecurity, electronics). Clicking
a floor's card opens that domain's own page.

Live link: vanshika-portfolio-1zal.vercel.app

## Running it

No build step, no dependencies to install. Serve the folder:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000

Three.js and the fonts load from CDNs, so opening `index.html` directly over
`file://` also works.

## Layout

- `index.html` is the tower: markup, styles, and the Three.js scene.
- `low-level.html`, `competitive-programming.html`, `research.html`,
  `security.html`, `electronics.html` are the floor pages; they share `domain.css`.
- `vercel.json` turns on clean URLs, so `/security` works as well as `/security.html`.
- `index.original.html` is a snapshot of an earlier version, kept for reference.

## Editing

Floors are defined in the `PROJECTS` array near the top of the script. The last
entry is the top floor. Each entry's title, sub and first three tags are drawn
onto its 3D card; `url` is the page the card opens and `slug` is the `#hash`
that brings a visitor back to that floor. Adding or removing an entry restacks
the tower automatically. The projects themselves live in the floor pages.

The prose sections (short version, floor links, about, stack, contact) live in
the `#outro` markup.

## Built with

C++ is the day job, but this one is HTML, CSS, and Three.js r128.
