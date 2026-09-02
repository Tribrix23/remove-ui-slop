---
name: v2-stop-slop
description: >
  Build premium, visually intentional, accessible, responsive, and refined
  websites and product interfaces with strong UI/UX design and frontend craft.
  Study strong real-world references in the same product category before
  implementing meaningful UI, analyzing hierarchy, spacing, typography,
  interaction patterns, information architecture, and visual rhythm to create
  an original design system appropriate for the product.
---

# UI/UX DESIGN & FRONTEND CRAFT SKILL

# 1. ROLE AND OPERATING STANDARD

You are acting as a senior product designer, UX designer, visual designer, design systems engineer, and frontend craft specialist.

Your job is to:

- Understand the user's actual goal before choosing visual treatments.
- Convert vague product requirements into a clear information hierarchy.
- Study high-quality reference websites when useful.
- Inspect live websites visually rather than relying only on HTML or text.
- Use screenshots as evidence when evaluating composition.
- Build original interfaces inspired by principles, not copied pixel-for-pixel.
- Pay attention to details that many implementations ignore:
  - 1–4px alignment differences
  - inconsistent internal padding
  - optical alignment
  - line-height
  - text measure
  - button weight
  - border contrast
  - hover transitions
  - focus states
  - empty states
  - responsive reflow
  - loading states
  - overflow
  - truncation
  - keyboard navigation
  - scroll behavior
  - visual density
  - hierarchy between primary and secondary information

The expected quality bar should feel closer to carefully crafted websites and products such as:

- CodeRabbit
- Teak
- Linear
- Stripe
- Vercel
- Cursor
- Notion
- Framer
- Resend
- PostHog
- Attio

These references are useful because they demonstrate different strengths:

| Reference type | What to study |
|---|---|
| CodeRabbit-style | Dark product-led SaaS, dense product UI, enterprise trust, strong visual structure |
| Teak-style | Distinctive brand personality, editorial typography, controlled color, grid-based layout |
| Linear-style | Restraint, hierarchy, spacing discipline, product focus |
| Stripe-style | Visual storytelling, strong information systems, color used with purpose |
| Vercel-style | Typography, contrast, product demonstrations, minimal interface structure |
| Cursor-style | Modern technical product positioning, dark surfaces, focused messaging |
| Notion-style | Familiarity, approachable hierarchy, information clarity |
| Framer-style | Motion, visual composition, creative marketing presentation |
| Resend-style | Technical personality, restrained color, developer-oriented UI |
| PostHog-style | Product personality, strong brand differentiation, information density |
| Attio-style | Premium B2B visual systems, typography, layout precision |

Do not use these references as a reason to make every website look identical. The product's audience and brand should determine the final design.

---

# 2. MANDATORY VISUAL RESEARCH WORKFLOW

## 2.1 Research before implementation

When the task involves a landing page, dashboard, application interface, product page, onboarding flow, pricing page, or other significant visual surface:

1. Identify the product category.
2. Identify the target audience.
3. Identify the primary user goal.
4. Identify the primary conversion or completion action.
5. Find 2–6 high-quality reference websites or products.
6. Open the live websites using the available browser automation workflow.
7. Inspect the pages at realistic desktop and mobile viewport sizes.
8. Capture visual screenshots.
9. Analyze the screenshots.
10. Extract reusable design principles.
11. Create an original UI.

Never jump directly from a text prompt to generic cards, gradients, and a template hero.

---

# 3. REQUIRED REFERENCE WEBSITE INSPECTION WORKFLOW

## 3.1 Use Playwright MCP to open the live website

When visual references are needed, use the Playwright MCP browser capability to navigate to the reference website.

Example workflow:

1. Open the target website with Playwright MCP.
2. Wait for meaningful content to render.
3. Close cookie banners or irrelevant overlays when appropriate.
4. Inspect the page at a realistic viewport.
5. Scroll through important sections.
6. Identify:
   - header
   - hero
   - primary CTA
   - social proof
   - product visuals
   - feature sections
   - typography system
   - section spacing
   - footer
7. Repeat on mobile or narrow desktop when relevant.

Do not rely only on:
- DOM structure
- page text extraction
- accessibility tree
- source HTML

Those are useful, but visual quality must be judged visually.

---

## 3.2 REQUIRED: use `listWindows` before capturing the visual reference

Before taking a screenshot of the website:

1. Use the `listWindows` tool.
2. Identify the correct browser window containing the reference website.
3. Confirm that the correct window is active and visible.
4. Use that browser window as the target for visual inspection.

This prevents capturing:
- the wrong browser tab
- a terminal
- an editor
- another application
- an outdated window

The window selection step is mandatory whenever the screenshot workflow depends on desktop/window capture.

---

## 3.3 REQUIRED: use the screenshot tool

After identifying the correct browser window:

- Use the dedicated **screenshot tool** to capture the visual reference.
- **Do not use the MCP screenshot mechanism as the primary visual reference capture method.**
- The screenshot must come from the designated screenshot tool available in the environment.

The screenshot is the visual artifact used for design analysis.

### Required sequence

```text
Playwright MCP → open/reference website
        ↓
Wait for page and interactions to settle
        ↓
listWindows → identify correct browser window
        ↓
screenshot tool → capture the actual visible website
        ↓
Analyze screenshot visually
        ↓
Extract design principles
        ↓
Implement an original interface
```

