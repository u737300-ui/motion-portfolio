# Motion — Photographer Portfolio

Single-file cinematic photographer portfolio with a 3D camera lens hero and a photo-card reel in **continuous left-to-right loop motion**:

- Cards travel the full curved path from the left edge to the right edge at a constant speed, then wrap straight back to the left — no fade-out at the edges, no slowdown on hover, seamless repeat.
- The loop only pauses while a photo lightbox is open, and resumes from the exact same position on close.
- NEW under the hero: a 3D staircase section (300vh of scroll) — a central pole lettered "JAM" / "STUDIO" and all 22 photo cards riding a conveyor up the pole. Scrolling moves the cards directly (no snap-back, so desktop wheel scrolls respond notch by notch): each card enters low from the pole's left side, rises to the front and OPENS — biggest, brightest, its description revealed, clickable to open the photo viewer — then keeps rising past the pole's right side and disappears at the top. Only 5 cards show at once (the open one, 2 below, 2 above). Performance: the WebGL hero renders nothing while off-screen, stair images load at a lighter size, and only visible cards get compositing layers.
- Below it, a door with a "GALLERY" name plate: the full archive gallery (category filters + grid) stays hidden until the door is clicked — the door swings open, then the gallery reveals and scrolls into view. A "Close gallery" button hides the gallery again, scrolls back to the door, and the door swings closed; clicking the open door also closes both.
- Light / dark theme toggle.
- Pricing + booking sections in the same layout as the Jam Studio live site: 3 cards (Weddings / Portraits / Events & Editorial, "Request a Quote", "Book on WhatsApp" buttons that scroll to the form and pre-select the service), then a two-column book section ("Your date, held in light." + 01/02/03 steps beside the form — service, date, name, phone/WhatsApp, city/venue, details) whose submit opens WhatsApp with the whole booking pre-written (set the photographer's number in `CONFIG.whatsapp`).
- Under the book section, a "Talk to Jam Studio" contact section with three cards — Instagram (@jam_studio_official.pk), Facebook (Jam Studio photography, facebook.com/jamstudiosdkofficial) and Email. Each card is driven by `CONFIG` (`instagram` / `facebook` / `email`) and hides automatically while its value is empty. Jam Studio lists no public email on their Instagram or Facebook profiles (checked 2026-11-11); `CONFIG.email` is set to studionikon42@gmail.com, provided by Arslan on 2026-11-11, so all three cards show.

## Preview on GitHub Pages

Repo root contains `index.html` only (no build step). Enable **Settings → Pages → Deploy from a branch → main / (root)**.

Live: https://u737300-ui.github.io/motion-portfolio/

## Before real client use — edit `CONFIG` in `index.html`

1. `name`, `bio`, `location` — the photographer's real details.
2. `whatsapp` — digits only, international format (e.g. `923001234567`).
3. `instagram` / `facebook` / `email` — the client's profile URLs and public email for the contact cards (a card hides while its value is empty).
4. `photos` — replace the placeholder frames with real photos: `{src:"photos/01.jpg", title:"…", cat:"Weddings"}`.
