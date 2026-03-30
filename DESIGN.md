# Design System — Daege

## Product Context
- **What this is:** AI/IT developer blog + project portfolio showcase
- **Who it's for:** US-based potential clients, hiring managers, developer community
- **Space/industry:** Developer portfolio / tech blog
- **Project type:** Static site (Hugo + Blowfish theme)

## Aesthetic Direction
- **Direction:** Industrial-Minimal — function-first, data-dense developer feel with sharp typographic hierarchy
- **Decoration level:** Intentional — subtle grid lines, code block styling. No decorative blobs or illustrations.
- **Mood:** Professional but approachable. Like a well-organized workshop — everything has a place, tools are visible, craft is evident.
- **Reference sites:** brittanychiang.com (dark+accent), leerob.io (extreme minimal), joshwcomeau.com (interactive+content)

## Typography
- **Display/Hero:** Clash Grotesk (600) — geometric, bold, modern. Stands out from the Inter/Roboto crowd.
- **Body:** Plus Jakarta Sans (400, 500, 600) — warm, readable sans-serif with personality
- **UI/Labels:** JetBrains Mono (400) — monospace for labels, dates, section markers, nav accents
- **Data/Tables:** JetBrains Mono (tabular-nums) — consistent column alignment
- **Code:** JetBrains Mono (400, 500)
- **Loading:** Bunny Fonts CDN (Plus Jakarta Sans, JetBrains Mono) + Fontshare (Clash Grotesk)
- **Scale:**
  - xs: 12px / 0.75rem
  - sm: 13px / 0.8125rem
  - base: 16px / 1rem
  - lg: 18px / 1.125rem
  - xl: 20px / 1.25rem
  - 2xl: 24px / 1.5rem
  - 3xl: 32px / 2rem
  - 4xl: 48px / 3rem
  - 5xl: 56px / 3.5rem

## Color

### Dark Mode (default)
- **Approach:** Restrained — cyan accent carries all emphasis, violet as secondary for taxonomy
- **Background:** #0C0E12 — near-black with subtle blue tint
- **Surface:** #161920 — cards, code blocks, elevated elements
- **Surface hover:** #1E2028
- **Primary text:** #E4E4E7 — bright gray, high contrast
- **Muted text:** #71717A — secondary content, dates, labels
- **Accent (cyan):** #22D3EE — links, CTAs, hover states, primary emphasis
- **Accent hover:** #06B6D4
- **Accent secondary (violet):** #A78BFA — tags, categories, taxonomy
- **Border:** #27272A
- **Semantic:**
  - Success: #34D399
  - Warning: #FBBF24
  - Error: #F87171
  - Info: #60A5FA

### Light Mode
- **Background:** #FAFAFA
- **Surface:** #FFFFFF
- **Surface hover:** #F4F4F5
- **Primary text:** #18181B
- **Muted text:** #71717A
- **Accent:** #0891B2 — darker cyan for light backgrounds
- **Accent hover:** #0E7490
- **Accent secondary:** #7C3AED — darker violet
- **Border:** #E4E4E7

## Spacing
- **Base unit:** 4px
- **Density:** Comfortable
- **Scale:**
  - 2xs: 2px
  - xs: 4px
  - sm: 8px
  - md: 16px
  - lg: 24px
  - xl: 32px
  - 2xl: 48px
  - 3xl: 64px

## Layout
- **Approach:** Grid-disciplined — blog single column (readability), project gallery 2-3 column cards
- **Grid:** 1 col (mobile) / 2 col (tablet) / 3 col (desktop, projects only)
- **Max content width:** 960px (blog body: 720px)
- **Border radius:**
  - sm: 4px (tags, small elements)
  - md: 8px (cards, buttons, inputs)
  - lg: 12px (large cards, modals)
  - full: 9999px (pills, status badges)

## Motion
- **Approach:** Minimal-functional — page transitions and hover states only
- **Easing:** enter(ease-out) exit(ease-in) move(ease-in-out)
- **Duration:**
  - micro: 50-100ms (hover color change)
  - short: 150-250ms (button transitions, card hover lift)
  - medium: 250-400ms (theme toggle, page transitions)
  - long: 400-700ms (not used — keep it snappy)
- **Hover effects:** Cards lift 2px (translateY), border color shifts to accent

## Component Patterns
- **Navigation:** Logo left, links center/right, language toggle (EN/KO) far right
- **Section labels:** JetBrains Mono, uppercase, accent-secondary color, 0.08em letter-spacing
- **Project cards:** Surface bg, border, 24px padding, hover: border→accent + translateY(-2px)
- **Blog posts:** Borderless, date (mono) + title (Clash Grotesk) + excerpt (Jakarta Sans) + tags
- **Tags:** Mono font, pill shape, surface bg + violet text + border
- **Buttons:** Primary (cyan bg, dark text), Secondary (cyan border + text), Ghost (muted text)
- **Code blocks:** Surface bg, mono font, cyan text, border, 16px padding

## Decisions Log
| Date | Decision | Rationale |
|------|----------|-----------|
| 2026-03-30 | Clash Grotesk for display | Geometric, bold — differentiates from Inter/Roboto-heavy developer sites |
| 2026-03-30 | Cyan + Violet dual accent | Cyan for primary actions, violet for taxonomy — creates information hierarchy beyond single-accent sites |
| 2026-03-30 | Dark mode default | Matches AI/IT developer brand, reduces eye strain, industry standard for dev portfolios |
| 2026-03-30 | Industrial-Minimal aesthetic | Function-first approach that lets content and projects speak for themselves |
| 2026-03-30 | JetBrains Mono for UI labels | Monospace accents add technical credibility and visual rhythm |