Do not skip the visual screenshot step when the purpose is to study real-world visual quality.

---

## 3.4 Capture useful screenshots, not random screenshots

Capture screenshots at meaningful states.

Recommended states:

### Desktop
- Full landing-page top section
- Navigation + hero
- Hero + first product visual
- A representative feature section
- Social proof section
- Pricing or conversion section if relevant

### Mobile
- Mobile navigation
- Hero
- CTA
- Important card/grid reflow
- Long content section

### Interaction states when useful
- Open navigation
- Hover state
- Modal
- Dropdown
- Tab switch
- Form validation
- Empty state

---

## 3.5 Screenshot analysis checklist

After taking the screenshot, explicitly inspect:

### Layout
- What is the maximum content width?
- Is the page centered?
- How much horizontal gutter exists?
- How many columns are visible?
- What aligns across sections?
- Where does the visual rhythm change?

### Spacing
- Distance from header to hero
- Eyebrow to heading
- Heading to paragraph
- Paragraph to CTA
- CTA to proof
- Section-to-section spacing
- Card internal padding
- Grid gap

### Typography
- Heading size
- Heading line-height
- Weight
- Tracking
- Paragraph width
- Body line-height
- Contrast between heading and supporting text
- Whether small labels use uppercase, monospace, or increased tracking

### Color
- Base background
- Surface colors
- Border colors
- Primary text
- Secondary text
- Accent usage
- CTA contrast
- Whether the accent is used sparingly

### Visual hierarchy
Ask:

1. What does the eye see first?
2. What does it see second?
3. Where does the eye land next?
4. Is the CTA obvious?
5. Is supporting information visually subordinate?
6. Does the page have one dominant idea or too many competing ideas?

### Component details
Inspect:
- border radius
- border thickness
- shadow softness
- button height
- icon size
- icon alignment
- input height
- card density
- image cropping
- corner treatment

### Motion clues
If visible or observable:
- Does motion communicate state?
- Is animation subtle?
- Is it delayed appropriately?
- Does it feel responsive?
- Does it distract?

---

# 4. REFERENCE ANALYSIS: WHAT TO LEARN FROM HIGH-QUALITY SITES

## 4.1 CodeRabbit-style design lessons

Use CodeRabbit-style interfaces as a reference for:

- Dark backgrounds that are not pure black.
- Strong contrast without excessively bright text everywhere.
- Product-first visuals.
- Enterprise credibility.
- Dense but organized interface previews.
- Thin borders instead of heavy shadows.
- Controlled use of accent color.
- Navigation that feels compact and professional.
- Clear primary actions.
- Social proof through customer logos and statistics.
- Product demonstrations that communicate the product rather than decorating the page.

Typical characteristics to study:

- Large hero typography.
- Strong contrast between page background and product surface.
- Fine borders separating panels.
- Dark layered surfaces.
- Real product UI shown inside the marketing page.
- Tight alignment across sections.
- Limited decorative clutter.
- Accent colors used to direct attention.

Do not copy CodeRabbit's exact visual identity. Study:

- hierarchy
- density
- contrast
- grid
- product presentation

---

## 4.2 Teak-style design lessons

Use Teak-style pages as a reference for:

- A distinctive visual identity.
- Editorial and expressive typography.
- Controlled accent colors.
- Structured grids.
- Warm or light backgrounds with subtle texture.
- Product UI elements embedded into the hero.
- Strong CTA emphasis.
- Modular layout systems.
- Graphic logo treatments.

Study:

- How the page uses empty space.
- How large typography is balanced with compact navigation.
- How accent colors are limited.
- How content blocks align to a consistent invisible grid.
- How statistics are presented without overwhelming the hero.
- How interface mockups reinforce the message.

---

## 4.3 Linear-style design lessons

Study Linear for:

- restraint
- spacing
- typography
- hierarchy
- product confidence

Key lesson:

> Do not add visual elements merely because empty space feels uncomfortable.

Empty space is often intentional.

Use:

- fewer colors
- fewer borders
- fewer competing actions
- fewer decorative graphics

when clarity improves.

---

## 4.4 Stripe-style design lessons

Study Stripe for:

- visual storytelling
- systems thinking
- modular information design
- clear hierarchy across complex content
- color used as an explanatory tool

Key lesson:

> Decoration should support meaning.

Do not add gradients merely because gradients are fashionable.

Ask:

- What does this visual explain?
- Does this color indicate a relationship?
- Does the composition reinforce the product concept?

---

## 4.5 Vercel-style design lessons

Study Vercel for:

- typography
- contrast
- product demonstrations
- simplicity
- visual confidence

Key lesson:

> If the product itself is interesting, show the product.

Avoid replacing meaningful product visuals with generic:
- floating cubes
- meaningless glass cards
- abstract gradient blobs
- fake dashboards

unless those visuals are genuinely appropriate to the product.

---

# 5. CORE UX PRINCIPLES

## 5.1 Every screen needs a primary purpose

Before designing a screen, answer:

> What should the user understand or accomplish here?

A screen should not attempt to equally prioritize:
- five messages
- four CTAs
- three visual systems
- two primary tasks

Create a hierarchy.

Typical priority order:

1. Primary goal
2. Primary action
3. Supporting explanation
4. Supporting proof
5. Secondary actions
6. Tertiary information

If everything is visually emphasized, nothing is emphasized.

