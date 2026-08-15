# pg-11x-variants

Three independent, high-quality explorations of ONE direction — the "11x.ai" reclothe
(`12-11x-frontier` in the `pg-landing-lab` repo) — not a return to the 16-competitor lab.
Separate repo, separate folder, per explicit instruction, because the previous round mixed
concerns (one page, patched repeatedly, in place) and the result read as low-effort.

## Objective

Land on a single landing page for PitchGenius.AI that a stranger would call the best version
of the 11x.ai-style direction — sharp, serious, human — not a generic SaaS template and not
an AI-generated stock-photo composite. Three variants exist to compare real alternatives
side by side, not to produce three mediocre options and average them.

## What's here

- `context/` — the governing docs. Read all of them before writing a line of code.
  `MESSAGE.md` (brand voice/tone), `PRODUCT.md` (real data, do not invent numbers/names),
  `RULES.md` (static HTML/CSS/JS only, no build step), `MEETING-REQUIREMENTS.md` and
  `MEETING-PER-DESIGN-TAKEAWAYS.md` (what was said in the actual client call, with
  timestamps — this is not optional reading).
- `reference/assets/hero-mockup-reference.png` — the approved hero layout target.
- `reference/assets/hero-people-band.png` — the approved people-band photo asset, flagged
  this session as reading like an AI composite (identical lighting/scale/expression across
  all 8 people, one visible artifact on the glasses-wearing figure's ear). Each variant must
  make its own call on this: use it as-is, source/generate a genuine alternative, or drop the
  concept — and say which, and why, in that variant's own notes.
- `context/buyer-blueprint-palette.json` / `buyer-readiness-palette.json` — **NOT for this
  landing page.** These recolor the real product app (a separate codebase). Do not apply them
  here. If a variant needs to depict these product surfaces, match the real product's actual
  current look, not an invented palette.
- `variant-a/`, `variant-b/`, `variant-c/` — one self-contained `site/` per variant.

## Quality bar — checked by a hostile reviewer, not self-graded

Every item below caused a real, confirmed defect in the prior round. This list exists because
of those, not as theory.

1. **No self-sabotaging copy.** Never write "we don't have X yet" or "a number we can't
   prove" as a headline. If PRODUCT.md forbids a claim, argue from mechanism/logic instead of
   confessing the absence. Read every headline as a buyer would, not as a checklist-compliance
   pass.
2. **One color system per page.** Every card-like surface (live call card, any recreated
   product UI, CTAs) shares one palette family. A light pastel card next to a dark card on the
   same page is a defect, not a style choice — confirmed this session.
3. **Satoshi on every heading**, not just the hero. Check `getComputedStyle` on h1–h5 and any
   pull-quote — a silent fallback to the body font is invisible until you check computationally.
4. **Pixel-measure against `hero-mockup-reference.png`**, don't eyeball it. Left margins,
   vertical rhythm, and text-align bugs from a leftover rule are exactly the kind of thing that
   looks fine at a glance and wrong on inspection.
5. **No generic B2B template sections.** A 4-cell feature grid with roman-numeral eyebrows and
   hairline borders on white is what every competitor already has. If a section could be
   copy-pasted onto a random SaaS site unchanged, it's not done.
6. **Page height matches content density.** A 7-screen-tall page with sections that are mostly
   padding is a defect, not "editorial breathing room." Justify every screen of scroll.
7. **The "cards stack on scroll" interaction is a requested feature**, not decoration —
   before/during/after (or equivalent) should read as a real scrollytelling moment, not three
   flat rows. Build it, don't fake it with a static repeat of the same card shape.
8. **Real product data only** — PRODUCT.md's two coherent moments (Russell Pontone /
   Judd Barakove) are the only source of live-call numbers. No invented archetypes, no
   Gerald-style placeholders left in as if final.
9. **Zero console errors, real screenshots, at 375/768/1440/1920px** — a codex/agent sandbox
   that can't launch a browser must say so explicitly and stay BLOCKED on visual proof; the
   human operator verifies with a real screenshot before anything is called done.

## Process — mandatory, not optional

Every variant, and every fix inside a variant, goes through a hostile subagent review before
being reported as done. The reviewer is told explicitly not to invent problems that don't
exist — but if it finds real ones, the variant stays open. Two consecutive clean hostile
rounds = passes. One round with a finding = fix it, review again. This is a standing policy
for this whole effort, not a one-time step.

## Non-goals

- Not rebuilding the other 15 reference directions. This is 11x only.
- Not touching the real product codebase (`pitch-genius`) from here — that work happens in
  that repo directly, tracked separately.
