# Style Presets

Curated visual styles for launch pages and product stories. Each preset is designed to create a distinct emotional response — no generic “AI slop” aesthetics. **Abstract shapes only where decoration is needed — no illustrations unless explicitly intended.**

---

## 1. Institutional Clarity

**Vibe:** Credible, calm, precise

**Layout:** Structured grid with strong horizontal bands. Hero content left-aligned, trust signals and proof blocks distributed in clean rows.

**Typography:**
- Display: `Inter` (700)
- Body: `Source Serif 4` (400/500)

**Colors:**
```css
:root {
    --bg-primary: #f8fafc;
    --bg-surface: #e2e8f0;
    --text-primary: #0f172a;
    --text-secondary: #475569;
    --accent-blue: #2563eb;
    --accent-sky: #0ea5e9;
}
```

**Signature Elements:**
- Visible grid alignment
- Trust-logo bands
- Restrained line icons
- Structured proof/stat modules
- Thin section dividers for orderly pacing

**Failure Mode:**
- Feels generic, soulless, and indistinguishable from a template-heavy B2B site

---

## 2. Product Precision

**Vibe:** Sharp, intelligent, efficient

**Layout:** Dense but controlled product-marketing layout. Hero with interface screenshot, followed by modular feature rows and conversion blocks.

**Typography:**
- Display: `Geist` (700) — fallback: `Cabinet Grotesk` (Fontshare) or `Inter` (Google Fonts)
- Body: `IBM Plex Sans` (400/500)

**Colors:**
```css
:root {
    --bg-primary: #ffffff;
    --bg-surface: #f3f4f6;
    --text-primary: #111827;
    --text-secondary: #4b5563;
    --accent-violet: #7c3aed;
    --accent-cyan: #06b6d4;
}
```

**Signature Elements:**
- Product UI screenshots
- Feature comparison cards
- Subtle gradient glows
- Annotated interface callouts
- Repeated CTA rhythm throughout the page

**Failure Mode:**
- Looks like every other modern SaaS page and explains features without creating any emotional pull

---

## 3. Editorial Authority

**Vibe:** Literate, thoughtful, high-taste

**Layout:** Editorial column structure with generous margins. Asymmetric placement of text blocks, pull quotes, and supporting content.

**Typography:**
- Display: `Canela` (500/600) — fallback: `Playfair Display` (Google Fonts)
- Body: `Neue Haas Grotesk Text` (400/500) — fallback: `DM Sans` (Google Fonts)

**Colors:**
```css
:root {
    --bg-primary: #f7f3ee;
    --bg-surface: #ede7df;
    --text-primary: #1c1917;
    --text-secondary: #57534e;
    --accent-brown: #6b4f3a;
    --accent-rust: #7c2d12;
}
```

**Signature Elements:**
- Asymmetric editorial layout
- Oversized pull quotes
- Caption-style metadata
- Elegant section dividers
- Generous whitespace around long-form text

**Failure Mode:**
- Feels pretentious, slow, and too text-heavy to hold attention

---

## 4. Cinematic Immersion

**Vibe:** Dramatic, immersive, ambitious

**Layout:** Scene-based storytelling with large viewport sections. Content unfolds as chapters, with dramatic visual transitions and controlled pacing.

**Typography:**
- Display: `Satoshi` (700/900) — available on Fontshare
- Body: `PP Neue Montreal` (400/500) — fallback: `Satoshi` (Fontshare) or `Inter` (Google Fonts)

**Colors:**
```css
:root {
    --bg-primary: #050816;
    --bg-surface: #111827;
    --text-primary: #f5f3ff;
    --text-secondary: #c4b5fd;
    --accent-lavender: #c084fc;
    --accent-blue: #60a5fa;
}
```

**Signature Elements:**
- Full-bleed visual scenes
- Layered parallax depth
- Chapter-like scroll reveals
- Atmospheric gradient lighting
- Oversized headline moments with dramatic spacing

**Failure Mode:**
- Becomes all spectacle and no substance, with motion overwhelming clarity