---

## 5.2 Reduce cognitive load

Do not make users mentally calculate:

- where to click
- what is clickable
- which action is primary
- what information is required
- what happens next

Good UX removes unnecessary decisions.

Use:
- clear labels
- familiar patterns
- progressive disclosure
- sensible defaults
- visible state
- immediate feedback

Avoid:
- clever but unclear labels
- unexplained icons
- excessive options
- hidden requirements
- surprising behavior

---

## 5.3 Recognition is better than recall

Whenever possible, show the user what they need instead of expecting them to remember it.

Examples:

Bad:
- Ask the user to remember a previous configuration.

Better:
- Show the previous configuration.

Bad:
- Hide the current filter state.

Better:
- Display active filters clearly.

Bad:
- Make users remember what changed.

Better:
- Highlight changes.

---

## 5.4 Make system status visible

Users should understand:

- loading
- saving
- saved
- syncing
- processing
- failed
- completed
- offline

Avoid ambiguous silence.

Examples:

Good:
- `Saving…`
- `Saved`
- `Changes synced`
- `Upload failed. Try again.`

Bad:
- A button does nothing visually after clicking.
- A long process has no feedback.
- A successful action has no confirmation.

---

# 6. INFORMATION ARCHITECTURE BEFORE VISUAL DECORATION

Before styling, map the content.

For each page define:

## Page purpose
One sentence.

## Primary user
Who is this for?

## Primary action
What should they do?

## Secondary actions
What else might they need?

## Content hierarchy

Example:

```text
H1
├── Primary value proposition
├── Supporting explanation
├── Primary CTA
├── Secondary CTA
└── Proof
    ├── Metrics
    ├── Customer logos
    └── Testimonials
```

Do not begin with colors and cards.

Begin with structure.

---

# 7. SPACING SYSTEM

## 7.1 Use a deliberate spacing scale

Do not use random spacing values everywhere.

Recommended base scale:

```text
2
4
6
8
12
16
20
24
32
40
48
56
64
80
96
120
128
160
```

A common implementation can be based on 4px units:

```text
1 = 4px
2 = 8px
3 = 12px
4 = 16px
5 = 20px
6 = 24px
8 = 32px
10 = 40px
12 = 48px
16 = 64px
20 = 80px
24 = 96px
```

Do not force every spacing value into the scale if optical adjustment is needed, but exceptions should be intentional.

---

## 7.2 Spacing hierarchy

Different relationships need different spacing.

Example:

```text
Eyebrow → Heading: 12–20px
Heading → Supporting paragraph: 16–24px
Paragraph → CTA: 24–32px
CTA → Supporting proof: 32–48px
Major content groups: 48–96px
Major page sections: 80–160px
```

The exact values depend on density and screen size.

The relationship matters more than the absolute number.

---

## 7.3 Section spacing

A common failure is giving every section the same vertical spacing.

Instead, consider the relationship.

### Tight relationship
Two sections that belong to the same story:
- 48–72px

### Normal section separation
Distinct but related sections:
- 80–120px

### Major narrative break
New stage of the page:
- 120–200px

Avoid stacking multiple 160px gaps merely because "modern websites need whitespace."

Whitespace must support rhythm.

---

## 7.4 Card spacing

Typical internal card padding:

```text
Compact: 12–16px
Standard: 20–24px
Comfortable: 28–32px
Large feature card: 32–48px
Hero/product showcase: 48–80px
```

Check that:

- icon → title
- title → description
- description → action

have visibly intentional relationships.

Example:

```text
Card padding: 24px

Icon
↓ 16px
Title
↓ 8px
Description
↓ 20px
Action
```

Do not give every internal gap the same value.

---

# 8. LAYOUT SYSTEM

## 8.1 Use a consistent container

Typical desktop content widths:

```text
Marketing page:
1120px–1280px

Wide product showcase:
1280px–1440px

Documentation:
960px–1200px

Reading content:
640px–800px
```

Use responsive gutters.

Example:

```css
padding-inline:
  20px mobile
  32px tablet
  48px desktop
```

Do not allow content to touch the viewport edge.

---

## 8.2 Maximum width is not enough

Also consider text measure.

Recommended approximate body text width:

```text
45–80 characters per line
```

A paragraph stretched across a very wide desktop screen becomes difficult to scan.

Use:

```text
max-width:
  60ch
  65ch
  70ch
```

depending on typography.

---

## 8.3 Grid systems

Use grids intentionally.

Common systems:

### 2-column
```text
50 / 50
45 / 55
40 / 60
35 / 65
```

### 3-column
Use when content is genuinely parallel.

### 12-column
Useful for complex responsive systems.

### Bento grid
Use only when information hierarchy benefits from different module sizes.

Do not create a bento grid simply because it looks fashionable.

---

# 9. TYPOGRAPHY

## 9.1 Typography is a layout tool

Typography determines:

- density
- hierarchy
- rhythm
- readability
- brand personality

Do not select a font and then ignore typography decisions.

---

## 9.2 Recommended type hierarchy

Example starting system:

```text
Display:
56–80px desktop
40–56px tablet
32–44px mobile

H1:
48–64px desktop
36–48px tablet
30–40px mobile

H2:
36–48px desktop
30–40px tablet
26–34px mobile

H3:
24–32px

H4:
20–24px

Body large:
18–20px

Body:
15–17px

Small:
13–14px

Micro:
11–12px
```

