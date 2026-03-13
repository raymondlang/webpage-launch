# Style Sampler Template

Use this template to generate `_style-preview.html`. The sampler shows 3–4 curated style options as side-by-side hero previews so the user can **see** the direction before committing.

## Rules

- Each card renders a mini hero using the style's real fonts, colors, and accent
- Use the product's actual headline and subheadline from discovery — not placeholder text
- Cards should be tall enough to feel like a real hero (min-height ~70vh each) but not full-page
- The page background between cards should be neutral (`#1a1a1a` for dark gaps or `#f0f0f0` for light gaps) so styles don't bleed together
- Load all fonts for all shown styles in one combined set of `<link>` tags
- Each card gets a visible label: "Option N — Style Name" and a one-line vibe description
- The sampler itself has no interactivity beyond scrolling — no buttons that do anything, no JS logic
- Include `prefers-reduced-motion` support

## HTML structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Style Preview — {Product Name}</title>

  <!-- Load ALL fonts needed for all shown styles -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link rel="stylesheet" href="..." />

  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; }

    body {
      background: #1a1a1a;
      font-family: system-ui, sans-serif;
      color: #999;
    }

    .sampler-header {
      text-align: center;
      padding: clamp(2rem, 4vh, 4rem) 1rem;
    }

    .sampler-header h1 {
      font-size: clamp(1rem, 2vw, 1.25rem);
      font-weight: 400;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: #666;
    }

    .sampler-header p {
      font-size: clamp(0.85rem, 1.2vw, 1rem);
      color: #555;
      margin-top: 0.5rem;
    }

    .style-card {
      min-height: 70vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding: clamp(2rem, 6vw, 6rem);
      position: relative;
    }

    .style-label {
      position: absolute;
      top: clamp(1rem, 2vh, 2rem);
      left: clamp(2rem, 6vw, 6rem);
      font-family: system-ui, sans-serif;
      font-size: clamp(0.75rem, 1vw, 0.875rem);
      letter-spacing: 0.08em;
      text-transform: uppercase;
      opacity: 0.6;
    }

    .style-vibe {
      font-family: system-ui, sans-serif;
      font-size: clamp(0.8rem, 1vw, 0.9rem);
      margin-top: 0.25rem;
      font-style: italic;
      text-transform: none;
      letter-spacing: 0;
    }

    /* Each card overrides these with its style's values */
    .style-card .hero-headline {
      line-height: 0.95;
      letter-spacing: -0.03em;
      text-wrap: balance;
      max-width: 14ch;
      margin-bottom: clamp(1rem, 2vw, 1.5rem);
    }

    .style-card .hero-sub {
      max-width: 42ch;
      line-height: 1.5;
      margin-bottom: clamp(1.5rem, 3vw, 2rem);
    }

    .style-card .hero-cta {
      display: inline-block;
      padding: 0.9em 2em;
      font-weight: 600;
      font-size: clamp(0.9rem, 1.1vw, 1rem);
      border: none;
      cursor: default;
      text-decoration: none;
    }

    .card-divider {
      height: clamp(2rem, 4vh, 4rem);
      background: #1a1a1a;
    }

    @media (prefers-reduced-motion: reduce) {
      * { animation: none !important; transition: none !important; }
    }
  </style>
</head>
<body>
  <div class="sampler-header">
    <h1>Style Preview — {Product Name}</h1>
    <p>Pick a direction. Say "Option 2" or "mix of 1 and 3" or describe what you want.</p>
  </div>

  <!-- Repeat this block for each style option -->
  <div class="style-card" style="
    background: var(--bg);
    color: var(--text);
    font-family: var(--font-body);
  ">
    <div class="style-label" style="color: var(--text-secondary);">
      Option N — Style Name
      <div class="style-vibe">one-line vibe description</div>
    </div>
    <h2 class="hero-headline" style="
      font-family: var(--font-display);
      font-size: clamp(2.5rem, 7vw, 5rem);
      color: var(--text);
    ">{Product's real headline}</h2>
    <p class="hero-sub" style="
      font-size: clamp(1rem, 1.4vw, 1.25rem);
      color: var(--text-secondary);
    ">{Product's real subheadline}</p>
    <div>
      <span class="hero-cta" style="
        background: var(--accent);
        color: var(--cta-text);
        border-radius: ...;
      ">Sample CTA</span>
    </div>
  </div>
  <div class="card-divider"></div>

  <!-- Next style card... -->

</body>
</html>
```

## Per-card overrides

Set CSS custom properties as inline styles on each `.style-card`:

```html
<div class="style-card" style="
  --bg: #f7f3ee;
  --text: #1c1917;
  --text-secondary: #57534e;
  --accent: #6b4f3a;
  --cta-text: #fff;
  --font-display: 'Playfair Display', serif;
  --font-body: 'Inter', sans-serif;
">
```

## What NOT to include

- No JavaScript
- No interactivity (buttons don't link anywhere)
- No full page sections beyond the hero preview
- No images or placeholders
- No footer or navigation
