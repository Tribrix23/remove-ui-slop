# Premium SaaS Landing Page Design Skill

## Skill Metadata

```yaml
name: premium-saas-landing-page
description: >
  Design and implement premium, modern SaaS landing pages with a dark,
  technical, enterprise-grade visual language inspired by high-quality
  developer tools and modern software companies.
version: 1.0.0
```

---

# 1. Purpose

Use this skill when asked to design, create, improve, or implement:

- SaaS landing pages
- AI product websites
- Developer tool websites
- Enterprise software websites
- Cybersecurity product pages
- Infrastructure platforms
- Startup homepages
- Product marketing pages
- Technology company websites

The goal is to produce websites that feel intentionally art-directed and professionally designed.

The output MUST NOT look like a generic AI-generated landing page.

---

# 2. Visual Reference Profile

Target visual characteristics:

- Dark premium interface
- Enterprise technology aesthetic
- Editorial typography
- Large whitespace
- Thin low-contrast borders
- Grid-based composition
- Large bold headlines
- Small technical labels
- Monospace metadata
- Product UI integrated into the composition
- Subtle animation
- Restrained accent colors
- High information density in product previews
- Minimal decorative elements

The overall impression should be:

> A sophisticated software company with a mature design team.

---

# 3. Design Philosophy

Follow these principles.

## 3.1 Restraint

Do not decorate every empty area.

Whitespace is intentional.

Avoid:

- Random floating blobs
- Excessive gradients
- Too many cards
- Excessive shadows
- Multiple accent colors
- Giant rounded pills
- Emoji icons
- Generic stock illustrations

## 3.2 Hierarchy

Every section must immediately communicate:

1. What the user should look at first.
2. What information is secondary.
3. What action the user should take.

Use typography, spacing, contrast, and position instead of excessive visual effects.

## 3.3 Product First

Whenever possible, show the actual product experience.

Prefer:

```text
Headline
↓
Product interface visualization
```

Instead of:

```text
Headline
↓
Generic illustration
↓
Feature cards
```

---

# 4. Color System

## Base Colors

Use very dark neutral colors.

```css
:root {
  --background: #0d0d0f;
  --background-secondary: #121214;
  --background-tertiary: #17171b;
  --surface: #1b1b20;

  --text-primary: #f5f5f7;
  --text-secondary: #a1a1aa;
  --text-muted: #71717a;

  --border: rgba(255, 255, 255, 0.08);
  --border-subtle: rgba(255, 255, 255, 0.05);
  --border-hover: rgba(255, 255, 255, 0.15);
}
```

Avoid pure black unless specifically requested.

## Accent Color

Select ONE dominant accent color.

Examples:

```css
--accent-orange: #ff5c1a;
--accent-green: #5eead4;
--accent-blue: #60a5fa;
--accent-purple: #a78bfa;
```

Accent colors should primarily be used for:

- Eyebrow labels
- Small status indicators
- Active tabs
- Links
- Important badges
- Small visual details

Do not make every button, icon, border, and heading colorful.

---

# 5. Typography

## Preferred Fonts

Primary UI font:

- Inter
- Geist
- SF Pro Display
- Manrope

Technical font:

- Geist Mono
- JetBrains Mono
- IBM Plex Mono

## Hero Typography

Hero headlines must feel editorial and confident.

Recommended style:

```css
.hero-title {
  font-size: clamp(3.5rem, 6vw, 7rem);
  line-height: 0.95;
  letter-spacing: -0.055em;
  font-weight: 600;
  max-width: 900px;
}
```

Rules:

- Keep headlines short.
- Prefer 4–12 words.
- Use sentence case.
- Avoid marketing clichés.
- Allow intentional line breaks.
- Use negative letter spacing for large headings.

Good:

```text
The future isn't writing code.
It's reviewing it.
```

Bad:

```text
Revolutionize Your Workflow With The World's Most Powerful AI Platform
```

## Supporting Text

```css
.hero-description {
  font-size: 18px;
  line-height: 1.5;
  color: var(--text-secondary);
  max-width: 420px;
}
```

Keep supporting copy concise.

---

# 6. Layout System

Use a centered content container.

```css
.container {
  width: min(100% - 48px, 1440px);
  margin-inline: auto;
}
```

Desktop maximum widths:

```text
1200px
1280px
1440px
```

Do not make everything full width.

---

# 7. Navigation

Use a clean horizontal navigation.

Structure:

```text
[Logo]

Enterprise
Security
Customers
Pricing
Blog
Resources

[Log in]
[Primary CTA]
```

Recommended implementation:

