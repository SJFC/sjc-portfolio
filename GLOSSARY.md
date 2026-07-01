# Working Glossary

*A shared language between Sarah-Jane Crowson and Claude (Anthropic) for directing the build of this portfolio site. Living document — grows as we name new things.*

This exists because design language and engineering language pull in different directions. A word like "palimpsest" is doing real conceptual work in the practice — it can't be retired just because it's ambiguous as a build instruction. So the method here isn't to flatten the poetic vocabulary into technical vocabulary, but to give each poetic term a precise technical anchor underneath it, so when one of us says the word, both of us know exactly which code it points to.

Each entry: **the word we'll say** → what it means in plain terms → where it actually lives in the code, so either of us can find and adjust it without a long description.

---

## Effects and mechanisms

**Token / tokens**
A named, reusable design value — a colour, a size, a spacing amount — defined once and referenced everywhere, instead of being retyped by hand each time it's needed.
→ `assets/css/tokens.css`, the `:root { --variable-name: value; }` block at the top of the file.

**The Palimpsest**
The two-layer scroll effect: a fixed-size, low-opacity copy of an image sits still and unmoving (the *ghost layer*) while a second, identical copy moves and changes in front of it — starting oversized and out of focus, then shrinking and sharpening as the reader scrolls, until it comes to rest at the same size as the ghost beneath it. Two images of the same picture, one still, one becoming.
→ The `.proj-block` component: `.proj-base-img` (the still ghost) + `.proj-sticky__img` (the moving foreground), both inside `.proj-runway` / `.proj-sticky`.

**Ghost layer** *(image sense)*
The fixed, low-opacity, unmoving copy of an image that sits behind the moving layer in a Palimpsest. Distinct from —
→ `.proj-base-img`

**Ghost text / the fossil layer** *(typographic sense)*
A separate but related idea: a line of your own earlier poetry, set pale and oversized, running behind a whole section as texture rather than as a Palimpsest's paired image. Same instinct (something underneath persisting), different mechanism — text, not image; whole-section, not single-block.
→ `.ml-ghost-text`

**Scroll runway**
The tall, otherwise-empty container that creates the distance over which a scroll-driven effect plays out. Taller runway = more scroll distance = a slower, more deliberate transition.
→ `.proj-runway` (currently `300vh`)

**Pin / pinned**
An element held fixed in the centre of the viewport while the page keeps scrolling past it, until its runway runs out and it releases back into normal flow. Built with `position: sticky`.
→ `.proj-sticky`

**Coming into focus**
The blur-to-sharp transition that runs alongside the shrink, inside a Palimpsest. Controlled by one number (`MAX_BLUR`) in the script at the bottom of each case study page.

**Dwell**
The portion of a runway's scroll distance reserved for the image to sit fully resolved — sharp, settled, not moving — before it releases. Without dwell, an image reaches clarity for a single instant and is gone; with it, there's a real pause to actually look.
→ The `DWELL` constant in the page's `<script>` block (currently `0.35`, i.e. the final 35% of the runway is held still and sharp)

**Settling / landing**
The moment a pinned image releases and continues scrolling at normal speed, now sitting at its final size — which we set to deliberately match the size of a plain static image elsewhere on the page, so a settled Palimpsest and a static slide read as the same kind of object.

**Fixed image / static image**
A plain image with no scroll-driven motion at all — what Deity of Keys and Invocation and Alchemy were turned back into. The "default" state; a Palimpsest is something added on top of this, not the only way an image can appear.
→ `.slide-figure`, `.slide-figure--mounted`, `.slide-figure--projection`

**The strip / specimen strip**
The horizontal row of evenly sized, evenly aligned images — what the closing five-image section became once we removed the stagger. Distinct from a scattered or staggered layout; the word "strip" specifically implies uniformity, like a contact sheet or a row of slide mounts.
→ `.ml-grid`

**The moth**
The single creature that flies once across a section, triggered the moment that section scrolls into view, and never repeats. Built from two layered motions: a slow drifting flight path, and a faster, independent wing-flap.
→ `#ml-moth`, `.is-flying`, the `moth-drift` and `wing-flap-left` / `wing-flap-right` keyframes

**Reveal**
The simple fade-up-as-you-scroll-to-it effect used for ordinary text and content — much plainer than a Palimpsest, just an opacity and position fade, no pinning, no runway.
→ `.reveal` / `.is-visible`, driven by the `IntersectionObserver` near the bottom of the script

**Eased / easing**
A transition that speeds up and slows down rather than moving at a constant rate — used so the focus-pull in a Palimpsest feels weighted rather than mechanical.
→ The `eased` calculation inside `updateProjections()`

---

## Diagnostic phrases

Plain-English symptoms, and what they tend to actually mean — useful shorthand for troubleshooting without re-describing the whole problem each time.

**"It disappears before it resolves, regardless of scroll speed"**
Almost certainly *not* a timing problem — this is the signature symptom of a broken pin. Usually means something between the moving element and the page itself has `overflow: hidden` set on it, which silently stops `position: sticky` from working at all. (This is exactly what happened with `.ml-sequence` — worth remembering as a CSS gotcha, since it's easy to reintroduce by accident when adding a new section that needs `overflow: hidden` for an unrelated reason.)

**"It doesn't coalesce"**
The image reaches clarity but only for an instant — needs *dwell* added or increased.

**"It vanishes into the background"**
A contrast problem, not a motion problem — usually a dark-toned image losing definition against a dark section background once blurred. Fixed by strengthening the ghost layer's opacity or adding a faint glow behind the pinned area, not by changing the motion itself.

---

## Open vocabulary

Terms we've used once but haven't fully pinned down yet — worth firming up next time they come up:

- *"Aligned" vs "staggered"* — we now have one of each (the strip is aligned, the original specimen-board idea was staggered) but haven't named the staggered version, in case we want it again elsewhere.
- *Section rhythm* — the pattern of alternating image-only / text-only / text-and-image sections across a single case study page. Useful term, not yet attached to any specific code (it's a structural decision made in the HTML, not a reusable component).
