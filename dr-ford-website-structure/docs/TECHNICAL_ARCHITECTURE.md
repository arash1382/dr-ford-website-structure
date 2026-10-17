# Technical Architecture

Use the React setup provided by Google AI Studio Build Mode. Inspect the generated project and its existing framework before changing dependencies.

Suggested conceptual separation:
- layout components: header, footer, navigation, page shell
- section components: homepage sections
- UI components: buttons, cards, accordions, carousels, form controls
- data: courses, events, founders, partners, FAQs, navigation
- routes/pages: route-level screens
- styles: global styles and design tokens
- utilities: helpers and integrations

Keep content data separate from visual components. Centralize translations and direction handling. Use direction-aware spacing and test icons, arrows, forms, and navigation in RTL and LTR.

Do not assume a database, email service, payment gateway, or CMS is connected. Identify integrations that need configuration. Never expose secrets or commit API tokens to GitHub.

Quality checks: no broken routes, dead links, console errors, mobile overflow, RTL/LTR bugs, inaccessible focus states, or false form-submission claims.
