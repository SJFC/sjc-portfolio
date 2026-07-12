# Sarah-Jane Crowson — Portfolio Site

A bespoke static website documenting the practice of Sarah-Jane Crowson, poet, artist and practitioner-researcher. Built as a postgraduate portfolio submission for the MDES 10 module at the University of Sunderland.

Live at: https://sjfc.github.io/sjc-portfolio/

---

## About this site

This site was built as a deliberate artistic and academic object, not only as a container for work. The design system, scroll behaviours, and visual language were developed in parallel with — and in response to — the practice it documents. The site is intended to be *entered* rather than encountered: text-light, image-beautiful, with interactions that carry conceptual weight rather than merely organising content.

The three case studies documented here make one connected argument — that classification without changed conditions is containment, not care — asked of three different materials: the photograph, the plant, and the spreadsheet.

- **Minor Deities: representations &c., under glass** — a magic lantern slideshow body of work shown in Hereford, 2023 (*critical spatial practice*)
- **Botanica: a data humanist question** — a living installation, launching at h.Art, Hereford, September 2026 (*critical data visualisation*)
- **Regulated Instruments: revealing layers** — a participatory consultation methodology applied to a regulated Access and Participation Plan (*participatory consultations*)

---

## Transparency statement: AI collaboration

This site was built through active collaboration with two AI assistants at different stages: **Claude** (Anthropic) during the original design and build, and **Codex** (OpenAI) during a later accessibility, editorial-structure and visual-rhythm review. I want to be explicit about what those collaborations involved, because transparency about AI use is both an ethical obligation and, in the context of this practice, a subject the work itself addresses. This approach was disclosed to the course tutor at the outset of the project.

### What Claude contributed

- The original HTML, CSS, and JavaScript build was written by Claude, working from my direction
- The design system architecture (shared token file, reusable components, scroll-effect utilities) was proposed and built by Claude
- Placeholder draft text was written by Claude from my case study documents, as a starting point for my own editing
- Debugging — including diagnosing why `position: sticky` was failing due to `overflow: hidden` on an ancestor element — was carried out by Claude through analysis of screen recordings I provided
- In the later editorial stage, Claude performed "cold reads" of the site against its intended audiences (examiner, supervisor, prospective clients), produced snag lists, and carried agreed fixes into complete page files for me to review and commit

### What Codex contributed

- Audited the homepage, About page, participation page and all case studies for accessible heading structure, then implemented a single visible `h1` per page, consistent `h2` sections and properly nested `h3` subsections while retaining the existing visual design
- Distinguished structural headings from eyebrows, poetic labels, captions and navigation text, and checked the resulting page outlines without CSS
- Reordered the *Revealing Layers* project framing and question, and introduced concise method signposts across all three case studies to make the long-form arguments easier to scan
- Proposed and implemented a photo-essay rhythm: breaking up the initial image run in *Minor Deities*, restoring the aligned collage-to-photograph dissolve in *Botanica*, incorporating earlier botanical studies as clearly labelled visual research, and presenting the plant images more compactly as a discovered series
- Helped curate and implement the “Selected published work” section on the About page, using work and selections I supplied
- Refined the landing-page orientation, project-card hierarchy and mirror interaction; simplified the response form; and integrated my spreadsheet-to-wildflower thank-you animation so that it begins only after a confirmed submission
- Added a small number of bridge sentences, headings, captions and interface labels for clarity; I reviewed and approved these in conversation before or during implementation
- Performed responsive and reduced-motion checks, verified image loading and heading counts, preserved the existing Formspree workflow, and prepared optimised web copies of newly added images without altering my source files

### What I contributed

- All conceptual and curatorial decisions: what to include, what to leave out, how to sequence it
- Final editorial authority over all text: I edited AI drafts directly, wrote from scratch, supplied copy through editing documents, and accepted, revised or rejected later wording suggestions
- All design direction and final decisions: palette, typography, interaction concepts, image selection, sequencing and the decision about which recommendations to implement
- All source images and artwork
- The poems, care-label captions, and poetic fragments throughout
- All titles, and the editorial decisions of the later "drawer stage": renaming, re-sequencing, and the reading-across-pages that surfaced the site's connective systems

