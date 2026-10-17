# Taxo Source-Code Analysis Brief for Google AI Studio

## Purpose

Use the supplied `taxo.ai (1).zip` archive as a **technical reference** for understanding how the Taxo page is structured and how its interactions are implemented. The goal is to recreate suitable architectural and interaction patterns for the Dr. Ford website using clean, maintainable code.

**Do not use Taxo's images, fonts, logos, copy, brand styling, or other visual assets.** The archive is supplied to study implementation patterns and page structure only.

## What the archive contains

The inspected archive contains 129 entries, including:
- `taxo.ai/index.html` — a large saved HTML document (about 547 KB) containing page markup, generated classes, metadata, and references to runtime assets.
- Framer-generated JavaScript modules, including `script_main.jF5U1wHY.mjs` and multiple page/component bundles.
- React, Framer Motion, Framer runtime, and other supporting modules.
- A Lenis smooth-scroll stylesheet/runtime reference.
- Custom or embedded modules with names such as `FollowCursor_Prod`, `ShimmerGrid_Prod`, `AvoidLayoutJumping_Prod`, and `AnimatedNumberCounter_Prod`.
- Image and font files, which are out of scope for this analysis.

The page title in the saved HTML is `Taxo - Intelligent Healthcare`. Its metadata describes Taxo as an AI-powered platform for specialty clinics.

## Important technical limitation

This is a **published-site capture**, not the original editable Framer project. Much of the JavaScript is bundled, minified, or generated. The archive does not necessarily contain the original authoring components, design canvas, CMS data, or all source files in their original form.

Therefore:
- Inspect the HTML and JavaScript to identify observable structure and interaction patterns.
- Do not claim to have recovered the original source architecture exactly.
- Do not blindly copy the compiled runtime or generated bundles into the Dr. Ford project.
- Where implementation details cannot be reliably established from the archive, label them as inferred rather than confirmed.

## Observable page structure

The captured homepage includes these recognizable content areas:
1. Header/navigation
2. Hero with the headline “Intelligent healthcare” and supporting introduction
3. Product/solution introduction
4. Metrics/counter section, with labels including “Capacity unlocked”, “More patients seen”, and “Languages supported”
5. Frequently Asked Questions accordion
6. Security section
7. Footer

The HTML includes repeated responsive or variant renderings of some content, so repeated headings in the source should not automatically be interpreted as separate user-facing sections. Inspect layout wrappers, generated component boundaries, and breakpoint behavior before counting them.

The captured navigation includes links such as Solutions, Blog, Careers, Request Demo, and Login. Their presence in the HTML does not prove every destination page is included in the ZIP.

## Interactions and implementation patterns to investigate

Inspect the supplied source to identify evidence for:
- Responsive navigation and layout breakpoints
- Page-section/component boundaries
- Hero composition and entrance/reveal motion
- Scroll-triggered transitions
- Number counter behavior
- FAQ expand/collapse behavior
- Cursor-following effects, if active on this page
- Grid shimmer effects, if active on this page
- Layout-jump prevention techniques
- Smooth-scroll integration and how it coexists with native scrolling
- Reduced-motion behavior, if detectable
- Lazy loading and asset-loading behavior
- Accessibility and keyboard behavior, where detectable

Do not assume a module is used on the visible homepage just because it exists in the archive. Trace imports and references before concluding it is active.

## What to produce for Dr. Ford

Create an independent implementation plan with these outputs:

### A. Page architecture
Map the reference's visible sections and describe the purpose of each section, its likely component boundary, and its responsive behavior.

### B. Interaction inventory
For each identifiable interaction, record:
- Trigger
- Visual/functional result
- Whether evidence is directly visible in the source or inferred
- How to implement the same *kind* of behavior independently

### C. Reusable component plan
Propose clean React components for Dr. Ford, such as:
- `SiteHeader`
- `HeroSection`
- `SchoolIntroduction`
- `LearningPaths`
- `CourseOverview`
- `ImpactStats`
- `FoundersCarousel`
- `PartnerCarousel`
- `WhyDrFord`
- `FAQSection`
- `FinalCTA`
- `SiteFooter`

These are Dr. Ford components, not claims about Taxo's original component names.

### D. Clean implementation
Use the framework and dependencies actually available in the Google AI Studio project. Prefer small, understandable components over a copied or minified reference bundle. Add a dependency only when it serves a clear need.

### E. Evidence and uncertainty
Separate findings into:
- **Observed in archive**
- **Likely implementation pattern**
- **Unknown / requires browser inspection**

Do not invent implementation details that the saved files cannot establish.

## Dr. Ford-specific constraints

- Use Dr. Ford's own sitemap and content.
- Keep the Dr. Ford palette: `#080A09`, `#101411`, `#171B18`, `#F5F7F5`, `#A8AEA9`, `#B7FF00`.
- Do not use orange.
- Do not reuse Taxo's assets, typography, branding, wording, or exact page composition.
- Persian must use correct RTL layout; English must use LTR.
- Keep the design original and use the actual Dr. Ford logo only when supplied.
- Use verified course details, founders, partners, dates, and metrics only.
- Do not create dead buttons or pretend a form has been submitted without a real integration.

## Recommended workflow

1. Inspect the archive's HTML and trace its relevant CSS and JavaScript references.
2. Produce the architecture and interaction inventory before writing code.
3. Map useful patterns to Dr. Ford's own homepage and sitemap.
4. Implement one section at a time in clean React components.
5. Test responsive behavior, keyboard interactions, RTL/LTR, reduced motion, and performance.
6. Explain what was observed directly and what was inferred.
