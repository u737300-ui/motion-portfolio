# Motion — Photographer Portfolio

Single-file cinematic photographer portfolio with a 3D camera lens hero and a photo-card reel in **continuous left-to-right loop motion**:

- Cards travel the full curved path from the left edge to the right edge at a constant speed, then wrap straight back to the left — no fade-out at the edges, no slowdown on hover, seamless repeat.
- The loop only pauses while a photo lightbox is open, and resumes from the exact same position on close.
- Archive gallery with category filters, light / dark theme toggle, booking / contact section.

## Preview on GitHub Pages

Repo root contains `index.html` only (no build step). Enable **Settings → Pages → Deploy from a branch → main / (root)**.

Live: https://u737300-ui.github.io/motion-portfolio/

## Before real client use — edit `CONFIG` in `index.html`

1. `name`, `bio`, `location` — the photographer's real details.
2. `whatsapp` — digits only, international format (e.g. `923001234567`).
3. `instagram` — full profile URL.
4. `photos` — replace the placeholder frames with real photos: `{src:"photos/01.jpg", title:"…", cat:"Weddings"}`.
