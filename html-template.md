# One-Page Launch Output Standard

This is the generation contract for **instant launch pages**: single-page websites meant to explain a product fast, feel polished, and convert a user into a clear next step.

The generator should optimize for:
- immediate readability
- clean viewport behavior
- fast loading
- modular styling
- safe responsiveness
- optional editing only when explicitly enabled

## 1. Output Shell

Every generated page should ship as a **single one-page site** with a stable semantic structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Page Title</title>

  <!-- Preferred: Fontshare or Google Fonts -->
  <link rel="stylesheet" href="https://api.fontshare.com/v2/css?f[]=..." />

  <style>
    :root {
      /* Theme tokens */
      --bg-primary: #0a0f1c;
      --bg-secondary: #111827;
      --text-primary: #ffffff;
      --text-secondary: #9ca3af;
      --accent: #00d1ff;
      --border: rgba(255,255,255,0.08);

      /* Type scale */
      --font-display: 'Clash Display', sans-serif;
      --font-body: 'Satoshi', sans-serif;
      --display-size: clamp(2rem, 6vw, 5rem);
      --h2-size: clamp(1.25rem, 3vw, 2.25rem);
      --body-size: clamp(0.95rem, 1.2vw, 1.125rem);

      /* Layout scale */
      --section-x: clamp(1rem, 4vw, 2rem);
      --section-y: clamp(2.5rem, 8vh, 6rem);
      --gap: clamp(1rem, 2vw, 1.5rem);
      --radius: 16px;
    }

    /* Include viewport-baseline.css here */

    body {
      background: var(--bg-primary);
      color: var(--text-primary);
      font-family: var(--font-body);
    }
  </style>
</head>
<body>
  <header><!-- brand / nav --></header>

  <main>
    <section id="hero"></section>
    <section id="features"></section>
    <section id="proof"></section>
    <section id="showcase"></section>
    <section id="faq"></section>
    <section id="cta"></section>
  </main>

  <footer></footer>

  <script>
    // runtime controller goes here
  </script>
</body>
</html>
```

## 2. Section Contract

Each page should contain six core sections:

1. **Hero**  
   Clear promise, supporting line, primary CTA, optional secondary CTA, optional hero visual.

2. **Features**  
   Three to six benefits or capabilities. Keep scannable.

3. **Proof**  
   Metrics, testimonial, customer logos, or trust markers.

4. **Showcase**  
   Product screenshot, workflow preview, media frame, or explanatory visual.

5. **FAQ**  
   Three to six objections or clarifications.

6. **CTA**  
   Final action: waitlist, book demo, request access, subscribe, or buy.

This should be treated as a default scaffold, not a prison. Styles can change the look, but the page should still honor this narrative sequence.

## 3. Runtime Behavior

Every launch page should include a lightweight page controller.

### Required runtime responsibilities
- update a progress indicator on scroll
- manage section reveal states
- generate optional navigation dots
- support keyboard movement between major sections
- support touch-friendly scrolling behavior

### Runtime class pattern
```js
class LaunchRuntime {
  constructor() {
    this.sections = document.querySelectorAll('main section');
    this.init();
  }

  init() {
    this.setupRevealObserver();
    this.setupProgress();
    this.setupNavDots();
    this.setupKeyboard();
    this.setupTouch();
  }
}
```

### Reveal behavior
Use `IntersectionObserver` to add a `.visible` class when elements enter the viewport.  
This is the default trigger for transitions, counters, and low-cost motion.

## 4. Style and Motion Rules

The baseline system should control:
- containment
- scaling
- safe collapse
- image safety

The style layer should control:
- colors
- typefaces
- surface treatments
- decorative motifs
- motion personality

### Motion baseline
Use a simple reveal pattern by default:

```css
.reveal {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity 0.6s ease, transform 0.6s ease;
}

.visible {
  opacity: 1;
  transform: translateY(0);
}
```

Optional enhancements may include:
- parallax
- custom cursor
- magnetic buttons
- particles
- tilt effects
- animated counters

Only include these when they reinforce the chosen style.

## 5. Editing Mode

Editing must be **explicitly enabled**.  
If editing is off, generate no editing UI, CSS, or JS.

When enabled, use:
- a hidden entry point in the top-left corner
- a JS-managed toggle button
- localStorage autosave
- export/save support

Do **not** rely on CSS-only hover chains for the toggle reveal.  
Use JS with a short delay so the button remains clickable.

### Required interaction paths
- click the toggle
- hover into hotzone, then move to toggle
- press `E` to toggle edit mode
- use save/export shortcut only while editing

## 6. Asset Handling

If no images are provided, omit image processing entirely.

If images are provided:
- process them before HTML generation
- save processed versions with a new filename
- preserve originals
- use direct file paths, never base64 blobs
- place images into named slots only

### Recommended image slots
- `hero`
- `showcase`
- `proof`
- `logo`
- `og-image`

### Default rules
- screenshots: `object-fit: contain`
- atmospheric / brand imagery: `object-fit: cover`
- logos: preserve shape and don’t overscale
- missing image slot: collapse gracefully or swap in a styled placeholder

## 7. Code Standards

Comments should explain:
- what each block is for
- what can be customized
- what should not be removed

Do not over-comment obvious syntax.

Accessibility requirements:
- semantic landmarks
- visible focus states
- labeled controls and forms
- keyboard support
- reduced-motion support
- alt text for all non-decorative images
- 44px minimum interactive targets where practical

## 8. Delivery Format

### Smallest output
```txt
launch-page.html
assets/
```

### Preferred maintainable output
```txt
index.html
assets/
  hero.webp
  showcase.webp
css/
  viewport-baseline.css
  theme.css
js/
  launch-runtime.js
  inline-editor.js   # only if enabled
```

## 9. Core Product Principle

This generator is not a page builder.

It is a **structured launch-page engine** with:
- a stable narrative scaffold
- a small runtime layer
- optional enhancement modules
- optional editing mode
- clean separation between baseline layout and style expression

The base system should be boring.  
The style system should be expressive.
