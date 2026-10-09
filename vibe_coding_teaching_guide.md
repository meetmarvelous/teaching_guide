# Vibe Coding & Modern Web Architecture
### A Field Guide to Directing AI for Production-Ready Web Interfaces

Building modern web projects with AI is not about letting a model guess blindly—it is about acting as the **Product Architect and Code Director**, steering generation with precise specifications, design systems, and systematic review to produce production-grade code.

---

## 1. Core Principles Before Writing the First Prompt

Before generating code, establish the foundational rules that separate amateur output from clean, professional web design.

### The Mental Shift: From Coder to Technical Director
* **Avoid Monolithic Prompts:** Never ask for an entire website in a single prompt. Doing so produces generic templates, inconsistent styling, and fragile layout structures.
* **Think in Component Layers:** Direct the build layer by layer:
  Tokens & Global Setup → Layout Shell → Section Content → Interactions & Polish
* **Act as the Quality Inspector:** You remain responsible for semantic markup, valid linking, accessibility, and responsive breakpoints.

### Visual Design Fundamentals
High-converting, polished web interfaces follow strict aesthetic systems to enforce during prompting:

* **The 60-30-10 Color Rule:**
  * **60% Dominant Neutral:** Backgrounds and main canvases (e.g., `#0a0a0c` dark slate or `#f9fafb` off-white).
  * **30% Structural Secondary:** Card surfaces, navigation bars, borders, and modal layers.
  * **10% High-Contrast Accent:** Reserved strictly for primary call-to-action (CTA) buttons, active badges, and focus rings.
* **Mathematical Spacing Scale:**
  * Mandate consistent spatial rhythm using multiples of 4px or 8px (`8px`, `16px`, `24px`, `32px`, `48px`, `64px`, `80px`).
  * Enforce consistent layout padding rather than arbitrary pixel values.
* **Typographic Hierarchy:**
  * Limit the design to a maximum of two font families (e.g., a display font for headers and a legible sans-serif for body copy).
  * Explicitly specify line heights (`1.1` to `1.2` for display headings, `1.5` to `1.6` for long-form body text) and font weights (`400` body, `600` subheadings, `700`–`800` hero titles).
* **Depth & Surface Treatment:**
  * Avoid heavy, blurry drop shadows.
  * Mandate subtle translucent borders (`border: 1px solid rgba(255, 255, 255, 0.08)`) and soft ambient shadows.

### Web Architecture & Modern Best Practices
* **Semantic HTML5:** Prompts must require `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, and `<footer>` rather than uncontrolled `<div>` nesting.
* **Fluid Layouts:** Mandate modern CSS units (`rem`, `ch`, `%`, `clamp()`) and CSS Grid / Flexbox over fixed pixel widths.
* **Performance & Media Handling:** Use modern image formats (WebP, AVIF), set explicit width and height attributes to eliminate Cumulative Layout Shift (CLS), and use SVG for clean, scalable icons.
* **Accessibility (WCAG AA Standard):**
  * All `<img>` tags must include descriptive `alt` attributes.
  * Contrast ratios must meet standard thresholds (minimum 4.5:1 for normal text).
  * Interactive elements must feature visible `:focus-visible` outlines.
  * Buttons must be native `<button>` elements, not clickable `<div>` tags.

---

## 2. Anatomy of a High-Impact Landing Page / Portfolio

Plan your site around this modular architecture before writing a single prompt:

| Section | Role & Strategic Objective | Key Technical & Design Requirements |
| :--- | :--- | :--- |
| **Sticky Navigation** | Instant orientation & branding | Brand mark/name, 3–4 anchor links, 1 primary action button, translucent background (`backdrop-filter: blur(12px)`). |
| **Hero Section** | Value proposition above the fold | Single bold headline (H1), 2-sentence explanatory copy, dual CTA group (Primary + Secondary), high-impact showcase visual. |
| **Social Proof / Metrics** | Trust verification | Stat counter grid (e.g., "3+ Projects Shipped", "99.9% Performance") or tool/client badges in subdued monochrome. |
| **Core Showcase (Work / Products)** | Primary deliverable | 2–3 column responsive CSS Grid of cards, category tags/pills, subtle hover micro-interactions (`transform: translateY(-4px)`). |
| **Highlight / About** | Story and technical context | Asymmetric two-column layout (editorial narrative on one side, skill badge matrix or interactive preview on the other). |
| **Contact / Final CTA** | Direct conversion | Streamlined form or high-visibility email link card with clear next steps. |
| **Footer** | Wayfinding & legal baseline | Copyright notice, secondary links, social SVG icons, clean top border boundary. |

---

## 3. The 4-Step Prompting Framework (R-C-S-O)

Structure every prompt using the **R-C-S-O Framework** to eliminate generic outputs:

```text
[Role]       Act as a senior frontend engineer and UI/UX designer.
[Context]    I am building a [developer portfolio / product landing page] for [target audience/niche].
[Specs]      - Visual style: [Dark mode minimal / Clean modern Swiss / Bold editorial]
             - Typography: [Inter & Space Grotesk via Google Fonts]
             - Spacing & Layout: [CSS Grid / Flexbox, container max-width 1200px, 8px spacing rhythm]
             - Semantic rules: [Semantic HTML5 tags, accessible contrast, BEM naming or clean CSS classes]
[Output]     Provide production-ready [HTML / CSS] code strictly for the [specific section]. Include explanatory comments.
```

---

## 4. End-to-End Build Workflow

### Phase 1: Pre-Prompt Blueprinting
1. **Define the Concept:** Choose between a Personal Developer Portfolio, a Micro-SaaS Landing Page, or a Product Showcase.
2. **Establish the Palette:** Select primary, background, card, border, and accent colors.
3. **Draft the Section Sequence:** Write out the exact visual flow:
   Nav → Hero → Metrics → Showcase → About → Contact → Footer

### Phase 2: Design Tokens & Base Setup
* Direct the model to generate a unified `:root` stylesheet containing:
  * Color variables (`--bg-primary`, `--bg-surface`, `--accent`, `--text-main`, `--text-muted`).
  * Font families and responsive font scales.
  * Universal CSS box-sizing resets and baseline container constraints.
* Verify the base configuration locally in the browser before moving forward.

### Phase 3: Incremental Section Builds
* **Strict Rule:** Complete, review, and test each section before requesting the next one.
* Feed existing class names and CSS variables back into the prompt so the model maintains architectural consistency across every section.

### Phase 4: Mobile Verification & Polish
* Resize the browser viewport down to 375px (mobile breakpoint) to detect layout clipping, horizontal scrollbars, or text overflow.
* Request targeted CSS micro-interactions:
  * Smooth transitions (`transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);`).
  * Hover elevations and focus rings for keyboard navigation.
* Verify that all links, buttons, and asset paths are valid and functional.