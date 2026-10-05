---
name: ui-graphic
description: >
  Identity art for community profiles: a wide banner and a portrait, plus the
  six-plate system members can wear. Use when designing or changing profile
  images, banners, member cards, stalls, or any face-forward community UI.
metadata:
  short-description: "Banner and portrait system distilled from ten graphic and interface practices"
user-invocable: false
---

# UI graphic identity

Every public member has two pictures: a **banner** (wide, environmental) and a
**portrait** (a person, or a crop of the same plate). They overlap. The name
sits beside the portrait on the page color, not on a scrim.

This is an original system. The ten practices below are references for
*behavior*, not art to trace.

## The ten practices

| Practice | What to take |
|---|---|
| Paula Scher | Scale does the talking. The name is the largest type on the stall. The banner does not need a caption. |
| Massimo Vignelli | One system, few parts. Six plates, two type families, one accent. A portrait and a banner are the same grammar. |
| Dieter Rams | Nothing decorative that is not the identity. No extra badges, no gradient blobs, no icon confetti. |
| Josef Müller-Brockmann | Alignment is the layout. The portrait sits on a shared left edge with the bio and the actions. |
| Jessica Hische | The portrait has to carry the person at stamp size. If the banner failed to load, the plate crop still reads. |
| Karri Saarinen | Calm density. Tabs, follow, and track rows are quiet. One copper action. Motion confirms (a live ring while a track plays). |
| Rauno Freiberg | Hover is physical and short. The banner image scales slightly. Reduced motion disables it. |
| Tobias van Schneider | The banner is a print, full-bleed, with air where the eye rests. Editorial, not a dashboard header. |
| Jessica Walsh | Color is a block used once. Each plate has one hot shape. The rest is field, paper, or ink. |
| Michael Bierut | The same mark must survive a 64px avatar, a card, and a stall. House files and plate crops both have to. |

## Assets

House artists use commissioned files in `public/community/`:

| Handle | Banner | Portrait | Plate fallback |
|---|---|---|---|
| mira-sol | mira-sol-banner.jpg | mira-sol-portrait.jpg | copper |
| night-dispatch | night-dispatch-banner.jpg | night-dispatch-portrait.jpg | dispatch |
| juniper-hale | juniper-hale-banner.jpg | juniper-hale-portrait.jpg | kitchen |
| kestrel | kestrel-banner.jpg | kestrel-portrait.jpg | orbit |
| sable-choir | sable-choir-banner.jpg | sable-choir-portrait.jpg | windows |
| rio-pell | rio-pell-banner.jpg | rio-pell-portrait.jpg | receipt |

Members do not upload. They wear a plate: `copper`, `dispatch`, `kitchen`, `orbit`, `windows`, `receipt`. The portrait is the right-hand crop of that plate (`xMaxYMid slice`) unless they pick a second plate on purpose. Choosing a banner keeps the portrait linked until the member picks a different one.

If a house file 404s, `ArtFrame` falls back to the plate. Never leave a broken image icon or a gray box.

## Rules when you change the art

- Stay inside the ObzueAI Independent palette: paper `#f4efe6`, ink `#1c1915`, copper `#c24b24`. Plate fields may shift hue; the accent does not.
- Banners are places or objects. Portraits are fictional musicians, illustrated, not photographs of real people.
- No text, logos, or watermarks inside the image files. Type is set in the component.
- Do not add a second typeface.
- The portrait ring is `border-surface`, so it cuts out of the banner in the page color.

Plate geometry lives in `PlateGraphic` inside `src/components/identity.tsx`. See `references/plates.md`.