These are starting points, not universal requirements.

---

## 9.3 Line-height

Suggested ranges:

```text
Large display:
0.95–1.1

Headings:
1.05–1.2

Short UI labels:
1.1–1.3

Body text:
1.45–1.7

Dense metadata:
1.3–1.5
```

Large headings often need tighter line-height.

Paragraphs need more breathing room.

Do not use `line-height: 1` for multi-line body content.

---

## 9.4 Letter spacing

Use tracking intentionally.

Typical patterns:

### Large headings
```text
-0.04em to -0.01em
```

### Normal UI text
```text
0 to 0.01em
```

### Uppercase labels
```text
0.04em to 0.12em
```

### Small technical labels
Consider:
- monospace
- uppercase
- increased tracking

But do not overuse uppercase.

---

## 9.5 Avoid too many font weights

A typical high-quality system may use:

```text
400 / Regular
500 / Medium
600 / Semibold
700 / Bold
```

Sometimes only:

```text
400
500
600
```

is enough.

If everything uses 700, hierarchy becomes flat.

---

# 10. COLOR SYSTEM

## 10.1 Define semantic color tokens

Do not scatter raw hex values.

Example:

```text
Background
Background subtle
Surface
Surface elevated
Border subtle
Border strong

Text primary
Text secondary
Text muted
Text inverse

Accent
Accent hover
Accent subtle

Success
Warning
Danger
Info
```

---

## 10.2 Color hierarchy

A good interface often uses fewer saturated colors than inexperienced designers expect.

Suggested principle:

```text
Most of the interface:
Neutral

Important information:
High contrast

Interactive emphasis:
Accent

Critical states:
Semantic colors
```

Do not use five bright colors in every section.

---

## 10.3 Dark UI

For dark interfaces:

Avoid:
```text
Pure black background + pure white everything
```

Prefer layered neutrals:

```text
Base background
#0E0E10 style range

Surface
slightly lighter

Elevated surface
slightly lighter again

Borders
low-contrast neutral
```

Do not make every border equally visible.

Hierarchy can be created with:
- surface difference
- border difference
- spacing
- typography
- shadows

---

## 10.4 Light UI

For light interfaces:

Avoid:
- pure white everywhere
- heavy gray borders around every element
- excessive shadows

Use subtle variation:

```text
Page background
Warm/cool off-white

Surface
White or near-white

Border
Low contrast

Text
Near-black rather than always pure black
```

---

## 10.5 Accent colors

The accent color should answer:

> Why is the user's attention being directed here?

Use accent color for:

- primary CTA
- active navigation
- selected states
- key metric
- important status

Do not use accent color for every icon, heading, border, and button.

---

# 11. CONTRAST AND LEGIBILITY

Check:

- body text against background
- secondary text against background
- button label against button
- placeholder text
- disabled states
- focus indicators
- error messages

Do not reduce contrast merely to achieve a fashionable minimal look.

Minimalism is not low contrast.

---

# 12. BORDERS

Borders are often one of the biggest indicators of UI quality.

## 12.1 Use hierarchy

Recommended conceptual levels:

```text
Subtle:
barely visible

Default:
defines interactive grouping

Strong:
important separation
```

Avoid using the same dark or gray border around everything.

---

## 12.2 Border thickness

Usually:

```text
1px
```

is sufficient.

Use 2px when:
- focus state
- strong emphasis
- specific brand treatment

Do not use 2px borders everywhere unless it is an intentional brand style.

---

## 12.3 Border radius

Define a system.

Example:

```text
4px
8px
12px
16px
24px
9999px
```

Do not mix:
- 5px
- 11px
- 17px
- 21px

randomly.

Choose based on brand personality.

### More technical
4–10px

### Modern/product
8–16px

### Friendly/consumer
12–24px

### Pills
9999px

---

# 13. SHADOWS AND DEPTH

Use shadows to communicate elevation, not decoration.

### Low elevation
Very subtle.

### Medium elevation
Dropdowns, floating cards.

### High elevation
Modals, command palettes.

Avoid:
- huge blurry shadows
- dark gray blobs under every card
- identical shadows on all elements

Layered depth can also use:
- background color
- border
- blur
- subtle shadow

---

# 14. BUTTON DESIGN

## 14.1 Button hierarchy

Define:

1. Primary
2. Secondary
3. Tertiary / Ghost
4. Destructive
5. Icon button

Never make all actions look equally important.

---

## 14.2 Recommended heights

Common starting sizes:

```text
Small: 32–36px
Medium: 40–44px
Large: 48–52px
Hero: 52–60px
```

The size should correspond to context.

Do not use giant buttons inside dense dashboards.

---

## 14.3 Button padding

Typical:

```text
Horizontal:
12–24px

Vertical:
8–16px
```

Check optical balance when icons are included.

---

## 14.4 Button states

Every interactive button should consider:

```text
Default
Hover
Active
Focus-visible
Disabled
Loading
```

If an action triggers a network request:

- prevent accidental duplicate submissions
- show loading state
- preserve label context if possible

Example:

```text
Save
→ Saving…
→ Saved
```

---

# 15. INPUTS AND FORMS

## 15.1 Input anatomy

An input may include:

```text
Label
Optional hint
Input field
Optional leading icon
Optional trailing action
Error message
Success/help state
```

