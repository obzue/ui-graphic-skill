# Plates

Each plate is one SVG composition. Banner and portrait are two crops of it
unless a house file replaces both.

| Id | Hue | Banner idea | Focal crop (portrait) |
|---|---:|---|---|
| copper | 22 | Dark field, lantern circle on the right, copper rule along the bottom | The lantern |
| dispatch | 210 | Vertical rain rules, a dark block on the right, a cream platform edge | The dark block |
| kitchen | 92 | A four-pane window on the right, a small copper sun on the left | The window |
| orbit | 198 | Two rings and a copper center on the right, a loose grid of lights | The orbit |
| windows | 36 | Four tall shutters of soft light on a deep field | The last shutter |
| receipt | 12 | Paper ground, ink rules, one copper bar on the right | The copper bar |

Class tokens in `src/styles.css`: `plate-field`, `plate-soft`, `plate-deep`, `plate-paper`, `plate-cream`, `plate-ink`, `plate-hot`, `plate-ring`. They read `--hue` from the wrapper.

Motion: `.banner-zoom` on hover, 700ms, disabled under `prefers-reduced-motion`. `.portrait-live` is a copper ring while that member's room-tone preview is playing.

Do not invent a seventh plate without adding it to `PLATES` in `src/lib/identity.ts` and to the save allow-list (`plateById` falls unknown ids back to copper).