---

## 5. Luxury Restraint

**Vibe:** Elegant, expensive, controlled

**Layout:** Sparse composition with large negative space. Strong image hierarchy and minimal copy, with a slow, deliberate reading rhythm.

**Typography:**
- Display: `Didot` (700) — fallback: `Playfair Display` (Google Fonts) or `Cormorant Garamond` (Google Fonts)
- Body: `Suisse Int’l` (400/500) — fallback: `Inter` (Google Fonts)

**Colors:**
```css
:root {
    --bg-primary: #f5f1eb;
    --bg-surface: #e7dfd4;
    --text-primary: #111111;
    --text-secondary: #6b7280;
    --accent-gold: #b79b6c;
    --accent-bronze: #8b6f47;
}
```

**Signature Elements:**
- Large negative space
- Art-directed photography
- Refined micro-hover transitions
- Tightly cropped image framing
- Minimal navigation with quiet confidence

**Failure Mode:**
- Feels empty, inaccessible, and overly reliant on aesthetic signaling

---

## 6. Playful Warmth

**Vibe:** Friendly, energetic, welcoming

**Layout:** Rounded modular layout with light asymmetry. Clear sections, soft containers, and visual rhythm that feels open and easy.

**Typography:**
- Display: `DM Sans` (700/800)
- Body: `Nunito` (400/500)

**Colors:**
```css
:root {
    --bg-primary: #fff7ed;
    --bg-surface: #fde68a;
    --text-primary: #7c2d12;
    --text-secondary: #9a3412;
    --accent-coral: #fb7185;
    --accent-green: #22c55e;
}
```

**Signature Elements:**
- Rounded cards
- Expressive illustrations or abstract shapes
- Bouncy micro-interactions
- Layered color-block sections
- Soft shadowing that keeps everything approachable

**Failure Mode:**
- Feels childish, noisy, or unserious for higher-trust products

---

## 7. Rebel Minimalism

**Vibe:** Cool, opinionated, stripped-down

**Layout:** Hard-edged, reduced layout with oversized type and very few elements per screen. Strong pacing through omission.

**Typography:**
- Display: `Space Grotesk` (700)
- Body: `Instrument Serif` (400)

**Colors:**
```css
:root {
    --bg-primary: #fafaf9;
    --bg-surface: #e7e5e4;
    --text-primary: #0a0a0a;
    --text-secondary: #57534e;
    --accent-magenta: #e11d48;
    --accent-gray: #a3a3a3;
}
```

**Signature Elements:**
- Oversized typography
- Brutal whitespace
- Raw image crops
- Hard-edge section transitions
- Sparse navigation with almost no explanatory scaffolding

**Failure Mode:**
- Feels underbuilt, cold, and like taste is being used to hide weak content

---

## 8. Experimental Energy

**Vibe:** Unexpected, kinetic, memorable

**Layout:** Broken-grid composition with surprise moments. Sections feel intentionally irregular, but still controlled enough to navigate.

**Typography:**
- Display: `Monument Extended` (700) — fallback: `Syne` (Google Fonts) or `Clash Display` (Fontshare)
- Body: `ABC Diatype` (400/500) — fallback: `Space Grotesk` (Google Fonts)

**Colors:**
```css
:root {
    --bg-primary: #111111;
    --bg-surface: #1f2937;
    --text-primary: #f9fafb;
    --text-secondary: #d1d5db;
    --accent-lime: #d9ff3f;
    --accent-cyan: #00c2ff;
}
```

**Signature Elements:**
- Broken grid compositions
- Kinetic type treatments
- Surprising cursor interactions
- Animated geometric interruptions
- Unconventional transitions between sections

**Failure Mode:**
- Feels gimmicky, exhausting, and harder to use than it is worth

---

## 9. Mission-Driven Humanism

**Vibe:** Humane, sincere, hopeful

**Layout:** Story-led layout with emotional hierarchy. Human stories, impact proof, and softer section transitions carry the structure.