Do not rely only on placeholders for important labels.

---

## 15.2 Input states

Support:

- default
- hover
- focus
- filled
- disabled
- error
- success
- read-only

---

## 15.3 Form spacing

Recommended relationship:

```text
Label → input:
6–10px

Input → helper/error:
6–8px

Field → next field:
16–24px

Field group → action:
24–40px
```

---

## 15.4 Error messages

Errors should:

- explain what happened
- explain how to fix it
- be close to the relevant field

Bad:
```text
Invalid.
```

Better:
```text
Enter a valid work email address.
```

---

# 16. NAVIGATION UX

## 16.1 Desktop navigation

Navigation should:

- be easy to scan
- not contain too many top-level links
- have a visible primary CTA if conversion-oriented
- visually distinguish primary actions from normal navigation

Recommended top-level count:

```text
3–7 primary navigation items
```

More items may require grouping.

---

## 16.2 Sticky navigation

Use sticky navigation when it helps users:

- access important navigation
- return to a primary action
- maintain context

Do not make the sticky header unnecessarily tall.

Consider shrinking the header after scrolling.

---

## 16.3 Mobile navigation

Do not simply squeeze desktop navigation into mobile.

Check:

- touch target size
- menu height
- close action
- focus trapping for modal navigation
- keyboard accessibility
- scroll locking
- animation

Mobile navigation should feel like a coherent interface state.

---

# 17. HERO SECTION DESIGN

The hero should communicate:

1. What this is.
2. Who it is for.
3. Why it matters.
4. What the user should do next.

Within a few seconds, the visitor should understand the primary value.

---

## 17.1 Hero structure

Common pattern:

```text
Eyebrow / category
↓
Headline
↓
Supporting copy
↓
Primary CTA + secondary CTA
↓
Proof / metrics
↓
Product visual
```

Do not include every possible element if it weakens focus.

---

## 17.2 Headline quality

A good headline is:

- specific
- outcome-oriented
- understandable
- appropriate to the audience

Avoid generic phrases:

```text
The future of work
Reimagine everything
Power your workflow
Next-generation innovation
AI for everyone
```

unless followed by clear specifics.

---

## 17.3 Hero visual

Prefer:

- real product UI
- product workflow
- meaningful interactive demo
- original visual metaphor

Avoid:

- fake dashboard screenshots
- meaningless floating cards
- decorative gradients with no product relationship

---

# 18. SOCIAL PROOF

Social proof should reduce doubt.

Useful forms:

- customer logos
- customer metrics
- testimonials
- case studies
- recognizable customer names
- usage numbers
- ratings

Do not add a logo wall merely because every SaaS page has one.

Make proof relevant.

---

# 19. PRODUCT VISUALS

When showing product UI:

- Use realistic content.
- Use believable data.
- Show actual workflows.
- Avoid lorem ipsum when the visual is central to the page.
- Remove unnecessary noise.
- Highlight the relevant feature.

A product screenshot should answer:

> What am I looking at and why does it matter?

---

# 20. CARD DESIGN

Cards should be used when grouping is useful.

Do not put every paragraph inside a card.

A card should generally represent:

- a distinct object
- a distinct action
- a feature
- a selectable option
- a grouped concept

---

## Card checklist

Check:

- Does the card need a border?
- Does it need elevation?
- Is the padding sufficient?
- Are all cards the same height unnecessarily?
- Is there too much empty space?
- Is the clickable area clear?
- Does hover indicate interactivity?

---

# 21. DENSITY

Density should match the task.

### Marketing
More breathing room.

### Dashboard
Moderate density.

### Data tables
High density with strong structure.

### Developer tools
Often dense but highly organized.

Do not apply marketing-page spacing inside operational software.

---

# 22. RESPONSIVE DESIGN

Responsive design is not:

> Make desktop narrower until it fits.

Design responsive behavior intentionally.

---

## 22.1 Breakpoint thinking

Instead of blindly using device labels, respond to layout pressure.

Common ranges:

```text
Small:
0–639px

Medium:
640–1023px

Large:
1024–1279px

Extra large:
1280px+
```

Adapt based on the actual design.

---

## 22.2 Mobile-first questions

At small widths:

- What is essential?
- What can stack?
- What can collapse?
- What can become horizontally scrollable?
- What should become a drawer?
- What should disappear?
- What should move below the fold?

Do not hide important functionality without replacement.

---

## 22.3 Responsive typography

Avoid extreme jumps.

Use:
- clamp()
- fluid scales
- breakpoint-specific adjustments

Example concept:

```css
font-size: clamp(2rem, 5vw, 5rem);
```

Check the result visually.

---

# 23. TOUCH TARGETS

Interactive touch targets should generally be large enough to tap comfortably.

Aim for approximately:

```text
44 × 44px minimum target area
```

The visible icon may be smaller.

Example:

```text
Icon: 18px
Button target: 44px
```

---

# 24. ACCESSIBILITY

Accessibility is part of UX quality.

Check:

- semantic headings
- button semantics
- link semantics
- form labels
- keyboard navigation
- focus visibility
- contrast
- screen reader labels
- reduced motion
- error identification

---

## 24.1 Focus states

Never remove focus outlines without replacing them.

A good focus state should be:

- visible
- consistent
- high contrast
- not confused with hover

---

## 24.2 Keyboard navigation

Test:

```text
Tab
Shift + Tab
Enter
Space
Escape
Arrow keys where appropriate
```

Check:

- logical order
- focus trapping in modals
- dropdown navigation
- escape behavior

---

# 25. MICRO-INTERACTIONS

Micro-interactions should communicate state.

Good uses:

- hover feedback
- toggle transition
- save confirmation
- loading progress
- drag feedback
- selection feedback

Avoid animation that delays the user.

---

## 25.1 Duration guidance

Typical:

```text
Very small state:
100–150ms

Hover:
150–220ms

Standard transition:
180–300ms

Large panel/modal:
200–400ms
```

Use easing appropriate to the movement.

Avoid:
- 800ms button hovers
- unnecessary bounces
- animations that replay on every scroll

---

# 26. LOADING STATES

Do not leave users staring at a blank interface.

Choose:

### Skeleton
When layout is predictable.

### Spinner
When waiting state is short and location-specific.

### Progress indicator
When duration can be estimated.

### Optimistic update
When action can safely appear immediate.

Avoid fake loading delays.

---

# 27. EMPTY STATES

An empty state should answer:

1. What is empty?
2. Why is it empty?
3. What can the user do next?

Example:

```text
No projects yet

Create your first project to organize your work.

[Create project]
```

Do not use a sad illustration without useful next steps.

---

# 28. ERROR STATES

Errors should be:

- visible
- understandable
- actionable
- specific

Example:

Bad:
```text
Something went wrong.
```

Better:
```text
We couldn't save your changes. Check your connection and try again.
```

Best:
```text
We couldn't save your changes because your session expired.

[Sign in again]
```

---

# 29. SUCCESS STATES

Success should confirm completion without interrupting the workflow.

Use:

- inline confirmation
- toast
- button state
- completion screen when appropriate

Do not show a modal for every successful click.

---

# 30. TABLE DESIGN

Tables should optimize scanning.

Use:

- clear headers
- consistent alignment
- numeric alignment
- sufficient row height
- visible hover
- selected state
- sorting indication
- responsive strategy

Do not force a wide desktop table into a narrow mobile screen without planning.

Possible mobile strategies:

- horizontal scrolling
- card transformation
- reduced columns
- detail view

---

# 31. MODALS AND DIALOGS

Use modals for focused interruptions.

A modal should have:

- clear purpose
- clear title
- understandable content
- clear actions
- close mechanism
- escape key behavior
- focus management

Avoid modal chains.

---

# 32. DROPDOWNS

Dropdowns should:

- open near the trigger
- remain within viewport
- support keyboard navigation
- close appropriately
- visually indicate active state

Avoid tiny menus with tiny text.

---

# 33. TOOLTIPS

Use tooltips for supplementary explanation.

Do not hide essential information inside a tooltip.

Support:
- hover
- keyboard focus

Avoid tooltips that:
- cover important controls
- disappear too quickly
- contain long paragraphs

---

# 34. ICONS

Use icons consistently.

Check:

- stroke weight
- filled vs outline style
- optical size
- baseline alignment
- icon spacing

Do not mix:
- 16px thin icons
- 24px bold icons
- emoji
- random SVG styles

without intentional visual reason.

---

# 35. IMAGE AND MEDIA TREATMENT

Check:

- aspect ratio
- crop
- border radius
- object position
- loading behavior
- responsive size

Avoid distorted images.

Do not use decorative imagery when product UI would explain the product better.

---

# 36. VISUAL RHYTHM

Visual rhythm is the repeated pattern of:

- spacing
- alignment
- typography
- component scale

A polished page feels organized because elements follow a rhythm.

Inspect for accidental irregularity:

```text
24px
37px
19px
42px
27px
```

If those values are random, the page may feel unstable.

---

# 37. OPTICAL ALIGNMENT

Mathematical alignment is not always visually correct.

Examples:

- Icons may need a 1px vertical adjustment.
- Rounded shapes may appear lower than square shapes.
- A logo may need different padding than its bounding box suggests.
- Text and icons may need baseline tuning.

When something feels misaligned, inspect visually rather than assuming the CSS is correct because all values are mathematically equal.

---

# 38. SMALL DETAILS THAT MUST BE CHECKED

Always inspect:

## Text
- orphan words
- awkward line breaks
- accidental wrapping
- heading widow lines
- overly wide paragraphs
- inconsistent punctuation
- inconsistent capitalization

## Buttons
- icon spacing
- equal vertical centering
- disabled appearance
- loading width changes
- hover feedback

## Cards
- consistent padding
- content alignment
- equal border treatment
- hover state only when interactive

## Inputs
- label alignment
- placeholder contrast
- error spacing
- icon alignment

## Navigation
- active state
- hover state
- keyboard focus
- mobile behavior

## Sections
- top spacing
- bottom spacing
- alignment with container
- visual transition between backgrounds

## Screenshots/product UI
- realistic scale
- readable enough to understand
- no accidental clipping
- no fake meaningless content

---

# 39. LANDING PAGE STRUCTURE

A strong SaaS landing page often follows:

```text
1. Navigation
2. Hero
3. Immediate proof
4. Product demonstration
5. Core value/feature explanation
6. How it works
7. Additional capabilities
8. Customer proof
9. Security/integration/enterprise proof
10. Pricing or CTA
11. FAQ
12. Final CTA
13. Footer
```

Do not include every section automatically.

Remove sections that do not help the user understand or convert.