```css
.navbar {
  height: 72px;

  display: flex;
  align-items: center;
  justify-content: space-between;

  border-bottom: 1px solid var(--border);
}
```

Navigation links:

```css
.nav-link {
  font-size: 14px;
  font-weight: 500;
  color: var(--text-secondary);
}

.nav-link:hover {
  color: var(--text-primary);
}
```

Requirements:

- Logo left
- Navigation centered or near center
- Actions right
- No oversized buttons
- No unnecessary icons

---

# 8. Announcement Bar

An optional announcement bar may appear above the navigation.

Example:

```text
We raised $143M to build the control layer for software change.
Read more →
```

Style:

```css
.announcement {
  height: 40px;

  display: flex;
  justify-content: center;
  align-items: center;

  border-bottom: 1px solid var(--border);

  font-size: 13px;
  color: var(--text-secondary);
}
```

The announcement must remain visually subtle.

---

# 9. Hero Section

Use an asymmetric two-column composition.

Example:

```text
┌──────────────────────────────────────────────────────┐
│                                                      │
│  EYEBROW                                             │
│                                                      │
│  Large headline              Supporting statement    │
│  spanning multiple lines.    CTA                     │
│                                                      │
└──────────────────────────────────────────────────────┘
```

Implementation:

```css
.hero {
  display: grid;
  grid-template-columns: 1.4fr 0.8fr;

  gap: clamp(48px, 8vw, 140px);

  align-items: center;

  padding-top: 120px;
  padding-bottom: 100px;
}
```

On mobile:

```css
@media (max-width: 768px) {
  .hero {
    grid-template-columns: 1fr;
    padding-top: 72px;
  }
}
```

---

# 10. Eyebrow Labels

Use small technical labels above major headings.

Example:

```text
AGENTIC CHANGE MANAGEMENT
```

Style:

```css
.eyebrow {
  font-family: "JetBrains Mono", monospace;

  font-size: 11px;
  font-weight: 600;

  letter-spacing: 0.06em;

  text-transform: uppercase;

  color: var(--accent);
}
```

These labels should feel like system metadata.

---

# 11. Buttons

Buttons should have restrained corner radii.

Preferred:

```css
border-radius: 4px;
border-radius: 6px;
```

Avoid:

```css
border-radius: 9999px;
```

unless the design explicitly requires pill badges.

## Primary Button

```css
.button-primary {
  display: inline-flex;
  align-items: center;
  gap: 8px;

  padding: 12px 18px;

  background: #f5f5f5;
  color: #111;

  border-radius: 5px;

  font-size: 14px;
  font-weight: 500;

  transition:
    transform 180ms ease,
    background 180ms ease;
}

.button-primary:hover {
  background: #ffffff;
  transform: translateY(-1px);
}
```

## Secondary Button

```css
.button-secondary {
  background: transparent;

  border: 1px solid var(--border);

  color: var(--text-primary);

  padding: 12px 18px;

  border-radius: 5px;
}
```

---

# 12. Product Visualization

This is one of the most important parts of the design.

Do not simply create a fake browser screenshot.

Create layered, realistic software interfaces.

Possible interface types:

- Code review dashboard
- Analytics dashboard
- Security console
- AI agent interface
- IDE interface
- Project management board
- Infrastructure monitor
- Pull request viewer

The product visualization should feel:

- Dense
- Functional
- Technical
- Realistic
- Multi-layered

---

# 13. Layered Product Interface

Use multiple overlapping interface panels.

Example architecture:

```text
BACKGROUND
    ↓
Large dashboard

MIDDLE
    ↓
Secondary application panel

FOREGROUND
    ↓
Primary feature demonstration

DETAIL LAYER
    ↓
Badges, indicators, tooltips, metadata
```

Use absolute positioning carefully.

Example:

```css
.product-stage {
  position: relative;
  min-height: 700px;

  overflow: hidden;

  border-top: 1px solid var(--border);
}
```

Panel:

```css
.product-panel {
  position: absolute;

  background: #141418;

  border: 1px solid var(--border);

  border-radius: 6px;

  overflow: hidden;
}
```

---

# 14. Fake Product UI Rules

Product interfaces should contain believable information.

Include:

- Tabs
- Status indicators
- Priority labels
- Metadata
- Avatars
- Timestamps
- Search fields
- Tables
- Sidebars
- Code snippets
- Progress indicators
- Notification badges

Example:

```text
01 Review
02 Prioritize
03 Understand
04 Secure
```

Example dashboard data:

```text
P0   Critical
P1   High priority
P2   Needs review
P3   Scheduled
```

