# XPulse 200 4V — Taken Apart

An interactive 3D concept page for the Hero XPulse 200 4V. It opens on the official 360° studio photos. As you scroll, the photos hand off to a 3D model that comes apart one assembly at a time.

## Features

- **360° hero:** drag to rotate the bike using official studio photography (12 frames, 30° apart)
- **Scroll to take it apart:** the bike separates into 13 assemblies, one chapter at a time
- **Clickable parts:** select any part to open a panel with its details and specs
- **5 official colours:** switch paint schemes live on both the photos and the 3D model
- **Works on every screen:** phones (portrait and landscape), tablets, laptops and desktops, with support for iPhone notches
- **Built for speed:**
  - Phones load a lighter model (1.4 MB instead of 2.9 MB)
  - Graphics are prepared during loading, so scrolling doesn't stutter
  - Resolution drops automatically if a device can't keep up
- **Accessible:** keyboard navigation and reduced-motion support. If a device can't show 3D, the text and specs still work.

## Project structure

```
index.html        The whole site (HTML, CSS and JS in one file)
xpulse.glb        3D model for desktops and laptops (4096px texture)
xpulse-m.glb      3D model for phones and tablets (2048px texture)
360/<colour>/     360° photos, 1.webp to 12.webp for each colour
```

## Run locally

The browser won't load the 3D model if you open `index.html` directly from disk, so you need a local server:

```bash
python3 -m http.server 8000
# or
npx serve .
```

Then open http://localhost:8000.

## Deploy

It's a static site with no build step. Upload these files to any static host (GitHub Pages, Netlify, Vercel, Cloudflare Pages):

- `index.html`
- `xpulse.glb`
- `xpulse-m.glb`
- the `360/` folder

## Tech

- [Three.js](https://threejs.org/) 0.169 for 3D rendering (loaded from a CDN)
- [Lenis](https://github.com/darkroomengineering/lenis) for smooth scrolling
- Cormorant Garamond and Jost fonts from Google Fonts

## Credits

- 3D model: [Hero Xpulse](https://sketchfab.com/3d-models/hero-xpulse-434cdbdfad924bcd80c1f79858d887ae) by Bhavik Suthar
- 360° photography © Hero MotoCorp

This is a fan concept page, not affiliated with Hero MotoCorp. Figures are approximate.
