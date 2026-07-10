# BRAND.md — Sarah-Jane Crowson, portfolio design system

*A companion to `GLOSSARY.md` and `tokens.css`. The glossary maps poetic vocabulary to code; this document records the identity decisions and their reasons, so that any future page — or any future collaborator, human or otherwise — inherits the system rather than re-deciding it. Written at the close of the drawer-stage edit, July 2026.*

---

## 1. The identity in one breath

**Byline:** Poet · artist · practitioner-researcher — always in this order, always with interpuncts. Data humanism is the field; the byline names the person. "Human-centred" is rejected vocabulary: it is the field's beige carpet, and this practice plants a flag instead.

**The bio sentence:** *I design poetic, participatory ways for organisations to communicate complex information, listen to the lives ghosted by data, and make representation more accessible, situated and humane.* — "ghosted by data" is load-bearing: the contemporary sense (dropped, unanswered) and the spectral sense (still present as trace) are both meant. It threads to "ghostly velum" in the found sapphics and to the site's palimpsest grammar.

**The claim:** classification without changed conditions is containment, not care. Every case study asks this of a different material — the photograph, the plant, the spreadsheet. The claim appears in each page's closing register and, as of the drawer edit, on the front door.

**The position the language must protect:** data is not a synonym for truth. Any future positioning copy that promises to "uncover truths" in data contradicts the practice and is rejected on sight.

---

## 2. Voice and the synonym system

Two registers coexist deliberately, and the tension between them *is* the brand:

- **The poetic register** — Cormorant italic, first person, image-led. Captions, standfirsts, plant conditions, closing reflections.
- **The institutional register** — Inter, uppercase, letterspaced, exact. Eyebrows, stat grids, credits, metadata. Deliberately the coolest thing on any page; one beat among warmer ones.

**The synonym standfirsts.** Each case study opens with a standfirst in the family *"X is not a synonym for Y"*:

| Page | Standfirst |
|---|---|
| Minor Deities | To be preserved is not a synonym for free. |
| Botanica | Is categorisation a synonym for containment? |
| Regulated Instruments | Data is not a synonym for truth. |

Two assertions and one question — the question belongs to Botanica because Botanica is the work still alive. The set repeats on the index doors: the door quotes the standfirst, the arriving page keeps the promise. Samphire's caption ("Resilience is not a synonym for ease") carries the motif into the work itself. **Rule for future case studies:** a new page earns a new synonym line, or it does not join the set.

**Prose conventions.** Flowing prose over bullets in all visible copy. British spelling. Rhetorical figures are permitted and documented (e.g. the anadiplosis closing the About disclosure: "…unintended containment. Containment in specific environments…"). Poems are quoted exactly and never edited in passing; dashes and spacing inside poems are the poet's domain.

---

## 3. Type system

| Token | Face | Role and rationale |
|---|---|---|
| `--font-display` | Cormorant Garamond (EB Garamond, Georgia fallback) | Display and the poetic voice: titles, standfirsts, captions, poems, closing reflections. Weight 500 for headings, italic for everything spoken rather than stated. |
| `--font-body` | EB Garamond (Georgia fallback) | Body prose at `--text-base` (1.125rem), line-height 1.65. The reading voice. |
| `--font-sans` | Inter (system fallback) | The institutional voice: eyebrows, stat numbers and labels, nav, credits, form chrome. Always small (`--text-xs`/`--text-sm`), always letterspaced (0.08–0.15em), usually uppercase. Inter never appears at display size — the institution does not get the biggest voice on any page. |

**Scale:** 0.8 / 0.95 / 1.125 / 1.4 / 1.9 / 2.8 / 4 / 5.5rem (`--text-xs` → `--text-3xl`). Page titles clamp responsively around `--text-2xl`; the scale is shared so no page re-invents hierarchy.

**Measures:** body prose at `--measure` (38rem); wide compositions at `--measure-wide` (56rem). Prose never runs wider than the measure even inside wide sections.

---

## 4. Colour

### The landing / botanical register (cream ground)

| Token | Hex | Territory |
|---|---|---|
| `--cream` | `#F5EFE4` | The daylight ground: statement, About, text sections, response card paper. |
| `--navy` | `#1C2B3A` | Primary text on cream; the consultation page's dark ground; send-button ground. |
| `--magenta` | `#7B1750` | **The site-wide accent, drawn from the sewing-box silk lining.** Default eyebrow colour, links on cream, argument numerals, Botanica's title. The single thread that runs through every register. |
| `--mauve-pink` | `#C4A0A8` | Botanica's soft voice: specimen captions, door subtitle, scroll cues on aubergine. |
| `--sage` | `#8A9A7E` | The consultation page's cool voice: eyebrows and poetic text on navy. |
| `--olive` | `#6B7654` | Section headings and standfirsts on cream; links in the consultation evidence. |
| `--warm-grey` | `#9B8E82` | The quiet voice everywhere: captions, credits, metadata, muted labels. |

### The nocturnal register (Minor Deities)

| Token | Hex | Territory |
|---|---|---|
| `--near-black` | `#15110E` | The lantern page's ground, the index opening, the 404. Warm-toned, never pure black. |
| `--deep-warm-grey` | `#2A211A` | Image-sequence grounds — deliberately not black, *so slides glow as in projection*. |
| `--slide-gold` | `#C99A4B` | Eyebrows and caption titles on dark grounds; site-wide focus-outline colour. |
| `--slide-amber` | `#E8B978` | Warmer highlights: sapphic extracts, plant names, dark-ground eyebrows; default text-palimpsest colour. |

### The aubergine register (Botanica)

