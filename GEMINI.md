# PhD Proposal Presentation Project

## Project Overview
This project is an interactive, web-based presentation for a PhD Thesis Proposal titled **"Intent Prediction from Physiological Signals"**. It explores reframing physiological noise as privileged context via asymmetric learning architectures.

## Technical Architecture
- **Framework:** Astro (Static Site Generator) for the main portfolio/projects site.
- **Presentation:** Served as a self-contained static HTML file in `public/presentation/index.html` to ensure reliable asset paths and bypass complex framework processing.
- **Styling:** Vanilla CSS + Tailwind CSS (via CDN in the static presentation).
- **Interactivity:**
    - Real-time BCI Signal Sandbox (Canvas-based simulation).
    - Dynamic Dark Mode / High Contrast theme.
    - Deep-linking support for individual slides (`#slide-N`).
- **Mathematics:** KaTeX for high-performance LaTeX rendering.
- **Integration:** Deep-linking to the source `Ph_D__Thesis_Proposal_in_Informatics.pdf` with automated page offsets (+2).

## Key Milestones Achieved
1.  **Framework Migration:** Moved presentation from `.astro` components to a static `.html` asset to fix pathing and deployment issues.
2.  **Responsive Scaling:** Implemented global typography and layout scaling for "cinematic" viewing on large PC screens.
3.  **Visual Language:** Added SVG-animated processing pipelines to illustrate methodological differences.
4.  **Academic Rigor:** Integrated real academic citations (Codina et al., von Lühmann et al.) with clickable DOI links.
5.  **PDF Synchronization:** Implemented a "Document Roadmap" and footer links that jump to specific pages in the source PhD proposal document.

## Presenting Instructions
- Local URL: `http://localhost:4321/about_me/presentation/index.html`
- Controls:
    - `Next/Prev` buttons or Arrow keys for navigation.
    - `Dark Mode` toggle for high-contrast viewing.
    - `Sandbox` mode for live hardware simulations.
