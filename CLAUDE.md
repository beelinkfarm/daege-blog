# Daege Blog

Hugo static blog + portfolio using Blowfish theme.

## Stack
- Hugo extended >= 0.117.0
- Blowfish theme (git submodule)
- Tailwind CSS (via Blowfish)

## Design System
Always read DESIGN.md before making any visual or UI decisions.
All font choices, colors, spacing, and aesthetic direction are defined there.
Do not deviate without explicit user approval.
In QA mode, flag any code that doesn't match DESIGN.md.

## Commands
```bash
hugo server --buildDrafts    # dev server
hugo                         # build to public/
```

## Content Structure
- content/en/ — English (primary)
- content/ko/ — Korean
- Blog posts: content/{lang}/blog/
- Projects: content/{lang}/projects/
- About: content/{lang}/about/