### How we worked

We developed a shared working glossary (`GLOSSARY.md`) that maps the conceptual and poetic vocabulary of the practice to precise technical implementations — so that a word like "palimpsest" could carry both its theoretical meaning and its engineering meaning without collapsing either one. Design decisions and their rationale are recorded in `BRAND.md` and in working logs, rather than accumulated through silent iteration.

The method was iterative in both directions. I directed by eye and feel, judged every effect on the live page rather than on description, provided screen recordings and screenshots when something was not working, edited text directly in the markup, and — over the course of the project — re-learned how to work in HTML myself, making small changes directly in the GitHub editor.

The collaboration also had distinct phases. Claude helped establish the site's architecture, interaction grammar and original implementation, then acted as a cold reader during the drawer-stage edit. In the later Codex pass, I supplied the complete current repository and additional artworks, animations and screenshots. Codex first inspected the existing patterns, proposed small and larger options, and implemented only the choices I approved. We repeatedly reviewed downloadable builds, adjusted wording and visual rhythm, and tested the result at desktop and mobile sizes. The AI systems acted as collaborative developers and critical readers; I remained the director, artist, poet, curator and final editor.

### Why this matters to the practice

The question of what AI can and cannot generate is not incidental to this work — it is one of its central preoccupations. Five questions produced through the thinking behind *Minor Deities* were contributed to Humanity's Last Exam (Nature, vol. 649, 2026), a benchmark designed to test the limits of current AI. The use of AI as a collaborator in building this portfolio is therefore not a contradiction of the practice's concerns, but an extension of them: an attempt to work *with* AI tools honestly, at the boundary of what they can and cannot do, rather than either refusing them or deferring to them uncritically.

---

## Repository map

- `index.html` — landing page: the mirror, the statement, three doors
- `about.html` — the person, in daylight; contact
- `404.html` — a residual space (served automatically by GitHub Pages for any missing address)
- `case-studies/` — the three case study pages and the Botanica participation page
- `assets/css/tokens.css` — the shared design system: colour, type scale, spacing, reusable components
- `assets/images/` — photography and collage, organised per page
- `assets/mirror-gift.html` — self-contained animated thank-you, loaded only after a successful mirror response
- `GLOSSARY.md` — the shared vocabulary: poetic terms mapped to their technical implementations
- `BRAND.md` — the identity decisions and their reasons: registers, grammar, conventions, governance
- Working logs and page-edit documents, where committed, record session-by-session decisions

---

## Technical notes

Built with plain HTML, CSS, and vanilla JavaScript — no framework, no build step, no dependencies beyond Google Fonts. Deployed via GitHub Pages.

The design system lives in `assets/css/tokens.css`. All colour values, type scale, spacing, and reusable component styles are defined there and referenced across pages, so any design-system change propagates site-wide rather than needing to be made per page. Each case study sets its own colour register locally on top of the shared tokens (see `BRAND.md`).

The landing-page mirror and the Botanica participation page post responses via Formspree. Each page carries a meta description; the landing page carries the site's machine-readable layer (Open Graph and JSON-LD structured data). On any future migration from GitHub Pages, the four absolute URLs noted in the `index.html` head comment are the only lines that change.

Browser support: all modern browsers. A `prefers-reduced-motion` fallback is implemented for all scroll-driven animations — users with this setting enabled see static, fully resolved versions of every animated element, as a complete experience rather than a degraded one.

---

## The site, in its own words

> *To be preserved is not a synonym for free.* — Minor Deities

> *Is categorisation a synonym for containment?* — Botanica

> *Data is not a synonym for truth.* — Regulated Instruments

> *Three connected projects asking what representation preserves, what it leaves out, and how people and living systems might speak back.*