Do not use lorem ipsum inside product interfaces.

Use believable software terminology.

---

# 15. Borders and Dividers

Borders are a major part of this visual style.

Use subtle borders to structure information.

```css
border: 1px solid rgba(255,255,255,0.08);
```

Section dividers:

```css
border-top: 1px solid var(--border);
```

Grid lines can be visible but subtle.

Example:

```css
background-image:
  linear-gradient(
    rgba(255,255,255,0.03) 1px,
    transparent 1px
  );
```

Never make grid lines visually dominant.

---

# 16. Cards

Avoid the common AI-generated design pattern:

```text
Rounded card
Rounded card
Rounded card
Rounded card
```

Instead, use cards only when they represent:

- Product modules
- Data containers
- Features
- Statistics
- Interactive components

Card style:

```css
.card {
  background: rgba(255,255,255,0.02);

  border: 1px solid var(--border);

  border-radius: 6px;

  padding: 24px;
}
```

Avoid large drop shadows.

---

# 17. Spacing System

Use a consistent spacing scale.

```text
4px
8px
12px
16px
24px
32px
48px
64px
96px
128px
160px
```

Major sections should have generous vertical spacing.

Example:

```css
section {
  padding-block: 120px;
}
```

Do not compress premium landing pages.

Whitespace creates hierarchy.

---

# 18. Grid Layout

Use CSS Grid for structured sections.

Example:

```css
.feature-grid {
  display: grid;

  grid-template-columns:
    repeat(12, minmax(0, 1fr));

  gap: 24px;
}
```

Allow elements to span different column sizes.

Example:

```css
.feature-main {
  grid-column: span 7;
}

.feature-side {
  grid-column: span 5;
}
```

Avoid making every element equal width.

Asymmetry creates visual interest.

---

# 19. Interaction Design

Animations should be subtle.

Recommended:

```css
transition: 180ms ease;
transition: 240ms cubic-bezier(.2,.8,.2,1);
```

Good animations:

- Small opacity fade
- 2–8px translate
- Border color change
- Background change
- Slight scale change
- Interface panel movement

Avoid:

- Excessive bouncing
- Long animations
- Constant floating
- Heavy parallax
- Distracting particle effects

---

# 20. Scroll Animations

Use entrance animations sparingly.

Recommended:

```text
opacity: 0 → 1
translateY: 16px → 0
```

Duration:

```text
300ms–700ms
```

Stagger related elements slightly.

Do not animate every single component.

---

# 21. Responsive Rules

## Desktop

Prioritize:

- Large typography
- Asymmetric layouts
- Complex product visualizations
- Multi-column grids

## Tablet

Reduce:

- Heading size
- Large gaps
- Panel overlap complexity

## Mobile

Prioritize:

- Readability
- Vertical stacking
- Horizontal scroll only when necessary for product demos

Never simply shrink the desktop layout.

Redesign layout behavior for mobile.

---

# 22. Mobile Navigation

On mobile:

```text
[Logo]                  [Menu]
```

Use a slide-out or dropdown navigation.

Do not attempt to fit all navigation links into a narrow screen.

---

# 23. Accessibility

Always implement:

- Semantic HTML
- Visible focus states
- Keyboard navigation
- Sufficient contrast
- ARIA labels when needed
- Proper button elements
- Proper link elements

Example:

```css
button:focus-visible,
a:focus-visible {
  outline: 2px solid var(--accent);
  outline-offset: 4px;
}
```

---

# 24. Implementation Standards

When generating React or Next.js code:

Use:

```text
React
Next.js
TypeScript
Tailwind CSS
Framer Motion (only when useful)
Lucide React icons
```

Recommended component structure:

```text
components/
├── landing/
│   ├── AnnouncementBar.tsx
│   ├── Navbar.tsx
│   ├── Hero.tsx
│   ├── ProductDemo.tsx
│   ├── FeatureGrid.tsx
│   ├── Metrics.tsx
│   ├── Testimonials.tsx
│   ├── CTA.tsx
│   └── Footer.tsx
```

Do not create one massive component containing the entire page.

---

# 25. Tailwind Standards

Prefer design tokens.

Example:

```js
const colors = {
  background: "#0d0d0f",
  surface: "#17171b",
  border: "rgba(255,255,255,0.08)",
}
```

Reusable patterns:

```tsx
className="
  border
  border-white/[0.08]
  bg-white/[0.02]
"
```

Avoid arbitrary random values throughout the application.

Create consistency.

---

# 26. Icon Usage

Use simple line icons.

Preferred:

- Lucide
- Heroicons