**Typography:**
- Display: `Public Sans` (700)
- Body: `Source Serif 4` (400/500)

**Colors:**
```css
:root {
    --bg-primary: #f4f1ea;
    --bg-surface: #dde5d8;
    --text-primary: #2f3e46;
    --text-secondary: #52796f;
    --accent-green: #5e8b7e;
    --accent-terracotta: #e07a5f;
}
```

**Signature Elements:**
- Documentary-style photography
- Impact-stat callouts
- Testimonial story blocks
- Soft organic section shapes
- Warm dividers and content framing that feel human, not corporate

**Failure Mode:**
- Feels nonprofit-generic or emotionally manipulative rather than genuinely moving

---

## 10. Community Belonging

**Vibe:** Social, magnetic, insider

**Layout:** Poster-inspired modular layout with punchy section breaks. High-energy proof and participation cues appear throughout.

**Typography:**
- Display: `Archivo Black` (900)
- Body: `Inter` (400/500)

**Colors:**
```css
:root {
    --bg-primary: #fff8e7;
    --bg-surface: #fde68a;
    --text-primary: #1f2937;
    --text-secondary: #4b5563;
    --accent-purple: #7c3aed;
    --accent-orange: #f97316;
}
```

**Signature Elements:**
- User-photo mosaics
- Slogan-driven section breaks
- Layered sticker-like graphics
- Event-poster inspired blocks
- Repeated signs of participation and member identity

**Failure Mode:**
- Feels try-hard, forced, or like fake community theater

---

## 11. Technical Frontier

**Vibe:** Advanced, rigorous, futuristic

**Layout:** Systems-oriented layout with clear modules, diagrams, and technical storytelling moments. Dense, but organized.

**Typography:**
- Display: `IBM Plex Sans` (700)
- Body: `IBM Plex Mono` (400/500)

**Colors:**
```css
:root {
    --bg-primary: #0a0f1c;
    --bg-surface: #111827;
    --text-primary: #dce7f7;
    --text-secondary: #94a3b8;
    --accent-cyan: #00d1ff;
    --accent-violet: #7c3aed;
}
```

**Signature Elements:**
- System diagrams
- Scan-line overlays
- Grid-based technical illustrations
- Blinking cursor or live-terminal motifs
- Layered schematic backgrounds for depth

**Failure Mode:**
- Feels sterile, buzzwordy, or like fake sci-fi for venture tourists

---

## 12. Conversion-Maximalist Direct Response

**Vibe:** Urgent, practical, persuasive

**Layout:** Outcome-first landing page layout with stacked conversion sections, repeated CTAs, and objection-handling blocks.

**Typography:**
- Display: `Helvetica Now Display` (700) — fallback: `Inter` (Google Fonts) or system `-apple-system, 'Helvetica Neue'`
- Body: `Arial` (400/700) — system font, universally available

**Colors:**
```css
:root {
    --bg-primary: #ffffff;
    --bg-surface: #f3f4f6;
    --text-primary: #111827;
    --text-secondary: #374151;
    --accent-red: #dc2626;
    --accent-blue: #2563eb;
}
```

**Signature Elements:**
- Repeated CTA blocks
- Objection-handling FAQ bands
- Benefit-first comparison sections
- High-contrast offer banners
- Tight scanning structure with bold emphasis points

**Failure Mode:**
- Feels spammy, loud, and optimized so hard for action that trust collapses

---

## Best combinations

- **Institutional Clarity + Product Precision** for serious B2B, healthcare, fintech, infrastructure
- **Editorial Authority + Luxury Restraint** for premium consulting, founder brands, thoughtful products
- **Technical Frontier + Cinematic Immersion** for AI, frontier tech, products that need to feel consequential
- **Community Belonging + Playful Warmth** for consumer, events, creator tools, social products
- **Conversion-Maximalist + Product Precision** for landing pages that need to sign people up without looking cheap

## Core principle

**Colors set the emotional temperature, typography sets the social status, and signature elements set the behavioral feel.**
