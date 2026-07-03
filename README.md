# NARA SHIKAMARU — Shadow Possession Awakening

A single-page, cinematic scroll experience built with vanilla HTML/CSS/JS and GSAP ScrollTrigger. Features a looping hero video, scroll-pinned image morph sequence, animated typography, and film-grain/HUD overlay effects — no framework, no build step required.

## ✨ Features

- **Preloader** with animated logo, kanji reveal, and progress bar
- **Hero section** with autoplay looping background video + flicker/particle FX
- **HUD overlay** (top/bottom fixed frame text, cinematic UI style)
- **Scroll-pinned transformation sequence** — three layered images (`1.png`, `2.png`, `3.png`) cross-fade/morph as the user scrolls, driven by GSAP ScrollTrigger
- **Custom cursor** with hover states (disabled on touch devices)
- **Outro section** with signature/kanji closing
- Fully responsive (desktop + mobile breakpoints included)

## 📁 Project Structure

```
Shikamaru/
├── shikamaru-site.html   # Main entry point (all CSS + JS inline)
├── 1.png                 # Base transformation image
├── 2.png                 # Seal-state transformation image
├── 3.png                 # Sage-state transformation image
├── video/
│   └── hero.mp4           # Hero background video (looping)
└── README.md
```

## 🚀 Getting Started

No installation or build tools needed — it's a static HTML file.

**Option 1 — Just open it**
Double-click `shikamaru-site.html` to open directly in a browser.

**Option 2 — Local server (recommended)**
Some browsers restrict video/autoplay or local file (`file://`) access. Serve it locally instead:

```bash
# Python
python3 -m http.server 8000

# Node
npx serve .
```

Then visit `http://localhost:8000/shikamaru-site.html`.

## 🧩 Dependencies

Loaded via CDN (no npm install needed):

- [GSAP 3.12.5](https://gsap.com/) — core animation engine
- [GSAP ScrollTrigger](https://gsap.com/docs/v3/Plugins/ScrollTrigger/) — scroll-pinned morph sequence
- Google Fonts: `Anton`, `Shojumaru`, `Space Mono`, `Shippori Mincho`, `Bebas Neue`

Requires an internet connection on first load (for CDN + font fetch), unless you vendor these locally.

## 🎨 Customization

Key CSS variables (top of `<style>` in the HTML file) control the theme:

| Variable | Purpose |
|---|---|
| `--ink` | Base background (near-black) |
| `--storm` | Hero backdrop tone |
| `--shadow` | Pale shadow-grey accent |
| `--deer` | Warm brown/dusk accent |
| `--volt` | Electric blue-white accent (lightning) |
| `--paper` | Off-white text color |

To swap the transformation images, replace `1.png`, `2.png`, `3.png` (keep filenames or update the `src` paths around the `morph__layer` elements). To change the hero video, replace `video/hero.mp4`.

## ⚠️ Notes

- Autoplay video may be muted-only on some mobile browsers by policy — the video already includes `muted autoplay playsinline loop` for compatibility.
- If images fail to load, inline `onerror` fallbacks are wired up in the script to swap in placeholder sources.
- This is a fan/tribute page (Naruto: Shikamaru) intended for personal/portfolio use — not for commercial redistribution given the IP involved.

## 📄 License

Personal/portfolio project. Character names and likeness belong to their respective copyright holders (Masashi Kishimoto / Shueisha / Studio Pierrot).
