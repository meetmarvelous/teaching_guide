# Web Design Prompt Workbook: 3 Real-World Projects
### Production-Ready Prompt Sequences (R-C-S-O Framework)

This workbook contains battle-tested prompt sequences for three distinct web projects. Every prompt adheres to the **R-C-S-O Framework** (`Role`, `Context`, `Specifications`, `Output`) to ensure clean, semantic, and production-ready HTML/CSS.

---

## How to Use This Workbook

1. **Follow the Sequence:** Build incrementally from Step 1 through Step 5 without skipping.
2. **Customize Parameters:** Copy each prompt and adjust bracketed tokens `[...]` to match your desired branding, copy, or assets.
3. **Test in the Browser:** Verify each section locally (desktop and mobile responsive views) before requesting the next section.
4. **Maintain Architectural Context:** Keep the same conversation thread or pass existing class names forward so the model preserves your CSS variables and layout hierarchy.

---

## Project 1: Developer Portfolio (Dark Mode Minimal)
**Aesthetic:** Deep slate background, high-contrast typography, electric cyan accents, subtle borders, and monospace details.

---

### Step 1: Base Design System & CSS Variables

```text
[Role] Act as a senior frontend engineer and modern web designer.

[Context] I am starting a modern, dark-themed personal portfolio for a junior frontend and web developer. I need the foundation setup before building any visible sections.

[Specs]
- Do a clean CSS reset.
- Import two Google Fonts: "Plus Jakarta Sans" for primary UI and "JetBrains Mono" for code accents and tags.
- Define a :root CSS variable palette:
  * Background: deep charcoal (#0a0d12)
  * Surface card background: slightly lighter dark (#121721)
  * Border color: subtle translucent white (rgba(255, 255, 255, 0.08))
  * Text primary: crisp off-white (#f3f4f6)
  * Text muted: neutral slate (#94a3b8)
  * Primary accent: electric cyan (#06b6d4)
- Define standard container constraints (max-width: 1120px; margin: 0 auto; padding: 0 1.5rem).

[Output] Provide only the starter index.html head setup and the base styles.css code including the :root variables and body reset.
```

---

### Step 2: Sticky Header & Navigation

```text
[Role] Act as a senior UI engineer.

[Context] I am adding the global top navigation to my developer portfolio using the design tokens we just defined.

[Specs]
- Use semantic <header> and <nav> tags.
- Layout: Fixed or sticky top bar with backdrop-filter blur (12px) and a bottom border matching our border variable.
- Left side: Logo/Branding with my name and a small glowing green dot indicating "Available for work".
- Center/Right side: 4 anchor links ("About", "Projects", "Skills", "Contact") with smooth hover transitions.
- Right end: High-contrast button linking to my resume/CV ("Download CV").
- Mobile: Flex wrap or clean layout that collapses cleanly on screens under 768px.

[Output] Provide the semantic HTML snippet for the header and the accompanying CSS rules.
```

---

### Step 3: High-Impact Hero Section

```text
[Role] Act as a creative director and frontend specialist.

[Context] I need the above-the-fold Hero section for my developer portfolio to immediately introduce who I am and what I build.

[Specs]
- Use semantic <header> or <section class="hero">.
- Pill badge at the top: Monospace font saying "Frontend Engineer & Interface Builder".
- Main Headline (H1): Bold, large clamp font size (clamp(2.5rem, 6vw, 4.5rem)), high-impact copy such as "Crafting clean, accessible, and high-performance digital experiences."
- Subtext: 2 sentences explaining my tech focus (HTML, CSS, JavaScript, responsive UI).
- Call-to-actions: Primary solid cyan button ("View My Work" jumping to #projects) and a secondary ghost button with border ("Get in Touch").
- Add a subtle background radial gradient glow behind the text without using external images.

[Output] Provide the clean HTML section code and the matching CSS rules.
```

---

### Step 4: Featured Projects Grid

```text
[Role] Act as a frontend developer.

[Context] I need the "Projects" showcase section for my portfolio.

[Specs]
- Section title (H2) with a small uppercase subtitle ("Featured Projects").
- Layout: CSS Grid (1 column on mobile, 2 columns on desktop) with a 24px gap.
- Create 3 sample project cards:
  * Each card has an aspect-ratio container for a screenshot mockup (use high quality Unsplash tech placeholder).
  * Project title (H3) and a 2-line description of the challenge solved.
  * Tag pills using JetBrains Mono (e.g., "HTML5", "CSS Grid", "JavaScript").
  * Action row at the bottom with two text links with subtle arrow hover animations: "Live Preview ↗" and "Source Code".
- Cards must have surface background, 1px subtle border, rounded corners (12px), and a smooth lift effect on hover (transform: translateY(-4px)).

[Output] Provide the semantic HTML markup and complete CSS styling.
```

