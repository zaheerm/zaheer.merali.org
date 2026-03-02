# Website Brand Guidelines — zaheer.merali.org

> The engineer who scaled Webex through a pandemic, now architecting enterprise AI — and still ships code from his phone on the bus.

These guidelines translate Zaheer's personal brand strategy into concrete visual and design rules for a modern single-page portfolio site. Every decision here serves the **Bold & Expressive** aesthetic: confident, high-contrast, technically sharp, with the kinetic energy of someone who ships at scale and cycles across continents.

---

## 1. Color Palette

Moving away from the dated red/yellow (#E04343/#FFE800) to a sophisticated palette that conveys enterprise AI authority with endurance energy.

### Core Colors

| Role | Color | Hex | Usage |
|------|-------|-----|-------|
| **Primary** | Deep Navy | `#0A1628` | Hero backgrounds, primary text, nav bar |
| **Secondary** | Electric Indigo | `#4F46E5` | Section accents, links, key highlights |
| **Accent** | Volt Green | `#22D3EE` | CTAs, hover states, the "spark" of energy |
| **Warm Accent** | Ember Orange | `#F97316` | Endurance/sport content, secondary CTAs |

### Neutrals

| Role | Hex | Usage |
|------|-----|-------|
| **White** | `#FFFFFF` | Light backgrounds, card surfaces |
| **Off-White** | `#F8FAFC` | Alternating section backgrounds |
| **Light Grey** | `#E2E8F0` | Borders, dividers, subtle UI |
| **Mid Grey** | `#94A3B8` | Secondary text, captions |
| **Dark Grey** | `#334155` | Body text on light backgrounds |
| **Near-Black** | `#0F172A` | Primary text, headings on light backgrounds |

### Surfaces

| Surface | Background | Text |
|---------|-----------|------|
| **Dark (hero, nav)** | `#0A1628` | `#F8FAFC` |
| **Light (content)** | `#FFFFFF` | `#0F172A` |
| **Alternate** | `#F8FAFC` | `#0F172A` |
| **Accent card** | `#4F46E5` | `#FFFFFF` |

### Interactive States

| State | Color | Notes |
|-------|-------|-------|
| **Link default** | `#4F46E5` | Electric Indigo |
| **Link hover** | `#22D3EE` | Volt Green — visible shift |
| **Focus ring** | `#22D3EE` at 50% opacity | 3px offset outline for accessibility |
| **Active/pressed** | `#3730A3` | Darker indigo |
| **Selection highlight** | `#4F46E5` at 15% opacity | Text selection background |

### Usage Rules

- Dark backgrounds (navy) are reserved for the hero and optionally the contact/footer section — never more than 2 dark sections.
- Electric Indigo is the workhorse accent; use Volt Green sparingly for moments that need to pop (CTAs, one key stat, hover feedback).
- Ember Orange appears only in endurance/sport context or as a secondary CTA — it should feel like a surprise, not a theme.
- Maintain a minimum contrast ratio of 4.5:1 for body text and 3:1 for large text (WCAG AA).

---

## 2. Typography

### Typeface Selection

| Role | Font | Source | Fallback |
|------|------|--------|----------|
| **Headings** | **Inter** | Google Fonts | system-ui, -apple-system, sans-serif |
| **Body** | **Inter** | Google Fonts | system-ui, -apple-system, sans-serif |
| **Code/Technical** | **JetBrains Mono** | Google Fonts | ui-monospace, "Cascadia Code", monospace |

Inter is used for both headings and body — differentiation comes from weight and size rather than font-family mixing. It's technically sharp, highly legible, and designed for screens. Load weights: 400, 500, 600, 700, 800.

### Type Scale

Base size: `18px` (1rem) on desktop, `16px` on mobile.

| Level | Size (rem) | Size (px) | Weight | Line Height | Letter Spacing | Usage |
|-------|-----------|-----------|--------|-------------|----------------|-------|
| **Display** | 4.5rem | 72px | 800 | 1.0 | -0.03em | Hero name only |
| **H1** | 3rem | 48px | 700 | 1.15 | -0.02em | Section headings |
| **H2** | 2rem | 32px | 700 | 1.25 | -0.01em | Sub-section headings |
| **H3** | 1.5rem | 24px | 600 | 1.3 | 0 | Card titles, feature labels |
| **Body Large** | 1.25rem | 20px | 400 | 1.6 | 0 | Intro paragraphs, lead text |
| **Body** | 1rem | 18px | 400 | 1.7 | 0 | Standard paragraphs |
| **Small** | 0.875rem | 14px | 500 | 1.5 | 0.01em | Captions, metadata |
| **Code** | 0.9rem | ~16px | 400 | 1.5 | 0 | Inline code, technical detail |

### Typography Rules

- **Headings** use tight negative letter-spacing for the bold, confident feel. Display and H1 sizes can go uppercase sparingly — never for body text.
- **Body text** line-height is generous (1.7) for readability. Max line length: 65-75 characters (`max-width: 42rem` on text blocks).
- **Bold text** within body uses weight 600 (semi-bold), not 700, to avoid heaviness.
- **Technical/code references** in body text use JetBrains Mono at 0.9em with a subtle background (`#F1F5F9`, 4px padding, 4px border-radius).
- No text shadows, no text stroke effects, no decorative fonts.

---

## 3. Layout & Spacing

### Grid System

- **Max content width:** `1200px` (75rem)
- **Content column:** centered with `auto` margins
- **CSS Grid** for section layouts; **Flexbox** for component-level alignment
- No Bootstrap — use CSS custom properties and native grid/flex
- **Columns:** Use a fluid 12-column grid when needed, but most sections are single-column or simple 2–3 column layouts

### Spacing Scale

Use a consistent 4px-based scale via CSS custom properties:

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | 4px | Tight internal spacing |
| `--space-2` | 8px | Icon gaps, compact padding |
| `--space-3` | 12px | Small component padding |
| `--space-4` | 16px | Standard component padding |
| `--space-6` | 24px | Card padding, form gaps |
| `--space-8` | 32px | Section inner padding |
| `--space-12` | 48px | Between content blocks |
| `--space-16` | 64px | Between major elements within a section |
| `--space-24` | 96px | Section padding (top/bottom) |
| `--space-32` | 128px | Hero section vertical padding |

### Section Rhythm

Each section of the single-page layout follows this vertical pattern:

```
[Section top padding: 96px]
  [Section heading]
  [Gap: 48px]
  [Section content]
[Section bottom padding: 96px]
```

The hero section gets larger padding (128px top, 96px bottom). Alternating sections use alternating backgrounds (white / off-white) to create visual separation without heavy dividers.

### Responsive Breakpoints

| Name | Width | Behaviour |
|------|-------|-----------|
| **Mobile** | < 640px | Single column, reduced type scale, stacked cards |
| **Tablet** | 640px – 1024px | 2-column grids where applicable |
| **Desktop** | > 1024px | Full layout, max-width container |

- The site is designed mobile-first. Base styles target mobile; `min-width` media queries add complexity.
- No horizontal scrolling at any breakpoint.
- Touch targets minimum 44x44px on mobile.

### Visual Hierarchy Rules

- Only one Display-size element on the page (the hero name).
- Each section has exactly one H1. Sub-content within a section uses H2 or H3.
- Whitespace is the primary hierarchy tool — not colour or size alone.

---

## 4. Visual Elements

### Photography & Imagery

- **Style:** High-contrast, candid, editorial. Conference talks, cycling action shots, real working environments — never stock-photo-generic.
- **Treatment:** Images can have a subtle dark overlay (`#0A1628` at 30–50% opacity) when used as backgrounds, ensuring text readability.
- **Aspect ratios:** Hero background images use 16:9 or wider. Profile/headshot images use 1:1 or 3:4.
- **No** clip-art, no cartoons, no AI-generated portraits.

### Icons

- Use a single, consistent icon set: **Phosphor Icons** (or Lucide) — clean, geometric, with both outline and filled variants.
- Icon size: 24px standard, 20px compact, 32px feature-sized.
- Icon color inherits from text color or uses the secondary accent.
- No Font Awesome (moving away from the current site's dependency).

### Decorative Elements

- **Gradient accent line:** A 4px horizontal gradient bar (`#4F46E5` → `#22D3EE`) used as a section header underline or card top-border. This is the primary decorative motif.
- **Subtle grid/dot pattern:** An optional very faint (`3–5%` opacity) dot grid on dark backgrounds for texture, evoking technical precision.
- **No** heavy borders, no drop shadows on sections, no rounded-everything. Borders are 1px and used sparingly.
- **Border radius:** 8px for cards and interactive elements. 4px for small components (tags, code blocks). 9999px (full-round) for buttons only if pill-shaped.

### Motion & Animation

- **Principle:** Motion is purposeful and fast. It confirms interaction, it doesn't entertain.
- **Duration:** 150ms for micro-interactions (hover, focus), 300ms for transitions (section reveals, page scroll).
- **Easing:** `cubic-bezier(0.4, 0, 0.2, 1)` for standard transitions. No bouncing, no elastic effects.
- **Scroll animations:** Sections fade in + slide up slightly (16px translateY) on scroll-enter. Use `IntersectionObserver`, not heavy animation libraries.
- **Hover effects:** Links get colour shift. Cards get a subtle `translateY(-2px)` lift. No zoom, no rotation, no shake.
- **Reduced motion:** Respect `prefers-reduced-motion`. When active, disable all transforms/animations; transitions remain for colour changes only.
- **No preloader.** The site should load fast enough not to need one.

### Expressing "Bold & Expressive"

The boldness comes from:
- **Oversized hero typography** (72px+ display text with tight tracking)
- **High-contrast colour pairings** (white text on deep navy; electric indigo accents on clean white)
- **Confident whitespace** — sections breathe, nothing is cramped
- **One bold accent per section** — a gradient line, a coloured stat, a vivid CTA — not everything screaming at once
- **Directness in copy** — short sentences, active voice, no filler

---

## 5. Site Structure

### Navigation

- **Fixed minimal top bar** on scroll: logo/name on left, section links on right, all text — no hamburger menu on desktop.
- **Mobile:** Hamburger menu that opens a full-screen overlay with large tap targets.
- **Nav links:** Home, About, Experience, Contact — matching the section anchors.
- **Active state:** Current section link gets the accent underline (gradient bar).
- **Scroll behaviour:** Smooth scroll to anchors. Nav bar gets a subtle background blur/darken after scrolling past the hero.

### Hero Section

- **Full viewport height** (`100vh` or close to it).
- **Dark background** (`#0A1628`) — optionally with a subtle ambient image or gradient mesh.
- **Display-sized name:** "Zaheer Merali" in 72px+ bold Inter, white.
- **Tagline below name:** The one-line brand summary or a condensed version. Body Large size, lighter weight, `#94A3B8` colour.
- **Rotating roles** (optional, simple): "Engineering Leader / AI Architect / Endurance Athlete" — CSS-only or minimal JS, not jQuery text rotator.
- **Single CTA or scroll indicator** at the bottom — subtle down-arrow or "Scroll" text.
- **No** background slideshow, no parallax, no video autoplay.

### About Section

- **Light background** (`#FFFFFF`).
- **Two-column layout on desktop:** Left column has a professional headshot (1:1, clean, high quality). Right column has 2–3 short paragraphs.
- **Content focus:** Updated positioning — not "a little about me" but a confident, specific statement about what Zaheer does and why it matters. Draw from the brand positioning statement.
- **Optional:** 3–4 key stats in a horizontal row below the text (e.g., "15+ Years at Cisco", "25 Years Open Source", "550km Cycling"). Stats use H2 size numbers with the Electric Indigo accent.
- **Single column on mobile**, image stacked above text.

### Experience / Highlights Section

- **Alternating background** (`#F8FAFC`).
- **Card-based layout:** 3–4 cards in a responsive grid (3 columns desktop, 1 column mobile).
- **Each card** represents a content pillar from the brand strategy:
  - Enterprise AI in Production
  - Engineering at Scale
  - AI-Augmented Developer
  - Endurance & Community
- **Card structure:** Icon (Phosphor, 32px), H3 title, 2-line description, optional link.
- **Cards have** the 4px gradient top-border as their accent.
- **No** timeline layout, no long-form resume. This is highlights, not a CV.

### Contact Section

- **Dark background** (`#0A1628`) to bookend the page with the hero.
- **Simple and direct:** H1 heading ("Let's Connect" or similar), then 3 contact methods in a row:
  - LinkedIn (primary — this is where Zaheer's brand lives)
  - GitHub
  - Email
- **Each contact method:** Icon + label + link. Clean, no boxes, no heavy styling.
- **Optional:** A single-line call to action above the links ("Building something at scale? Let's talk.").
- **No contact form.** Direct links only — less friction, less maintenance.

### Footer

- Minimal. Small text with copyright and "Built with [tech]" if desired.
- Same dark background as contact section — they can be visually continuous.

---

## 6. Voice & Copy

### Tone Rules (from Brand Strategy)

- **Direct and experience-backed.** Lead with what's been built, not opinions. "I shipped this" > "I think this."
- **Technically confident but accessible.** Complex systems explained clearly.
- **Conversational, not corporate.** No "thrilled to announce" or "passionate about". Write like talking to a sharp colleague.
- **Show the human.** The hospital-to-half-marathon story. The bus-stop coding. Real moments.
- **First person.** "I" statements with concrete details.

### Headline Writing Style

- Short, punchy, active voice.
- Lead with the action or the outcome, not the category.
- Good: "Scaling Webex Through a Pandemic" / "25 Years of Open Source"
- Bad: "My Professional Experience" / "About My Work"
- Use sentence case for headings, not Title Case (except the hero name).

### CTA Language

- Direct and low-friction: "View on LinkedIn", "See on GitHub", "Get in touch"
- No "Learn More", "Click Here", "Submit"
- CTAs should tell the visitor exactly what happens when they click.

### Copy Length

- Hero tagline: 1 sentence, max 15 words.
- About section: 2–3 short paragraphs, max 150 words total.
- Card descriptions: 1–2 sentences, max 30 words each.
- Everything earns its place. If a sentence doesn't add information, cut it.

---

## 7. Technical Constraints

### Static Site Requirements

- **No build tools required.** The site ships as plain HTML, CSS, and minimal JS. No webpack, no bundlers, no frameworks.
- **Single `index.html`** file for the entire single-page site.
- **Single CSS file** using modern CSS (custom properties, grid, flexbox, `clamp()`, `min()`, container queries if useful).
- **No Bootstrap.** No CSS framework dependency. All styles are custom and purpose-built.
- Hosted on GitHub Pages (or similar static hosting).

### CSS Architecture

- Use CSS custom properties (`--var`) for all colours, spacing, and typography values defined in these guidelines.
- Organize CSS in logical sections matching site structure: reset, custom properties, typography, layout, components, sections, utilities, responsive.
- Use modern CSS features: `clamp()` for fluid typography, `gap` for grid/flex spacing, `aspect-ratio` for images, `scroll-behavior: smooth`.
- No vendor prefixes unless required for a feature with <95% support. Autoprefixer not available — target modern evergreen browsers.

### Performance

- **Target:** Largest Contentful Paint < 2.5s, Cumulative Layout Shift < 0.1.
- **Fonts:** Load Inter (400, 600, 700, 800) and JetBrains Mono (400) via Google Fonts with `display=swap`. Subset to Latin if possible.
- **Images:** Use modern formats (WebP with JPEG fallback), lazy-load below-the-fold images, explicit `width`/`height` attributes to prevent layout shift.
- **JavaScript:** Minimal. Only for: smooth scroll polyfill (if needed), intersection observer for scroll animations, mobile nav toggle. No jQuery. Target < 5KB total JS.
- **No** preloader GIF, no Google Maps embed, no heavy icon font (use inline SVG icons or a small subset).

### Accessibility

- Semantic HTML5 elements (`header`, `main`, `section`, `nav`, `footer`).
- All images have descriptive `alt` text.
- Focus states are visible and use the defined focus ring style (`#22D3EE` at 50%, 3px offset).
- Skip-to-content link as the first focusable element.
- Colour contrast meets WCAG AA (4.5:1 body, 3:1 large text) — verified for all colour pairings in this guide.
- `prefers-reduced-motion` respected for all animations.
- `prefers-color-scheme` — not required for v1, but the palette is structured to support a future light/dark toggle.
- Landmark roles via semantic elements; `aria-label` on nav and sections where helpful.
- Interactive elements are keyboard-navigable in logical order.

---

## Appendix: CSS Custom Properties Starter

```css
:root {
  /* Colors */
  --color-primary: #0A1628;
  --color-secondary: #4F46E5;
  --color-accent: #22D3EE;
  --color-warm: #F97316;

  --color-white: #FFFFFF;
  --color-off-white: #F8FAFC;
  --color-light-grey: #E2E8F0;
  --color-mid-grey: #94A3B8;
  --color-dark-grey: #334155;
  --color-near-black: #0F172A;

  /* Typography */
  --font-body: 'Inter', system-ui, -apple-system, sans-serif;
  --font-mono: 'JetBrains Mono', ui-monospace, 'Cascadia Code', monospace;

  --text-display: clamp(3rem, 8vw, 4.5rem);
  --text-h1: clamp(2rem, 5vw, 3rem);
  --text-h2: clamp(1.5rem, 3vw, 2rem);
  --text-h3: 1.5rem;
  --text-body-lg: 1.25rem;
  --text-body: 1rem;
  --text-small: 0.875rem;

  /* Spacing */
  --space-1: 0.25rem;
  --space-2: 0.5rem;
  --space-3: 0.75rem;
  --space-4: 1rem;
  --space-6: 1.5rem;
  --space-8: 2rem;
  --space-12: 3rem;
  --space-16: 4rem;
  --space-24: 6rem;
  --space-32: 8rem;

  /* Layout */
  --max-width: 75rem;
  --content-width: 42rem;

  /* Motion */
  --ease-standard: cubic-bezier(0.4, 0, 0.2, 1);
  --duration-fast: 150ms;
  --duration-normal: 300ms;

  /* Borders */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-full: 9999px;
}
```

---

*These guidelines are the single source of truth for all visual and structural decisions on zaheer.merali.org. When in doubt, refer back to the brand positioning: confident, direct, technically sharp, with bold energy.*
