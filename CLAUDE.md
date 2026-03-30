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
- Bilingual: filename-based i18n (`.md` = EN, `.ko.md` = KO)
- Blog posts: `content/blog/{slug}/index.md` (page bundle)
- Projects (top-level): `content/projects/{name}/_index.md` (section)
- Projects (child): `content/projects/{parent}/{name}.md`
- About: `content/about/_index.md`

## Deployment
- GitHub Pages via GitHub Actions (auto-deploy on push to master)
- Repo: beelinkfarm/daege-blog
- Live: https://beelinkfarm.github.io/daege-blog/

---

## Blog Post Writing Guide

### Workflow
1. **Request to AI:** "이런 주제로 글 써줘" → AI가 아래 양식에 맞게 작성 + git push → 자동 배포
2. **Direct writing:** `content/blog/{slug}/index.md` 생성 → git push → 자동 배포

### Post Types

**Type 1: Project Build Log** (프로젝트 제작 과정)
- A project's story from idea to deployment
- Must link to the corresponding project page in `/projects/`

**Type 2: Technical Deep Dive** (기술 딥다이브)
- In-depth exploration of a specific technology, pattern, or API
- Code examples required

**Type 3: Tool Review** (도구 리뷰)
- Honest assessment of a tool/service actually used
- Must include pros, cons, and verdict

**Type 4: General / Opinion** (일반 / 의견)
- Thoughts on the industry, trends, or lessons learned

### Frontmatter Template (required fields)

```yaml
---
title: "Clear, Specific Title — Not Clickbait"
date: YYYY-MM-DD
summary: "1-2 sentence description for cards and SEO. Be specific."
tags: ["Tag1", "Tag2"]          # 2-5 tags, existing tags preferred
categories: ["Category"]        # One of: AI Tools, Web Dev, Automation, General
draft: false                    # true = hidden from production
---
```

### Section Structure (all posts must follow)

```markdown
## Opening (1-2 paragraphs)
What this post is about and why it matters. No fluff.

## Main Content (2-5 sections with ## headings)
The substance. Use code blocks, bullet points, and tables where appropriate.

## Key Takeaways (or "What I Learned")
3-5 bullet points summarizing the value. Readers who skim should get value here.
```

### Tone & Style Rules

- **Language:** English primary. Write as a practitioner, not a lecturer.
- **Voice:** First person ("I built", "I found"), direct, honest.
- **No fluff:** Skip "In this post, I will..." — just start.
- **Code examples:** Always include runnable/realistic code, not pseudocode.
- **Specifics over generalities:** "Reduced build time from 12s to 3s" > "Significantly improved performance"
- **Honesty about failures:** Document what didn't work and why. This builds trust.
- **Length:** 800-2000 words for blog posts. Quality > quantity.

### Korean Translation

- Every post should have a `.ko.md` version
- Translate naturally, not literally — adapt idioms and examples
- Keep code blocks and technical terms in English
- Korean tags use the Korean equivalents defined in existing posts

### File Naming

- Blog: `content/blog/{slug}/index.md` + `index.ko.md`
  - Slug: lowercase, hyphens, descriptive (e.g., `building-micro-tool-generator`)
- New project: `content/projects/{parent}/_index.md` or `content/projects/{name}.md`

### Adding a New Project

1. Determine if standalone or child of Dongili Tools / Micro Tool Gen
2. Create page with Live Demo + Source Code buttons
3. Include: Overview, Features/How It Works, Tech Stack sections
4. Add both EN and KO versions

### Categories & Tags (use existing when possible)

**Categories:** AI Tools, Web Tools, Browser Tools, Web Dev, Automation, General
**Common tags:** AI, Python, TypeScript, Claude API, FastAPI, Automation, Data, n8n

### Pre-publish Checklist

- [ ] Frontmatter complete (title, date, summary, tags, categories)
- [ ] Korean translation exists
- [ ] Links work (internal project links, external URLs)
- [ ] Code blocks have language specified (```python, ```bash, etc.)
- [ ] Summary is specific and under 160 characters (SEO)
- [ ] `hugo` builds without errors
