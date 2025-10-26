<!-- Banner placeholder; replace Theme/assets/img/banner.png once available -->
<p align="center">
  <img src="https://raw.githubusercontent.com/ztffn/Jellyfin-Celluloid-Theme/main/Previews/celluloidT2.png" alt="Celluloid Theme banner" width="100%">
</p>
<h1 align="center"> ⚠️ Work in progress. Not ready for use! ⚠️ </h1>

<h1 align="center">Celluloid</h1>
<p align="center"> A custom theme for <a href="https://jellyfin.org/">Jellyfin</a> — inspired by light leaks, film grain, and the quiet magic of cinema. Designed for rich visuals, clean typography, and a minimal, immersive viewing experience. </p>


<p align="center">
  <a href="#-features">Features</a> ·
  <a href="#-installation">Installation</a> ·
  <a href="#-repository-layout">Structure</a> ·
  <a href="#-development">Development</a>
</p>

---


## 🎬 Features

- Animated backgrounds inspired by light leaks and the organic glow of exposed film

- Vertical navigation menu with quick-access links to admin and settings pages

- Beautiful item highlights with a soft backlit glow 

- Minimal typography and simplified web elements. Posters and movie artwork take center stage

- Bold play buttons and clear info cues for interactable elements


---
> I like celluloid, I like film, I like the way that when a movie is projected it sort of breathes a little in the gate. That's the magic of it to me.
> 
> <sub>Gary Oldman</sub>
---

## 🧩 Installation

Until the packaged release is published, you can preview the theme by referencing the CSS directly from this repository.

### Option 1 — Jellyfin Dashboard (Custom CSS)

1. Go to **Dashboard → General → Custom CSS**.
2. Paste the following snippet at the bottom of the box:
   ```css
   @import url("https://raw.githubusercontent.com/ztffn/Jellyfin-Celluloid-Theme/main/Theme/celluloid.css");
   ```
3. Click **Save** and hard-refresh your browser/app (`Ctrl + Shift + R` / `Cmd + Shift + R`).

### Option 2 — Host Locally

1. Download `Theme/celluloid.css` and place it somewhere Jellyfin can reach (e.g. `/config/custom/web/celluloid.css`).
2. In **Dashboard → General → Custom CSS**, point to your local copy:
   ```css
   @import url("/custom/web/celluloid.css");
   ```
3. Save and refresh.

> **Tip:** Keep the import as the last line if you stack multiple community themes—Celluloid expects to be loaded after any base adjustments.

---

## 📁 Repository Layout

```
Jellyfin-Celluloid-Theme/
├── Theme/
│   ├── celluloid.css        # Core theme stylesheet (to be populated)
│   └── assets/
│       └── img/             # Banners, logos, promotional imagery
├── Previews/                # Optimized screenshots & videos (coming soon)
├── docs/                    # Additional usage notes & customization recipes
├── LICENSE
└── README.md
```

As assets are added you’ll find `webp` previews, color tokens, and optional add-on snippets inside `docs/`.

---

## 🛠️ Development

Want to help shape the theme?

1. Clone the repo and create a feature branch.
2. Work out of `Theme/celluloid.css` (feel free to break auxiliary snippets into `docs/` as needed).
3. Run your changes locally by pointing Jellyfin to your branch copy via `@import url("https://raw.githubusercontent.com/<username>/Jellyfin-Celluloid-Theme/<branch>/Theme/celluloid.css");`.
4. Submit a PR with before/after screenshots when possible.

Please keep new CSS tokens documented so we can maintain predictable customizations.

---

## 📣 Roadmap / Status

- [x] Repository scaffolding & docs
- [ ] Upload initial Celluloid CSS bundle
- [ ] Publish preview gallery
- [ ] Tag v1.0.0 release & announce

Stay tuned—once the CSS lands we’ll tag a pre-release and broaden testing.