| Value | Source | Territory |
|---|---|---|
| `#2A1020` | Drawn from the silk lining | Botanica's dark ground and index door — set locally, deliberately *not* a shared token, so the box's interior stays the box's own. |
| `--mauve-pink`, `--slide-amber` | Shared tokens | Botanica's soft and warm voices on the aubergine ground. |
| `--magenta` | Shared accent | At home here more than anywhere: this register is where the accent colour comes *from*. |

### The regulated register (Regulated Instruments)

Cooler and more structured than the other two — sage, olive and navy on cream — because this is the page where the institution is present in the room. Its register is assembled entirely from shared tokens plus one local tint, which is itself a statement: the consultation works *inside* the shared system rather than departing from it.

| Value | Source | Territory |
|---|---|---|
| `--navy` | Shared token, promoted to ground | The erasure chapters and found-sapphics grid sit on navy — the institutional colour made to hold poems. |
| `--sage`, `--olive` | Shared tokens | The page's voices: sage for eyebrows and poetic text on navy, olive for headings and links on cream. |
| `#EDE6D6` | Local tinted cream | The method section's ground (shared with About's tinted sections) — cream with the temperature slightly dropped. |
| `--warm-grey` | Shared token | The stat grid: the coolest, most exact beat on the page, deliberately so. |

### Grounds, stitched

Each case study sets `--page-ground` / `--page-ink` locally; shared components read those variables rather than hard-coding a register. The **thread silk** `#A63A5E` with shadow `#14100C` — the running-stitch colours — is currently dormant by decision (the stitch returns as material, via the Singer, in a future Botanica iteration); the variable stays live because the response card and stitch-rule borrow it.

**The registers in one line:** Minor Deities is nocturnal near-black with gold; Botanica is aubergine with mauve and amber; Regulated Instruments is sage, olive and navy on cream; the person (About) is cream in daylight. Magenta stitches all four together.

---

## 5. The opening grammar

Every case study opens identically: **eyebrow → h1 → standfirst**, still and centred, *orientation before motion*. Motion begins only after the reader knows where they are.

- **Eyebrow:** the named practice, in the institutional voice. The set — *critical spatial practice / critical data visualisation / participatory consultations* — is a deliberate sequence: critique of the image, critique of the dataset, then critique handed to other people. Each names a citable field (Rendell; the data-humanism literature; the co-design tradition), so the three eyebrows double as a literature map.
- **h1:** title, colon, italic subtitle in `em`. A superseded title may be demoted to subtitle rather than erased (*Regulated Instruments: revealing layers*) — the palimpsest applied to naming itself.
- **Standfirst:** the synonym line (§2).

Eyebrows are sentence case throughout ("Future work", not "Future Work"). Recurring motif-eyebrows within a page (e.g. "Revealing layers" on the consultation page) share one capitalisation.

---

## 6. Structural conventions

**Glass closes every case study.** Each closing section belongs to the glass thread, as a variation, never a repetition: Minor Deities ends *under* glass, Botanica ends with worlds *in* glass, Regulated Instruments ends with glass *removed* (eyebrow: "Glass, removed" over an empty-handed, direct closing). A fourth case study must find a fourth relationship to glass.

**Motion is an argument, used once.** The scroll-driven vocabulary (see `GLOSSARY.md`) — projection overlay, text palimpsest, materialising, accretion — each states the palimpsest claim kinetically. **Discipline: at most one image effect and one text palimpsest per page.** The first use teaches the mechanic; repetition demotes argument to wallpaper. All effects collapse gracefully under `prefers-reduced-motion`: static image, resolved line, resting moth — reduced motion is a full experience, not a degraded one.

**The machine-readable layer is the tag cloud's exile.** Visible skills tags and classification chrome are rejected — the site does not import the logic it critiques. Keywords live in JSON-LD and meta descriptions, "addressed to their actual readers." Every page carries a meta description.

**The 404 is a residual space.** The moth lives there; the page nobody is meant to find is styled as the lantern register's forgotten corner. Infrastructure is allowed to be part of the work.

---

## 7. Image treatment

- **Mounted artefacts** (`.slide-figure--mounted`): `--radius-slide` (4px), deep soft shadow — the object as kept thing.
- **Projection images** (`.slide-figure--projection`): no radius — light, not object.
- **Figures on cream** (About portrait, Botanica argument figures): small radius (3–4px), lighter shadow; captions centred, Cormorant italic, one line.
- **The portrait rule:** the person appears small and situated — beside the paragraph about where the practice comes from, never as masthead. The photograph is evidence of register, not decoration.
- **Alt text is part of the work:** written as description in the site's own voice, faithful to the object (including fragmented erasure words where the panel fragments them). Decorative duplicates carry `alt=""` + `aria-hidden`.
- Grids reserve `.ml-grid` (specimen-board, 4→2→1 columns); horizontal scroll-snap (`.bo-plants__track`) is Botanica's own.

---

## 8. Spacing, layout, access

Spacing runs the token ladder 0.5 → 12rem (`--space-1`–`--space-7`); sections breathe at `--space-5`/`--space-6`. The nav is fixed, `mix-blend-mode: difference`, so one nav survives every register. Focus states are visible everywhere, in `--slide-gold`. `overflow-x: hidden` lives on `body` only — never on ancestors of sticky elements (hard-won: it silently kills `position: sticky`).

---

## 9. Governance

- Decisions are made deliberately and documented with rationale — in this file, `GLOSSARY.md`, and the session logs — never accumulated through silent iteration.
- Effects and colours are judged **by eye on the live page**, not accepted on description.
- A new case study must arrive with: a named practice for its eyebrow, a synonym standfirst, its own ground register that magenta can stitch to the rest, a glass closing that extends the set, and at most one motion argument.
- Superseded elements are retired with a written reason and, where they have a future (the thread, the moth), a stated destination.

*Last updated: July 2026, at the close of the drawer-stage edit.*
