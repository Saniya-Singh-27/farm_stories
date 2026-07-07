# The Farm Stories — cinematic experience

An ultra-premium, single-file storytelling website for **Mango Meadows, Peelamadu**
(a boutique managed mango orchard of 25 families).

## What's here

```
the-farm-stories/
├── index.html      # the entire site (HTML + CSS + JS inline)
├── vendor/         # self-hosted libraries (no CDN dependency)
│   ├── gsap.min.js
│   ├── ScrollTrigger.min.js
│   ├── lenis.min.js
│   └── three.min.js
└── README.md
```

Everything is **self-contained** — the only external requests are the
photographic content (Unsplash) and an optional hero video, both of which
degrade gracefully if unavailable.

## Highlights

- **Cinematic hero** — full-screen orchard with slow Ken Burns motion, drifting
  mist, light rays and a graceful `<video>` enhancement (falls back to the
  animated still if the video can't play).
- **Lenis smooth scroll** wired to **GSAP ScrollTrigger** throughout.
- **Scroll-driven 3D miniature orchard** (Three.js) — a low-poly mango grove
  with `FogExp2` atmosphere, warm directional lighting, soft shadows and a
  camera rig that orbits, tilts, descends and zooms as you scroll.
- **Living particles** — mango leaves, blossoms and glowing pollen drift across
  every page and react to scroll velocity.
- **Editorial reveals** — images resolve from blur + scale + parallax, never a
  plain fade.
- **Aerial plot layout** with glowing, self-drawing boundaries.
- **Documentation cards** that unfold in 3D; an **owner dashboard** that
  assembles piece by piece.
- **Cinematic sunset finale** — the sun rises, the ridge pulls back and leaves
  drift across the closing call to action.
- **Plots & Ownership aggregator** (MagicBricks-style) — sticky search, sort,
  grid / list / aerial views, filter facets, favourites, live result count and
  average price, plus a full detail modal per plot.
- Fully **responsive** and respects **`prefers-reduced-motion`** (heavy motion
  and the 3D scrub collapse to static, readable layouts).

## Viewing it

It's a static site — open `index.html` in a browser, or serve the folder:

```bash
cd the-farm-stories && python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment note

This is a plain static folder with **no build step and no framework/deploy
config** (no `package.json`, `vercel.json`, etc.), so adding it to the
repository does not change how any existing Vercel/host project builds or
deploys. To publish just this experience, point a static host at the
`the-farm-stories/` directory.
