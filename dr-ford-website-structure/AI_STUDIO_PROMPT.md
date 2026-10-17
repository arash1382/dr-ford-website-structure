# Google AI Studio Build Mode — Initial Prompt

Build a polished, responsive bilingual website for **Dr. Ford**, an AI education school serving individual learners and organizations. Read `CUSTOM_INSTRUCTIONS.md` and the files in `docs/` as project requirements when available.

## Reference
Use https://taxo.ai/ for information hierarchy, section rhythm, and refined interactions. Do not copy its exact layouts, branding, content, illustrations, or assets.

## Design system
- Background `#080A09`
- Secondary background `#101411`
- Elevated surface `#171B18`
- Primary text `#F5F7F5`
- Secondary text `#A8AEA9`
- Accent phosphor lime `#B7FF00`
- No orange.
Use strong typography, generous negative space, precise grids, and restrained geometric visuals. If the official circular maze logo is supplied, derive subtle path motion from its geometry. Until then, use a neutral geometric placeholder, not a fabricated logo.

## Sitemap
- Home
- Courses: general courses, private courses, individual course details
- Events and Course Locations
- About Dr. Ford: philosophy, founders, educational approach
- Projects and Achievements
- Contact and Registration

## Homepage sections
1. Hero: concise positioning, CTA to explore courses, secondary CTA to learn about Dr. Ford.
2. Introduction: what the school is and its approach.
3. Learning paths: general and private courses.
4. Course delivery/events: show only confirmed dates and venues.
5. Impact: use only verified statistics; otherwise omit or mark development placeholders clearly.
6. Founders: horizontal gallery using supplied, approved portraits and names only.
7. Partners: horizontal logo carousel using approved logos only.
8. Why Dr. Ford: differentiators supported by supplied facts.
9. FAQ: accessible accordion with editable content.
10. Final CTA: course discovery and contact/registration.

## Language and functionality
- Visible Persian/English language switcher.
- Persian uses `lang="fa"` and `dir="rtl"`; English uses `lang="en"` and `dir="ltr"`.
- Switching language updates all visible text and layout direction.
- Responsive desktop, tablet, and mobile layouts.
- Functional navigation and CTAs, accessible keyboard/touch carousels, FAQ accordion, labelled and validated forms.
- Respect `prefers-reduced-motion`; do not hijack scrolling or delay access to content.
- Forms must clearly state if submission is not connected to a backend.
- Keep course, event, founder, partner, and FAQ content in data files separate from UI components.
- Use the React setup available in Google AI Studio Build Mode; inspect the generated project before adding dependencies.
- Do not invent real names, partner brands, schedules, locations, prices, statistics, or testimonials.

## First milestone
Build a visually polished, working homepage and navigation/language switcher first. Use clearly editable placeholders only where necessary. Then check routes, dead controls, RTL/LTR behavior, mobile overflow, console errors, focus states, and reduced-motion behavior. Summarize remaining placeholders and integrations.

## Source-code reference analysis
If the archive `taxo.ai (1).zip` is provided to the project, use it as a technical reference only. Read `docs/TAXO_SOURCE_ANALYSIS.md`. Inspect the HTML, CSS, and JavaScript to understand section structure, component boundaries, responsive patterns, and interaction behavior. Do not use its images, fonts, logo, copy, or brand assets. Do not copy minified Framer bundles into this project. First summarize observed patterns and uncertainties, then implement independent, clean React components adapted to Dr. Ford's sitemap and brand.