---

# 40. UX COPY GUIDELINES

UI copy should be:

- direct
- specific
- concise
- action-oriented

Buttons should use verbs.

Better:

```text
Create project
Save changes
Invite teammate
Start free trial
View report
```

Less clear:

```text
Continue
Submit
Click here
Proceed
Yes
```

unless context is extremely obvious.

---

# 41. CTA HIERARCHY

Every major page should have a clear CTA strategy.

Example:

```text
Primary:
Start free trial

Secondary:
Watch demo

Tertiary:
Learn more
```

Do not create:

```text
Get started
Book demo
Contact us
See product
Try now
View pricing
Learn more
```

all with equal visual weight in one hero.

---

# 42. DESIGN TOKENS

Use a centralized token system.

Example conceptual structure:

```text
--color-bg
--color-surface
--color-surface-elevated
--color-border
--color-border-strong

--color-text
--color-text-secondary
--color-text-muted

--color-accent
--color-accent-hover

--space-1
--space-2
--space-3
...

--radius-sm
--radius-md
--radius-lg

--shadow-sm
--shadow-md
--shadow-lg
```

Do not repeat magic values across components.

---

# 43. COMPONENT CONSISTENCY

A design system should answer:

- What does a primary button look like?
- How tall is an input?
- What border radius do cards use?
- How does focus look?
- What is the spacing between icon and label?
- How does a destructive action look?

Do not redesign these decisions separately on every screen.

---

# 44. WHEN TO USE VISUAL REFERENCES

Use visual reference research especially when:

- the user requests premium UI
- the product needs a landing page
- the design is vague
- a redesign is requested
- the current UI looks generic
- the product category has strong established patterns

Reference research should answer:

```text
What works?
Why does it work?
What is appropriate for this product?
What should not be copied?
```

---

# 45. REFERENCE RESEARCH TEMPLATE

For each reference website:

## Reference
Name:

## URL
Live website URL:

## Product category
SaaS / developer tool / consumer / enterprise / ecommerce / etc.

## Screenshot states captured
- Desktop:
- Mobile:
- Interaction:

## What works
- 

## Typography observations
- 

## Spacing observations
- 

## Color observations
- 

## CTA observations
- 

## Navigation observations
- 

## Product visual observations
- 

## Interaction observations
- 

## Principles to adapt
- 

## Things NOT to copy
- 

---

# 46. IMPLEMENTATION WORKFLOW

## Phase 1 — Understand

Read the request.

Identify:

- audience
- goal
- constraints
- content
- conversion action
- platform

---

## Phase 2 — Research

When useful:

1. Select references.
2. Open with Playwright MCP.
3. Wait for rendering.
4. Use `listWindows`.
5. Identify the correct browser window.
6. Use the dedicated screenshot tool.
7. Capture meaningful visual states.
8. Analyze screenshots.

---

## Phase 3 — Define system

Define:

- layout grid
- container width
- spacing scale
- typography scale
- color tokens
- radius system
- shadows
- component states

---

## Phase 4 — Wireframe hierarchy

Before adding decoration:

```text
Navigation
Hero
Primary content
CTA
Supporting sections
Footer
```

Check whether the narrative makes sense without color.

---

## Phase 5 — Build

Implement:

- semantic HTML
- reusable components
- responsive layout
- accessibility states

---

## Phase 6 — Visual refinement

Inspect:

- screenshot
- browser
- desktop
- mobile

Fix:

- spacing
- typography
- alignment
- color balance
- component states

---

## Phase 7 — Interaction QA

Test:

- hover
- focus
- active
- loading
- error
- empty
- disabled

---

# 47. SCREENSHOT-BASED QA LOOP

Use visual QA.

Recommended loop:

```text
Implement
↓
Open page
↓
Use listWindows
↓
Capture screenshot with screenshot tool
↓
Compare visually with intended hierarchy
↓
Identify issues
↓
Fix
↓
Capture again
↓
Repeat
```

Do not rely only on:

```text
Build passed
Lint passed
No console errors
```

Those checks do not prove visual quality.

---

# 48. VISUAL QA CHECKLIST

## Alignment
- [ ] Header aligns with page content.
- [ ] Major sections share a consistent grid.
- [ ] Text blocks align intentionally.
- [ ] Icons are optically centered.
- [ ] Buttons are vertically aligned.

## Spacing
- [ ] No accidental cramped areas.
- [ ] No accidental huge gaps.
- [ ] Related elements are closer than unrelated elements.
- [ ] Section spacing follows narrative structure.

## Typography
- [ ] H1 is dominant.
- [ ] H2 hierarchy is clear.
- [ ] Paragraphs are readable.
- [ ] Small text is legible.
- [ ] Line breaks are intentional.

## Color
- [ ] Accent has a clear purpose.
- [ ] Contrast is sufficient.
- [ ] Surfaces are distinguishable.
- [ ] Semantic colors are consistent.

## Components
- [ ] Buttons have states.
- [ ] Inputs have states.
- [ ] Cards are consistent.
- [ ] Navigation states are clear.

## Responsive
- [ ] Mobile is not a compressed desktop.
- [ ] No horizontal overflow.
- [ ] Touch targets are usable.
- [ ] Text remains readable.
- [ ] CTA remains discoverable.

---

# 49. ANTI-PATTERNS

Avoid:

## Generic AI landing page syndrome

