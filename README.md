# webpage-launch

A skill for Claude Code that reads your project folder and generates a distinctive one-page landing page — ready to open in a browser.

No templates. No build tools. No frameworks. Just one `index.html` with inline CSS and JS, crafted from your actual project.

## What it does

1. **Reads your project** — README, package.json, source files, docs, assets
2. **Shows you style options** — generates a visual sampler with 3-4 curated directions using your product's real headline and fonts
3. **Asks the right questions** — CTA, tone, constraints
4. **Generates `index.html`** — a complete, self-contained landing page

## Install

### As a Claude Code skill

Add this repo as a skill in your Claude Code configuration:

```bash
claude skill add webpage-launch https://github.com/raymondlang/webpage-launch
```

### As a Superpowers skill

Install via the Superpowers skill registry:

```bash
# Add to your superpowers skills directory
git clone https://github.com/raymondlang/webpage-launch.git ~/.claude/skills/webpage-launch
```

### Manual

Clone the repo and reference the `SKILL.md` file directly.

## Usage

Navigate to any project folder and invoke the skill:

```
/webpage-launch
```

Or ask Claude Code directly:

> "Generate a landing page for this project"

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

The skill picks 3-4 that fit your product and shows them visually before you commit.

## License

MIT