---

### Step 5: Contact CTA & Footer

```text
[Role] Act as a frontend developer and accessibility reviewer.

[Context] I need the final closing section and footer to encourage visitors to reach out.

[Specs]
- Section: "Let's Build Something Together" with a short encouraging paragraph.
- Large direct contact email button (mailto link) styled like a prominent CTA.
- Footer with semantic <footer> tag:
  * Top border separating it from the main content.
  * Flexbox layout with copyright notice on the left and social media links (GitHub, LinkedIn, Twitter/X) on the right.
  * Ensure full keyboard accessibility (:focus-visible styling on all links).

[Output] Provide the HTML and CSS snippets.
```

---

## Project 2: SaaS Landing Page ("TaskFlow")
**Aesthetic:** Clean light mode, electric indigo primary accent, modern card elevations, and conversion-focused copy.

---

### Step 1: Design Tokens & Typography

```text
[Role] Act as a product designer and frontend engineer.

[Context] I am building a conversion-focused landing page for a fictional SaaS productivity tool called "TaskFlow".

[Specs]
- Setup CSS reset and modern typography using Google Fonts "Inter".
- Color system in :root:
  * Pure white background (#ffffff) and subtle off-white section background (#f8fafc)
  * Text primary: deep slate (#0f172a)
  * Text secondary: neutral muted (#64748b)
  * Primary brand color: electric indigo (#6366f1) with a hover state (#4f46e5)
  * Card border: 1px solid #e2e8f0
- Fluid sizing scale and standard button styling classes (.btn-primary, .btn-secondary).

[Output] Provide the starter HTML shell and the CSS tokens/global styles.
```

---

### Step 2: Hero Section with Mockup & Social Proof

```text
[Role] Act as a growth engineer and frontend designer.

[Context] I am building the Hero section for the TaskFlow landing page to drive signups.

[Specs]
- Centered layout with maximum width of 800px for text.
- Notification chip: "✨ Version 2.0 is now live — Read updates".
- Headline: "Manage team workflows without the busywork."
- Supporting paragraph explaining automated task management.
- Email capture input group: An inline text input + "Start Free Trial" button on desktop, stacking cleanly on mobile.
- Trust badge below: "No credit card required • 14-day free trial".
- Hero graphic container: A clean CSS mockup window with faux browser dots (red, yellow, green) and an interface preview card inside.

[Output] Provide the HTML structure and CSS.
```

---

### Step 3: Key Features (3-Column Grid)

```text
[Role] Act as a UI engineer.

[Context] I need the core feature breakdown section for the TaskFlow landing page.

[Specs]
- Section heading: "Everything you need to ship faster", with center-aligned subtext.
- CSS Grid with 3 equal columns on desktop (repeat(3, 1fr)), collapsing to 1 column on mobile (<768px).
- 3 feature cards:
  * 1: "Real-time Sync" (Icon placeholder or SVG, bold title, benefit description).
  * 2: "Automated Workflows" (Icon, bold title, benefit description).
  * 3: "Enterprise Security" (Icon, bold title, benefit description).
- Visual treatment: Light background, subtle box-shadow (0 4px 6px -1px rgba(0, 0, 0, 0.05)), rounded corners (16px), 24px internal padding.

[Output] Provide the semantic HTML section and the responsive CSS.
```

---

### Step 4: Simple Pricing Tier Cards

```text
[Role] Act as a frontend developer specializing in ecommerce/SaaS layouts.

[Context] I am creating the pricing table section for TaskFlow.

[Specs]
- 2-tier comparison card layout: "Starter" ($0/mo) and "Pro" ($29/mo).
- Highlight the "Pro" card visually with a "Most Popular" badge, an indigo border, and a slight scale boost.
- Inside each card:
  * Tier name, price with /month cadence, and target user summary.
  * Bulleted feature checklist using custom checkmark styling (green checkmarks).
  * Action button: Secondary button for Starter, Primary solid indigo for Pro.
- Ensure cards are equal height using Flexbox stretch or CSS Grid.

[Output] Provide the HTML code and CSS rules.
```

---

### Step 5: Accordion FAQ & Final CTA Banner