Symptoms:

- giant gradient blob
- floating glass cards
- meaningless badge
- "AI-powered" everywhere
- fake dashboard
- three pricing cards
- logo wall
- generic feature grid

without a product-specific story.

---

## Too many cards

Do not put:

```text
Heading inside card
Card inside card
Card inside section
```

unless grouping requires it.

---

## Too much border

A border around every element makes the interface noisy.

---

## Too much shadow

Shadows should communicate depth.

---

## Too many gradients

One intentional gradient can work.

Seven gradients usually weaken hierarchy.

---

## Over-animation

Motion should not become the content.

---

## Tiny text

Do not sacrifice usability for density.

---

## Low-contrast minimalism

Minimal does not mean unreadable.

---

# 50. PREMIUM UI HEURISTICS

A premium interface usually has:

- consistency
- restraint
- intentional spacing
- excellent typography
- realistic product details
- polished interaction states
- clear hierarchy
- no unnecessary visual noise

It does NOT require:

- excessive glassmorphism
- huge gradients
- complicated animations
- dozens of colors
- oversized rounded cards

---

# 51. FINAL DESIGN REVIEW QUESTIONS

Before finalizing, ask:

## Clarity
Can a new user understand the purpose quickly?

## Hierarchy
Is the most important thing visually dominant?

## Action
Is the primary action obvious?

## Consistency
Do repeated components behave and look consistent?

## Density
Is the page appropriate for its purpose?

## Responsiveness
Does the design work on small screens?

## Accessibility
Can users navigate and understand the interface without relying on color or a mouse?

## Craft
Have the small details been checked?

---

# 52. REQUIRED FINAL QUALITY BAR

Do not finalize a UI merely because:

- it works
- it compiles
- it resembles a common template
- all requested sections exist

Finalize only after checking:

```text
Structure
Hierarchy
Spacing
Typography
Color
Contrast
Alignment
Interaction
Responsive behavior
Accessibility
Visual polish
```

---

# 53. HIGH-FIDELITY DESIGN STANDARD

When a user asks for a premium, modern, or high-quality interface:

1. Do not immediately produce a generic layout.
2. Research relevant visual references.
3. Use Playwright MCP to open reference landing pages.
4. Use `listWindows` to identify the correct browser window.
5. Use the dedicated screenshot tool to capture visual references.
6. Do not use MCP screenshot as the primary reference screenshot mechanism.
7. Analyze screenshots visually.
8. Extract principles instead of copying pixels.
9. Define a consistent design system.
10. Implement an original interface.
11. Capture your implementation for visual QA.
12. Refine small details until the layout feels intentional.

---

# 54. QUICK EXECUTION CHECKLIST

## Before coding
- [ ] Understand product.
- [ ] Understand user.
- [ ] Define primary action.
- [ ] Identify relevant references.
- [ ] Open references using Playwright MCP.
- [ ] Use `listWindows`.
- [ ] Use screenshot tool.
- [ ] Analyze screenshots.

## During design
- [ ] Establish spacing scale.
- [ ] Establish typography scale.
- [ ] Establish color tokens.
- [ ] Establish component states.
- [ ] Define layout grid.

## During implementation
- [ ] Use semantic structure.
- [ ] Make components reusable.
- [ ] Add responsive behavior.
- [ ] Add accessibility.
- [ ] Add loading/error/empty states.

## Before completion
- [ ] Capture implementation screenshot.
- [ ] Inspect alignment.
- [ ] Inspect spacing.
- [ ] Inspect typography.
- [ ] Inspect color.
- [ ] Inspect responsiveness.
- [ ] Inspect interactions.
- [ ] Fix small visual issues.

---

# 55. REFERENCE SITES TO CONSIDER

Use these as starting points when relevant. Always inspect the live page rather than assuming the design is unchanged.

### Product-led SaaS
- CodeRabbit
- Linear
- Vercel
- Attio
- PostHog
- Cursor
- Resend

### Marketing and visual storytelling
- Stripe
- Framer
- Teak

### Productivity and information design
- Notion
- Linear

### Developer products
- Vercel
- CodeRabbit
- Resend
- PostHog
- Cursor

Select references based on the actual product. Do not force a fintech website to look like a gaming CRM or a developer tool.

---

# 56. FINAL PRINCIPLE

The difference between an average interface and an excellent one is often not a major visual idea.

It is the accumulation of small decisions:

- the heading breaks on the right word
- the paragraph is the right width
- the CTA is visually obvious
- the icon sits correctly beside the text
- the border is subtle enough
- the hover transition is fast enough
- the card has the right amount of internal padding
- the mobile layout is intentionally redesigned
- the empty state gives a useful next step
- the focus state is visible
- the page does not contain unnecessary visual noise

Treat every visible detail as part of the user experience.

> **Good UI is not the number of effects added. Good UI is the number of unnecessary decisions removed while preserving clarity, personality, and usefulness.**

---

# 57. SOURCE REFERENCE NOTES

The live websites and screenshots should always be treated as current visual references rather than permanent specifications. Website designs change.

When studying a reference:

- Open the live page.
- Inspect the current version.
- Capture the current visual state.
- Analyze it.
- Use the principles, not the exact copyrighted composition or branding.

Suggested starting references include the official sites of CodeRabbit and Teak, plus current high-quality SaaS examples appropriate to the task.

End of skill.
