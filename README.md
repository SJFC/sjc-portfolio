# Sarah-Jane Crowson — Portfolio Site

A bespoke static website documenting the practice of Sarah-Jane Crowson, practitioner-researcher and poet. Built as a postgraduate portfolio submission for the MDES 10 module at Sunderland University.

---

## About this site

This site was built as a deliberate artistic and academic object, not only as a container for work. The design system, scroll behaviours, and visual language were developed in parallel with — and in response to — the practice it documents. The site is intended to be *entered* rather than encountered: text-light, image-beautiful, with interactions that carry conceptual weight rather than merely organising content.

The three case studies documented here are:

- **Minor Deities: representations &c., under glass** — a magic lantern slideshow body of work shown at Hereford College of Arts, 2023
- **Botanica: A Data Humanist Question** — a living installation (in development, September 2025 launch)
- **Card Game** — in documentation

---

## Transparency statement: AI collaboration

This site was built in active collaboration with **Claude** (Anthropic), an AI assistant, across a series of working sessions. I want to be explicit about what that collaboration involved, because transparency about AI use is both an ethical obligation and, in the context of this practice, a subject the work itself addresses.

### What Claude contributed

- All HTML, CSS, and JavaScript was written by Claude, working from my direction
- The design system architecture (shared token file, reusable components, scroll-effect utilities) was proposed and built by Claude
- Placeholder draft text was written by Claude from my case study documents, as a starting point for my own editing
- Debugging — including diagnosing why `position: sticky` was failing due to `overflow: hidden` on an ancestor element — was carried out by Claude through analysis of screen recordings I provided

### What I contributed

- All conceptual and curatorial decisions: what to include, what to leave out, how to sequence it
- All final text on the site: I edited Claude's drafts directly in the code, or wrote from scratch, or provided copy through an editing document that Claude then placed into the markup
- All design direction: palette, typography, the palimpsest scroll effect concept, the image selection and sequencing, the decision to use a horizontal strip rather than vertical scroll for the closing image chapter, the moth's visual character and flight path
- All source images and artwork
- The poems, care-label captions, and poetic fragments throughout

### How we worked

We developed a shared working glossary (`GLOSSARY.md`) that maps the conceptual and poetic vocabulary of the practice to precise technical implementations — so that a word like "palimpsest" could carry both its theoretical meaning and its engineering meaning without collapsing either one. This glossary is included in the repository as a record of the collaborative method.

Design decisions were made iteratively: I directed by eye and feel, provided screen recordings when something wasn't working, and edited text directly in the markup rather than relaying changes back to Claude. Claude acted as a collaborative developer; I acted as director, poet, and editor.

### Why this matters to the practice

The question of what AI can and cannot generate is not incidental to this work — it is one of its central preoccupations. Five questions produced through the thinking behind *Minor Deities* were contributed to Humanity's Last Exam (Nature, vol. 649, 2026), a benchmark designed to test the limits of current AI. The use of AI as a collaborator in building this portfolio is therefore not a contradiction of the practice's concerns, but an extension of them: an attempt to work *with* AI tools honestly, at the boundary of what they can and cannot do, rather than either refusing them or deferring to them uncritically.

---

## Technical notes

Built with plain HTML, CSS, and vanilla JavaScript — no framework, no build step, no dependencies beyond Google Fonts. Deployed via GitHub Pages.

The design system lives in `assets/css/tokens.css`. All colour values, type scale, spacing, and reusable component styles are defined there and referenced across pages, so any design-system change propagates site-wide rather than needing to be made per page.

Browser support: all modern browsers. A `prefers-reduced-motion` fallback is implemented for all scroll-driven animations — users with this accessibility setting enabled see static versions of all animated elements.

---

