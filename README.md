# experiments

Web experiments and prototypes.

## Adding a new experiment

1. Create a new folder with your experiment name (e.g., `my-experiment/`)
2. Add your files (at minimum an `index.html`)
3. **Add an entry to the root `index.html`** so it appears on the homepage
4. **Include the Plausible analytics script** in your `<head>`
5. **Add OG metadata and a cover image** for social sharing

### Homepage listing

Use the template in `index.html`:

```html
<a href="/experiment-name/" class="experiment">
  <h2>Experiment Title</h2>
  <p>Brief description of what this experiment does or explores.</p>
  <div class="meta">Month Year</div>
</a>
```

### Required `<head>` elements

Every experiment page needs these in the `<head>`:

```html
<!-- Plausible Analytics (use main domain, NOT subdomain) -->
<script async defer data-domain="mattkirkland.com" src="https://plausible.io/js/plausible.js"></script>

<!-- Open Graph -->
<meta property="og:title" content="Your Experiment Title">
<meta property="og:description" content="Brief description of the experiment">
<meta property="og:type" content="website">
<meta property="og:url" content="https://experiments.mattkirkland.com/your-experiment/">
<meta property="og:image" content="https://experiments.mattkirkland.com/your-experiment/og-image.png">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Your Experiment Title">
<meta name="twitter:description" content="Brief description of the experiment">
<meta name="twitter:image" content="https://experiments.mattkirkland.com/your-experiment/og-image.png">
```

### Creating the OG image

Each experiment needs an `og-image.png` (1200×630px). To create one:

1. Create a temporary `og-generator.html` in your experiment folder:

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    html, body {
      width: 1200px;
      height: 630px;
      overflow: hidden;
    }
    body {
      background: #your-bg-color;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      font-family: -apple-system, BlinkMacSystemFont, sans-serif;
      text-align: center;
    }
    /* Add your styles */
  </style>
</head>
<body>
  <!-- Your OG image content -->
</body>
</html>
```

2. Open the file in a browser sized to 1200×630
3. Take a screenshot and save as `og-image.png`
4. Delete the `og-generator.html` file (don't commit it)

### Design principles

Follow the **frontend-design skill** guidelines (see `~/clawd/skills/frontend-design/SKILL.md`):

- **Be distinctive**: Avoid generic AI aesthetics. No Inter, Roboto, or system fonts. No purple gradients on white.
- **Commit to a direction**: Pick a bold aesthetic (vintage, brutalist, maximalist, refined minimal, retro-futuristic, etc.) and execute it fully.
- **Typography matters**: Use interesting, characterful fonts. Pair a distinctive display font with a refined body font.
- **Add atmosphere**: Use textures, gradients, patterns, shadows — not just solid colors.
- **Motion & delight**: Staggered animations on load, surprising hover states, micro-interactions.
- **Be memorable**: What's the one thing someone will remember about this page?

Every experiment should feel genuinely designed, not AI-generated.

### Checklist

- [ ] Folder created with `index.html`
- [ ] Added to homepage `index.html`
- [ ] Plausible script included
- [ ] OG meta tags added
- [ ] `og-image.png` created (1200×630)
- [ ] Follows frontend-design principles (distinctive, memorable, no generic aesthetics)