Rules:

- 16–20px for UI
- 20–24px for feature icons
- Stroke width around 1.5–2

Do not use emoji as interface icons.

---

# 27. Content Rules

Write concise, confident copy.

Preferred style:

```text
Ship faster.
Know what's changing.
Stop reviewing blindly.
Infrastructure without surprises.
```

Avoid:

```text
Unlock the power of next-generation innovation.
Transform your business today.
Revolutionary solutions for modern teams.
```

Copy should sound like a technical product company.

---

# 28. Section Structure

Recommended landing page architecture:

```text
1. Announcement Bar
2. Navigation
3. Hero
4. Product Visualization
5. Customer / Trust Logos
6. Core Feature Section
7. Deep Product Demonstration
8. Metrics
9. Enterprise / Security Section
10. Testimonials
11. Final CTA
12. Footer
```

Not every landing page needs all sections.

Choose based on the product.

---

# 29. Screenshot-Inspired Hero Pattern

When implementing a hero similar to a premium software company:

```text
┌──────────────────────────────────────────────────────┐
│ Announcement Bar                                     │
├──────────────────────────────────────────────────────┤
│ Logo        Nav Navigation              Login CTA    │
├──────────────────────────────────────────────────────┤
│                                                      │
│ EYEBROW                                              │
│                                                      │
│ LARGE HEADLINE                Supporting copy        │
│ spanning 2–3 lines            CTA                    │
│                                                      │
│                                                      │
├──────────────────────────────────────────────────────┤
│ PRODUCT NAVIGATION TABS                              │
├───────────────┬──────────────┬──────────────┬────────┤
│ Product UI    │ Dashboard    │ Analysis     │ Health │
│               │              │              │        │
│     Layered realistic software interface             │
│                                                      │
└──────────────────────────────────────────────────────┘
```

---

# 30. Quality Checklist

Before completing the design, verify:

## Visual Quality

- [ ] Does it look professionally art-directed?
- [ ] Is the layout asymmetric where appropriate?
- [ ] Is whitespace intentionally used?
- [ ] Are borders subtle?
- [ ] Are accent colors restrained?
- [ ] Does the typography have strong hierarchy?

## Generic AI Detection

Remove anything that looks like:

- [ ] Purple gradient everywhere
- [ ] Huge rounded cards
- [ ] Excessive glassmorphism
- [ ] Random floating shapes
- [ ] Emoji icons
- [ ] Generic feature card grids
- [ ] Marketing buzzwords
- [ ] Excessive gradients
- [ ] Identical spacing everywhere

## Product Quality

- [ ] Does the product mockup look believable?
- [ ] Does it contain realistic UI structure?
- [ ] Are there multiple levels of information?
- [ ] Does the UI support the product story?

## Code Quality

- [ ] Components are modular.
- [ ] Mobile layout works.
- [ ] No unnecessary dependencies.
- [ ] Animations are performant.
- [ ] Semantic HTML is used.
- [ ] Accessibility is considered.

---

# 31. AI Execution Instructions

When the user requests a landing page:

1. First understand the product.
2. Identify the target audience.
3. Determine the primary conversion action.
4. Create a visual hierarchy.
5. Design the hero before designing lower sections.
6. Build the product visualization around the core product.
7. Use asymmetric layouts where appropriate.
8. Apply the dark premium design system.
9. Ensure responsive behavior.
10. Review the result for generic AI design patterns.

Do not immediately generate random components.

Think about:

```text
Product identity
        ↓
Visual language
        ↓
Layout hierarchy
        ↓
Hero composition
        ↓
Product visualization
        ↓
Supporting sections
        ↓
Responsive behavior
```

---

# 32. Final Design Standard

The final output should feel comparable to a website designed by:

- A senior product designer
- A brand designer
- A frontend engineer specializing in motion and UI
- A modern SaaS startup design team

The result should NOT feel like:

> "A template generated from a generic landing page prompt."

It should feel intentional, product-specific, technically sophisticated, and visually restrained.

---

# Mandatory Default Behavior

Unless the user explicitly requests otherwise:

- Use dark mode for this style.
- Use large editorial typography.
- Use thin borders instead of heavy shadows.
- Use one primary accent color.
- Use realistic product UI.
- Avoid generic card grids.
- Use generous whitespace.
- Prefer asymmetric composition.
- Keep copy concise.
- Keep animations subtle.
- Build responsive layouts.
- Prioritize product storytelling.

The AI should always ask itself:

> Would this look credible on the homepage of a well-funded modern software company?

If the answer is no, redesign it before finishing.
