# Shoumik Ahmed — Portfolio Design Direction

## Design intent

A minimal, editorial portfolio for classmates, recruiters, and collaborators. The site should feel calm and deliberate: strong typography, generous whitespace, subtle motion, and enough technical texture to communicate software quality without looking like a generic developer template.

Working positioning:

> Computer Science student building reliable software and thoughtful developer experiences.

The visual language is inspired by the assignment reference's clear sectioning and navigation, but modernized into a single smooth scrolling experience with a compact sticky menu.

## Page structure

### 1. Sticky navigation

Left: `SHOUMIK AHMED` as a small wordmark.

Right: `About` · `Experience` · `Projects` · `Resume` · `Contact`.

The active section is indicated by a thin accent line. On mobile, the links collapse into a simple menu button.

### 2. Home / introduction

Full-height opening section with:

- Eyebrow: `COMPUTER SCIENCE · YORK UNIVERSITY`
- Main statement: `I build reliable software, then make it feel effortless.`
- Short summary grounded in the resume: Computer Science student with experience in test automation, API validation, CI/CD, debugging, and data-driven product quality.
- Two calls to action: `View projects` and `Download resume`.
- A small visual signature on the right: an abstract system map made from rounded nodes and thin connector lines, not a stock photo.

This satisfies the required professional introduction while keeping the opening personal and memorable.

### 3. About / what I care about

Three concise principles presented as text-led cards:

- `Make the path obvious` — clear interfaces and maintainable systems.
- `Test the edges` — automation, observability, and careful debugging.
- `Keep learning in public` — curiosity across product, data, and software design.

Include a brief note about the most rewarding co-op learning experience: tracing failures from Jenkins results, application logs, and New Relic monitoring into actionable fixes at Genesys.

### 4. Experience timeline

A vertical timeline with two work entries and one community entry:

- **Genesys — Software Developer in Test Intern** · May 2026–Dec 2026
  Kotlin API tests, Playwright end-to-end UI tests, Jenkins pipelines, New Relic, Git, Agile collaboration.
- **Dayforce — QA Analyst Intern** · Sept 2024–Apr 2025
  300+ manual test cases, 20+ Playwright regression tests, SQL Server validation, Jira defect tracking.
- **Lassonde Fall Campus Day — Keynote Presenter** · Sept 2023
  Presented to 200+ attendees and helped increase prospective student inquiries.

Use restrained metrics as proof points, not oversized dashboard cards.

### 5. Selected projects

Three project cards with expandable detail panels. Each panel includes title, description, tools, role/contribution, outcome, and a repository/demo link when available.

1. **AI Form Autofill App**
   AI-powered form completion concept that reduced completion time by 40% and improved data accuracy by 30%.
   Tags: AI · automation · UX · hackathon.
2. **Cruise Critic Database & Analytics**
   SQL Server and Power BI star-schema analytics layer for revenue, profitability, and destination demand.
   Tags: SQL · Power BI · DAX · analytics.
3. **Test Automation Toolkit**
   A portfolio case study built from the resume's testing practice: reusable Playwright patterns, API checks, failure triage, and regression thinking. This is clearly labeled as a learning/case-study piece unless a public repository is supplied.
   Tags: Playwright · TypeScript · APIs · CI/CD.

The third card is intentionally a case-study placeholder so we do not invent a project claim; it can be replaced with a real repository before publishing.

### 6. Skills / toolkit

Compact grouped list rather than a percentage bar chart:

- Languages: Java, Python, C++, Kotlin, JavaScript, TypeScript, SQL
- Frontend: HTML, CSS, React, Node.js
- Testing & quality: Playwright, Selenium, Postman, Jira, New Relic, debugging
- Systems & delivery: REST APIs, microservices, Docker, Jenkins, CI/CD, Linux, cloud platforms
- Data & design: Power BI, DAX, Excel, Google Sheets, Figma

### 7. Resume and contact

A dark, high-contrast closing band:

- `Want to build something dependable?`
- Email: `shoumik@my.yorku.ca`
- LinkedIn and GitHub links supplied by the user before implementation
- Downloadable, up-to-date resume

Do not include the phone number or home address in the public portfolio. The assignment explicitly calls for contact information without a home address, and the site should stay privacy-conscious.

## Visual system

### Palette

- Canvas: `#F6F7F4` warm off-white
- Ink: `#101312` near-black green
- Secondary text: `#66706A`
- Borders: `#DDE2DC`
- Accent: `#D86B4B` terracotta
- Accent wash: `#F0D9CF`
- Closing band: `#17211D`

### Typography

- Display: a high-contrast serif for the hero statement and project titles.
- Body/UI: a clean sans-serif for navigation, labels, metadata, and longer text.
- Large type should be fluid and responsive; body copy stays comfortably readable at 16–18px.

### Shape and motion

- 1px rules, 12–18px corner radii, and pill-shaped metadata tags.
- Reveal sections with a short upward fade as they enter the viewport.
- Project cards lift by a few pixels on hover; connector lines in the hero drift very subtly.
- Respect `prefers-reduced-motion` and keep every interaction usable without animation.

## Responsive behavior

- Desktop: two-column hero and project grid; sticky navigation remains visible.
- Tablet: preserve two columns where space allows, reduce display scale.
- Mobile: single-column flow, compact nav drawer, timeline becomes a simple stacked list, project details open inline.

## Content and privacy checklist before coding

- Add the user's actual LinkedIn, GitHub, and portfolio URLs.
- Confirm whether the AI Form Autofill and Cruise Critic project links are public.
- Replace or confirm the third project case study.
- Decide whether a professional photo is available. The initial design uses an abstract system graphic so the site does not depend on a photo.
- Add the final resume PDF as a download asset, without exposing the phone number elsewhere on the page.

## First-screen wireframe

```text
┌──────────────────────────────────────────────────────────────────────┐
│ SHOUMIK AHMED                 About  Experience  Projects  Resume  ↗ │
├──────────────────────────────────────────────────────────────────────┤
│ COMPUTER SCIENCE · YORK UNIVERSITY                                  │
│                                                                      │
│ I build reliable software,                                          │   abstract
│ then make it feel effortless.                                       │   system map
│                                                                      │
│ Testing, automation, and thoughtful interfaces                        │
│ for products people can trust.                                      │
│                                                                      │
│ [ View projects ]   [ Download resume ]                             │
└──────────────────────────────────────────────────────────────────────┘
```

## Build order after approval

1. Create the responsive visual shell and navigation.
2. Implement the introduction, experience, projects, skills, and contact sections.
3. Add the real external links and resume download.
4. Add restrained motion, accessibility states, and reduced-motion support.
5. Preview at desktop and mobile sizes, then prepare the project for Vercel deployment.
