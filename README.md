<!-- Banner placeholder; replace Theme/assets/img/banner.png once available -->
<p align="center">
  <img src="https://raw.githubusercontent.com/ztffn/Jellyfin-Celluloid-Theme/main/Theme/assets/img/banner.png" alt="Celluloid Theme banner" width="100%">
</p>

<h1 align="center">🎬 Celluloid</h1>
<p align="center">A cinematic custom theme for <a href="https://jellyfin.org/">Jellyfin</a>, crafted for rich visuals, thoughtful typography, and a polished TV-first experience.</p>

<p align="center">
  <a href="#-features">Features</a> ·
  <a href="#-installation">Installation</a> ·
  <a href="#-repository-layout">Structure</a> ·
  <a href="#-development">Development</a>
</p>

---

## ✨ Features

_Work in progress._ The initial public release will focus on:

- Elevated "cinema marquee" styling for library and detail views
- Bold typography with deliberate spacing and glassmorphism accents
- Responsive layouts that balance 10-foot UI needs with desktop precision
- Optional overlays (watchlist, play, info) tuned for remote input

> We’re preparing the base CSS now. Follow the repository to get notified when the first tagged release lands.

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
