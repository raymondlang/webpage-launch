# webpage-launch

A skill for Claude Code that reads your project folder and generates a distinctive one-page landing page — ready to open in a browser.

No templates. No build tools. No frameworks. Just one `index.html` with inline CSS and JS, crafted from your actual project.

## What it does

1. **Reads your project** — README, package.json, source files, docs, assets
2. **Shows you style options** — generates a visual sampler with 3-4 curated directions using your product's real headline and fonts
3. **Asks the right questions** — CTA, tone, constraints
4. **Generates `index.html`** — a complete, self-contained landing page

## Installation

### For Claude Code users

Copy the skill files to your Claude Code skills directory:

```bash
# Create the skill directory
mkdir -p ~/.claude/skills/webpage-launch

# Copy all files (or clone this repo directly)
cp SKILL.md styles.md style-sampler-template.md html-template.md viewport-baseline.css ~/.claude/skills/webpage-launch/
```

Or clone directly:

```bash
git clone https://github.com/raymondlang/webpage-launch.git ~/.claude/skills/webpage-launch
```

Then use it by typing `/webpage-launch` in Claude Code.

### As a Superpowers skill

```bash
git clone https://github.com/raymondlang/webpage-launch.git ~/.claude/skills/webpage-launch
```

## How to use

### Generate a landing page for any project

```
/webpage-launch
```

> "Generate a landing page for this project"

The skill will:

1. Read your project folder — README, package.json, source files, docs, assets
2. Summarize what it found and present its understanding of your product
3. Generate 3–4 visual style previews using your product's real headline and fonts
4. Open the style sampler in your browser so you can compare directions side by side
5. Ask about CTA, tone, and any constraints
6. Generate a complete `index.html` in your chosen style
7. Open it in your browser

### Start from an idea

```
/webpage-launch
```

> "I'm building a CLI tool for database migrations — make me a launch page"

The skill will work from your description, ask the right questions, and generate a page even without a full project folder.

### Revise

After generation, ask for targeted changes:

> "Make the hero darker and change the CTA to 'Start free trial'"

The skill makes surgical edits instead of regenerating the whole page.

## What you get

- A single `index.html` file — no dependencies, no build step
- Fonts loaded from Google Fonts or Fontshare
- Scroll-reveal animations, keyboard navigation, scroll progress bar
- Responsive from 320px to ultrawide
- `prefers-reduced-motion` support
- WCAG AA contrast compliance

## Files

| File | Purpose |
|------|---------|
| `SKILL.md` | Skill definition — the main instruction set |
| `styles.md` | 12 visual style presets with fonts, colors, and signature elements |
| `style-sampler-template.md` | Template for the visual style picker page |
| `html-template.md` | HTML output structure and runtime behavior reference |
| `viewport-baseline.css` | CSS baseline for viewport handling and responsive layout |

## Style presets

The skill includes 12 distinct visual directions:

1. **Institutional Clarity** — credible, calm, precise
2. **Product Precision** — sharp, intelligent, efficient
3. **Editorial Authority** — literate, thoughtful, high-taste
4. **Cinematic Immersion** — dramatic, immersive, ambitious
5. **Luxury Restraint** — elegant, expensive, controlled
6. **Playful Warmth** — friendly, energetic, welcoming
7. **Rebel Minimalism** — cool, opinionated, stripped-down
8. **Experimental Energy** — unexpected, kinetic, memorable
9. **Mission-Driven Humanism** — humane, sincere, hopeful
10. **Community Belonging** — social, magnetic, insider
11. **Technical Frontier** — advanced, rigorous, futuristic
12. **Conversion-Maximalist** — urgent, practical, persuasive

The skill picks 3–4 that fit your product and shows them visually before you commit.

## Philosophy

This skill was born from the belief that:

**You don't need a designer to ship a good landing page.** You just need to see real options and react to what you like.

**Dependencies are debt.** A single HTML file will work in 10 years. A React landing page from 2019? Good luck.

**Generic is forgettable.** Every landing page should feel like it was made for this product, not pulled from a template gallery.

**Show, don't ask.** Asking "do you want bold or minimal?" is useless. Showing two real previews side by side is a decision people can actually make.

## License

MIT
