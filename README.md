# Celluloid Dreams
<h1 align="center"> 🎥 Celluloid Theme for Jellyfin </h1>
<p align="center">
  <img src="https://raw.githubusercontent.com/ztffn/Jellyfin-Celluloid-Theme/main/Previews/celluloidD2.png" alt="Celluloid Theme banner" width="100%">
</p>




***A custom theme for <a href="https://jellyfin.org/">Jellyfin</a> inspired by light leaks, film grain, and the quiet magic of cinema. Designed for rich visuals, clean typography, and a minimal, immersive viewing experience.***

---
## 📣 Roadmap / Status

- [x] Repository scaffolding & docs
- [x] Clean up initial Celluloid CSS
- [x] Patch for Jellyfin 10.11
- [ ] Cross browser compatibility
- [ ] Publish preview gallery
- [ ] Tag v0.9.0 release & announce

### ***Ready for collaborators and contributors to help improve and expand the theme.***
---

## 🎬 Features

- Animated backgrounds inspired by light leaks and the organic glow of exposed film
- Vertical navigation menu with quick-access links to admin and settings pages
- Beautiful item highlights with a soft backlit glow 
- Minimal typography and simplified web elements. Posters and movie artwork take center stage
- Bold play buttons and clear info cues for interactable elements
- Customizable color scheme and UI elements


---
> I like celluloid, I like film, I like the way that when a movie is projected it sort of breathes a little in the gate. That's the magic of it to me.
> 
> <sub>Gary Oldman</sub>
---

## 🎥 Preview

https://github.com/user-attachments/assets/bc94e7ad-bd9b-499a-aa51-97ae47d579a0

---

## 🧩 Installation

Until the packaged release is published, you can preview the theme by referencing the CSS directly from this repository.

### Option 1 — Jellyfin Dashboard (Custom CSS)

1. Go to **Dashboard → General → Custom CSS**.
2. Paste one of the following snippets at the bottom of the box:

   **Stable version:**
   ```css
   @import url("https://raw.githubusercontent.com/ztffn/Jellyfin-Celluloid-Theme/main/Theme/celluloid.css");
   ```
   
   **Latest development version:**
   ```css
   @import url("https://raw.githubusercontent.com/ztffn/Jellyfin-Celluloid-Theme/main/Theme/celluloid-nightly.css");
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

---

## 🎨 Customization

Celluloid Theme is designed to be easily customizable. You can modify the theme's appearance by adjusting the CSS variables.

### Color Scheme

To customize the color scheme, add the following to your Custom CSS after importing the theme:

```css
:root {
    /* Change colors to your preference (RGB values) */
    --white: 255, 255, 255;           /* Text and highlights */
    --white-off: 230, 230, 230;       /* Secondary text */
    --jade-green: 0, 200, 100;        /* Success indicators */
    --honey-yellow: 255, 200, 0;      /* Stars and warnings */
    --cherry-red: 220, 50, 50;        /* Error states */
    --deep-blue: 50, 100, 255;        /* Links and focus states */
    
    /* Main accent color - use one of the above or define your own */
    --accent: var(--jade-green);      
}
```

### UI Rounding

To enable custom rounding throughout the UI, add:

```css
:root {
    /* Customize UI element rounding */
    --rounding: 12px;                 /* Default rounding for most elements */
    --rounding-alt: 9px;              /* Alternative rounding for smaller elements */
    --rounding-large: 24px;           /* Larger rounding for prominent elements */
    --rounding-circle: 100px;         /* Full circle rounding for avatar elements */
}
```

### Additional Customizations

For more advanced customizations, check out the `docs/` folder for additional recipes and examples.

## 🛠️ Development

Want to help shape the theme?

1. Clone the repo and create a feature branch.
2. Work out of `Theme/celluloid-nightly.css` (feel free to break auxiliary snippets into `docs/` as needed).
3. Run your changes locally by pointing Jellyfin to your branch copy via `@import url("https://raw.githubusercontent.com/<username>/Jellyfin-Celluloid-Theme/<branch>/Theme/celluloid.css");`.
4. Submit a PR with before/after screenshots when possible.

Please keep new CSS tokens documented so we can maintain predictable customizations.

---

## 🐞 Troubleshooting

### Common Issues

- **Theme not applying**: Make sure you've added the import as the last line in your Custom CSS and performed a hard refresh (`Ctrl + Shift + R` / `Cmd + Shift + R`).
- **Vertical menu not showing**: The vertical menu is designed to be visible on desktop views. It will automatically hide during video playback.
- **Light leaks not visible**: The animated light leaks are subtle by design and may vary depending on your display settings.

### Browser Compatibility

Celluloid Theme is tested and optimized for:
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)

If you encounter issues on a specific browser, please report them in the GitHub issues.

---

