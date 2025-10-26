# Celluloid Theme Customization Guide

This guide provides detailed instructions for customizing the Celluloid Theme for Jellyfin.

## Color Scheme

The theme uses RGB color values for maximum flexibility with opacity. You can modify these colors by adding custom CSS after importing the theme.

### Default Colors

```css
:root {
    --white: 243, 242, 243;           /* F3F2F3 - Used for text and highlights */
    --white-off: 207, 221, 233;       /* CFDDE9 - Used for secondary text */
    --jade-green: 0, 172, 111;        /* 00AC6F - Used for success indicators */
    --honey-yellow: 255, 194, 85;     /* FFC255 - Used for stars and warnings */
    --cherry-red: 212, 51, 83;        /* D43353 - Used for error states */
    --deep-blue: 78, 116, 247;        /* 4E74F7 - Used for links and focus states */
    
    /* Main accent color */
    --accent: var(--deep-blue);
}
```

### Example: Dark Green Theme

```css
:root {
    --white: 240, 240, 240;
    --white-off: 200, 220, 210;
    --jade-green: 0, 150, 80;
    --honey-yellow: 255, 200, 0;
    --cherry-red: 220, 60, 60;
    --deep-blue: 0, 120, 80;
    
    --accent: var(--jade-green);
}
```

### Example: Warm Gold Theme

```css
:root {
    --white: 255, 250, 240;
    --white-off: 240, 230, 210;
    --jade-green: 80, 150, 30;
    --honey-yellow: 255, 180, 0;
    --cherry-red: 230, 70, 50;
    --deep-blue: 200, 150, 50;
    
    --accent: var(--honey-yellow);
}
```

## UI Rounding

You can customize the roundness of UI elements by uncommenting and modifying these variables:

```css
:root {
    --rounding: 12px;          /* Default rounding for most elements */
    --rounding-alt: 9px;       /* Alternative rounding for smaller elements */
    --rounding-large: 24px;    /* Larger rounding for prominent elements */
    --rounding-circle: 100px;  /* Full circle rounding for avatar elements */
}
```

### Examples

#### Sharp Corners

```css
:root {
    --rounding: 0;
    --rounding-alt: 0;
    --rounding-large: 0;
    --rounding-circle: 100px;  /* Keep avatars circular */
}
```

#### Very Rounded

```css
:root {
    --rounding: 16px;
    --rounding-alt: 12px;
    --rounding-large: 32px;
    --rounding-circle: 100px;
}
```

## Font Size Adjustments

You can adjust the font sizes for better readability:

```css
body, h1, h2, h3, h4 {
    font-size: 110% !important; /* Default is 120% */
}

.detailPagePrimaryContainer {
    font-size: 105% !important; /* Default is 115% */
}
```

## Disabling Animations

If you prefer a more static look or want to reduce resource usage:

```css
/* Disable blob animations */
@keyframes blob_one, @keyframes blob_two, @keyframes blob_three {
    0%, 50%, 100% { 
        transform: none !important;
        border-radius: inherit !important;
    }
}

/* Disable gradient animation */
@keyframes gradient-anim {
    0%, 50%, 100% {
        background-position: 0% 50%;
    }
}

/* Disable card hover effects */
.card:hover .cardBox, .card.show-focus:focus .cardBox {
    transform: none !important;
}
.card:hover .cardBox::before, .card.show-focus:focus .cardBox::before {
    opacity: 0 !important;
}
```

## Advanced Customizations

### Custom Background Image

Replace the default background with your own:

```css
body.withSectionTabs .backdropImage {
    background-image: url("YOUR_IMAGE_URL_HERE") !important;
}
```

### Vertical Menu Width

Adjust the width of the collapsed and expanded vertical menu:

```css
body:not(.hide-scroll) .mainDrawer {
    width: 50px !important; /* Default is 60px */
}

.mainDrawer.focused, .mainDrawer:hover, .mainDrawer:focus-within {
    width: 220px !important; /* Default is 240px */
}
```

## Compatibility Notes

- Some customizations may not work properly on mobile devices or TV layouts
- Always test your customizations across different devices and browsers
- If you encounter any issues, try reverting to the default theme settings first

For more help or to share your customizations, visit the [GitHub repository](https://github.com/ztffn/Jellyfin-Celluloid-Theme).
