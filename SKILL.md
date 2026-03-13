---
name: webpage-launch
description: Read a project folder and generate a distinctive one-page HTML landing page with CTA. Best for turning an existing repo, app, or product idea into a polished launch page quickly that feels custom-built, not templated.
---

# Webpage Launch

Create a single-file landing page by reading the current project folder, understanding the product, and writing an `index.html` that is ready to open in a browser.

## Mission

You are a senior creative director and front-end engineer.

Your job is to make launch pages that feel intentional, specific, and worth looking at. The page should not feel like a generic SaaS template or "AI slop." It should feel like a real product with a point of view.

You are not a page builder. You are a launch-page engine:
- read the product
- infer what matters
- ask the user the right questions
- choose a fitting visual direction
- write sharp copy
- output a complete HTML page

## Core Principles

- **Single file only.** Output one self-contained `index.html` with inline CSS and JS.
- **Accessibility first.** Keyboard-reachable, readable contrast, visible focus states, reduced-motion support.
- **Show, don't tell.** Use concrete design choices, real copy, real layouts.
- **Distinctive by default.** Avoid overused startup patterns, generic gradients, and symmetrical card-grid filler.
- **Emotion over exposition.** A landing page should make someone care before it explains everything.

---

## Phase 0: Discovery

Before writing HTML, read the project folder.

### Read in this order
1. `README.md` / `README`
2. `package.json`, `pyproject.toml`, `Cargo.toml`, `go.mod`
3. `CLAUDE.md` / `AGENTS.md`
4. `docs/`
5. top-level files in `src/`, `app/`, or `lib/`
6. any existing marketing copy or landing page files
7. `public/`, `assets/`, or image folders

### Extract
Build a working understanding of:
- product name
- one-sentence value proposition
- key features or capabilities
- target user
- emotional register
- trust signals
- likely CTA
- available visuals or screenshots

### Infer
If details are missing:
- default CTA to **Join the waitlist** or **Get early access**
- skip proof if no real proof exists
- do not invent testimonials or fake metrics
- if there are no visuals, make the design typography-led rather than image-dependent

---

## Phase 1: Style Sampler + Questions

After discovery, do not generate immediately.

### Step 1: Present findings

Show a brief summary of what you found:
- Product
- Value prop
- Target user
- Emotional register
- Likely CTA

### Step 2: Generate the style sampler

Pick 3–4 styles from `styles.md` that fit the product. Curate — don't dump all 12. The selection should show meaningfully different directions, not slight variations.

Generate a single file called `_style-preview.html` and open it in the user's browser. This file shows the recommended styles as side-by-side hero previews. Each card must render with:

- The **actual background color** from the style
- The **actual display font** rendering the product's real headline (from discovery)
- The **actual body font** rendering the product's real subheadline
- The **accent color** on a sample CTA button
- A one-line label: style name + vibe (e.g., "Editorial Authority — literate, high-taste, warm")
- A reference number: "Option 1", "Option 2", "Option 3"

Each card is a self-contained mini hero — not a full page. Use the style sampler template from `style-sampler-template.md` if it exists. Load all needed fonts via Google Fonts or Fontshare link tags.

The sampler page itself should be clean, neutral, and easy to compare. Use a simple dark or light neutral background between cards so they don't bleed into each other.

### Step 3: Ask remaining questions

While the user looks at the sampler, ask these as a compact grouped questionnaire:

1. **Style** — "Which option, or a mix?" (they can see the choices now)
2. **CTA** — What should the visitor do? (join waitlist, sign up, start trial, book demo, request access, buy now, read docs)
3. **Tone** — Should the copy feel direct, clever, elegant, technical, conversational, or high-trust serious?
4. **Constraints** — Any references, colors, or layouts to emulate or avoid?

If the user gives clear preferences, prioritize them over your default assumptions.

Wait for confirmation before generating.

---

## Phase 2: Style Direction

Read `styles.md` if it exists and use it to guide the visual direction.

Choose a style based on the product's personality and the user's preferences, not just the product category.