```text
[Role] Act as a frontend developer.

[Context] I need the closing section of the SaaS landing page with frequently asked questions and a final banner CTA.

[Specs]
- Final CTA banner: Indigo background container with rounded edges, high-contrast white text, and a white button ("Get Started Today").
- FAQ list using semantic HTML: Use native HTML5 <details> and <summary> tags for 3 accordion questions (no JavaScript needed).
- Style the <details> and <summary> elements with clean borders, cursor pointers, and padding so they look like modern interactive cards.

[Output] Provide the semantic HTML snippet and CSS.
```

---

## Project 3: Boutique Cafe / Local Business Showcase
**Aesthetic:** Warm cream canvas, espresso dark brown type, terracotta accents, Playfair Display serifs, and high-impact photography.

---

### Step 1: Editorial Aesthetic & Variables

```text
[Role] Act as a creative frontend developer and editorial designer.

[Context] I am building a landing page for an artisanal specialty cafe called "Roast & Grain".

[Specs]
- Import Google Fonts: "Playfair Display" (serif for elegant headings) and "Plus Jakarta Sans" (clean sans-serif for body reading).
- Define warm, organic CSS variables in :root:
  * Background: warm cream / oatmeal (#fcfaf7)
  * Surface container: warm ivory (#f5f0ea)
  * Primary text: espresso dark brown (#231b15)
  * Secondary text: roasted mocha (#5c4d43)
  * Accent brand: terracotta / warm amber (#c86d51)
  * Border line: subtle sand tone (#e7ded3)
- Setup default body typography, link styling, and image responsiveness (max-width: 100%; height: auto).

[Output] Provide the base HTML template and CSS stylesheet setup.
```

---

### Step 2: Split-Screen Editorial Hero

```text
[Role] Act as a frontend designer.

[Context] I am building the Hero section for "Roast & Grain" cafe.

[Specs]
- Layout: 2-column asymmetric split layout using CSS Grid or Flexbox (equal height on desktop, stacking on mobile).
- Left column (Content):
  * Small uppercase subtitle: "Handcrafted Coffee & Slow Living".
  * Editorial Serif H1: "Coffee roasted with patience, brewed with intention."
  * Short intro paragraph describing the direct-trade beans.
  * Action row: "Explore Our Menu" button (terracotta fill) and "Find Our Cafe" link with an underline transition.
- Right column (Visual):
  * Featured photograph of coffee brewing or a latte art pour (Unsplash food/drink placeholder).
  * Border-radius: asymmetrical organic rounded corners (e.g., border-radius: 40px 12px 40px 12px).

[Output] Provide the HTML and CSS for this section.
```

---

### Step 3: Highlights & Signature Offerings

```text
[Role] Act as a frontend developer.

[Context] I am building the "Signature Offerings" menu showcase for Roast & Grain.

[Specs]
- Section title in serif font with a small centered divider line beneath it.
- 3-item showcase grid representing signature products:
  * 1: "Single-Origin Pour Over"
  * 2: "Oat Milk Cardamom Latte"
  * 3: "Sourdough Pastries & Bakes"
- For each item:
  * Circular or rounded image thumbnail at the top.
  * Item title in Playfair Display, tasting notes description, and price tag styled with the terracotta accent color.
- Responsive handling: Wrap cleanly on tablet/mobile screens.

[Output] Provide the HTML markup and CSS rules.
```

---

### Step 4: Story & Location Details

```text
[Role] Act as a UI frontend developer.

[Context] I need the "About Our Space & Visit Us" section for the cafe website.

[Specs]
- 2-column layout (Stacking on mobile):
  * Column 1 (Our Story): Warm narrative about sourcing sustainable beans directly from farmers, signed off with an italic note.
  * Column 2 (Visit Us Card): Styled info box containing cafe hours (Monday–Sunday schedule), physical address, and a "Get Directions" anchor link formatted as an outline button.
- Apply subtle 1px sand-colored borders and soft ivory background to the info card.

[Output] Provide the HTML structure and CSS styling.
```

---

### Step 5: Visual Photo Strip & Warm Footer

```text
[Role] Act as a frontend designer.

[Context] I need to conclude the Roast & Grain cafe website with an image gallery strip and warm footer.

[Specs]
- Gallery row: 4 square aspect-ratio photos in a row showing coffee beans, cozy cafe interior, and brewing gear (Unsplash coffee placeholders).
- Footer section:
  * Centered brand name in Playfair Display.
  * Quick links: Menu, Story, Contact, Instagram, Press.
  * Opening hours reminder and simple copyright statement.
  * Background matching the espresso dark brown tone (#231b15) with soft cream text (#fcfaf7) for high-contrast closure.

[Output] Provide the HTML and CSS code.
```