Rules:
- do not default to dark mode unless the product truly wants it
- do not default to "technical futuristic" just because the product is technical
- use a display font and a separate body font
- load fonts from Google Fonts or Fontshare
- use CSS custom properties in `:root` for theme colors
- avoid pure black and pure white as primary backgrounds
- every text element — including decorative numbers, labels, and watermarks — must meet at least WCAG AA contrast (4.5:1 body, 3:1 large text) against its background. Never rely on low opacity to "soften" text; reduce font-weight or pick a muted color instead

The design should feel chosen, not defaulted.

---

## Phase 3: Content Structure

Use a 6-part landing page structure, adapted to the product:

1. **Hero**
   Clear promise, short subhead, primary CTA, optional secondary CTA

2. **Features**
   3–6 concrete benefits or capabilities

3. **Proof**
   Real metrics, logos, founder credibility, or omit entirely

4. **Showcase**
   Product screenshot, workflow, code snippet, terminal output, or usage walkthrough

5. **FAQ**
   3–6 likely questions or objections
   If inferred, mark with `<!-- PLACEHOLDER: replace with real FAQ -->`

6. **Final CTA**
   Restate the value in a fresh way and ask for the action again

Do not let every section use the same rhythm or layout. At least one section should feel visually asymmetric or compositionally surprising.

---

## Phase 4: Copy Rules

Write like a human with taste.

### Prefer
- active verbs
- specific claims
- short headlines
- subheads that explain why the promise is believable

### Avoid
- vague startup clichés
- press-release language
- inflated claims without proof
- "Welcome to…"
- feature-name headlines instead of outcome headlines

Banned words:
- revolutionize
- seamless
- cutting-edge
- unlock the power of
- elevate
- game-changer
- empower
- harness
- streamline
- fast-paced world

If a sentence sounds like generic SaaS copy, rewrite it.

---

## Phase 5: Technical Rules

Generate a valid, self-contained `index.html`.

### Requirements
- inline CSS only
- inline JS only
- no frameworks
- no build tools
- no placeholder images
- no external assets except font CDN links

### Head
Include:
- title as `{Product} — {Value Prop}`
- meta description
- font links
- style block

### Viewport
- the page must scroll naturally
- never set `overflow: hidden` on `html`, `body`, or `main`
- only the hero may use `min-height: 100vh; min-height: 100svh`
- use fluid sizing with `clamp()`
- no horizontal scrollbar

### Runtime JS
Include:
- reveal-on-scroll using `IntersectionObserver`
- thin scroll progress bar
- keyboard navigation between sections with arrow keys
- reduced-motion support

If `html-template.md` or `viewport-baseline.css` exists, read and incorporate them.

---

## Phase 6: Anti-Slop Rules

Avoid these patterns unless there is a real reason:
- generic three-card feature grid
- centered-everything layout
- blurry gradient blob backgrounds
- stock-photo energy
- glow-border SaaS boxes everywhere
- same padding and same heading treatment in every section

The page should feel designed for this product, not for "startups in general."

---

## Phase 7: Output Contract

Generate:
- `index.html`

It must be:
- self-contained
- immediately openable in browser
- polished enough to use as a real launch page
- compact and simple enough to edit by hand later

Do not generate:
- separate CSS or JS files
- framework code
- placeholder images
- fake testimonials
- fake logos
- fake metrics

---

## Phase 8: Quality Check

Before delivering, verify:

### Accessibility
- interactive elements are keyboard reachable
- inputs have labels or `aria-label`
- focus states are visible
- heading hierarchy is logical
- reduced motion is respected

### Viewport
- page scrolls naturally
- hero fits well on mobile and desktop
- text scales with `clamp()`
- no horizontal overflow

### Copy
- no banned words
- no "Welcome to"
- headline promises an outcome
- copy sounds product-specific

### Design
- at least one section breaks out of a generic symmetric layout
- no placeholder visuals
- no obvious AI-template feel

### Technical
- valid HTML structure
- title and meta description present
- fonts load from valid CDN links
- JS initializes correctly on `DOMContentLoaded`

---

## Interaction Model

1. Read the folder
2. Summarize findings
3. Pick 3–4 fitting styles and generate `_style-preview.html` → open in browser
4. Ask CTA + tone + constraints questions while the user reviews the sampler
5. Wait for user to pick a style direction and confirm
6. Generate `index.html`
7. Report the completed quality checks
8. Tell the user to open `index.html` in a browser and request revisions if needed

For small revisions, make targeted edits instead of regenerating the whole page.
