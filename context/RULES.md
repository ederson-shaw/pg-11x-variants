# RULES — terms, hard limits, and the checklist you are graded on

**STANDING RULE, not a one-time patch — applies to every round, every future correction,
forever:** lean heavily on the reference. When a content requirement and the reference's
real structure conflict, the reference wins — fold facts into its real sections, never
add a section the reference wouldn't have. And every delivery gets reviewed critically,
by someone other than the model that built it, before it is called done — a self-report
of "DONE" is not verification, a fresh look with fresh eyes is.

## THE TERMS (these words mean exactly this here, nothing else)

**RECLOTHE — CORRECTED 2026-08-14, read this even if you read the old version.** The
first version of this rule explicitly forbade copying the reference's brand colours, and
that instruction was wrong — it is why the first pass of this project came back reading
as generic AI redesigns instead of recognisable clones of their reference site. The
founder's own words: *"eles vão fazer exato mesmo site mas mudar todo produto para pitch
genius"* — the exact same site, with the product swapped. Not a reinterpretation.

What you are doing: you take the reference site — its actual palette, actual type
choices, actual grid, actual spacing, actual motion, actual density — and you rebuild
it, as faithfully as hand-written HTML/CSS allows, carrying PitchGenius's product and
message instead of theirs. **Structure 1:1. Visual identity 1:1 where it is not a legal
problem. Content and product 0:1.**

- **You copy, closely:** section sequence, layout geometry, spacing rhythm, scroll and
  hover behaviour, hero structure, the type scale, the actual colour palette (the real
  hex values, not "inspired by"), the actual font choices or the closest free
  equivalent, the way sections transition, the overall density and rhythm.
- **You never copy:** their words, their headline copy, their logo, their photographs,
  their illustrations, their icons, their company name, their customers, their specific
  claims/numbers, and obviously never their trademarks. Not one sentence. Not one image
  file. The PRODUCT and the PEOPLE shown are PitchGenius's, always — everything else
  about how the page *looks* should be recognisably theirs.
- **Test:** put your page next to theirs. A stranger should say *"that's the same site,
  different product"* — not "that's inspired by X" and not "these have nothing in
  common." If your palette is not close to their real palette, you did not do the job.

**SIGNATURE.** Only relevant AFTER fidelity is satisfied. If, working within the
reference's real palette and structure, one thing about how you carried the product over
is worth naming, name it in `RESULT.md`. It is not permission to add a colour, a font, or
a layout device the reference does not have. Do not manufacture one if there isn't one.

**THE MEDIAN.** Still worth refusing: a dark navy gradient + cyan glow + 3D orb + four
generic icon cards is the median for ANY AI-generated SaaS page regardless of reference.
But refusing the median is not license to refuse the reference's own real palette —
those are different things. If the reference itself happens to use navy+cyan, keep it;
that is fidelity, not the median.

**FRICTION.** Anything between the visitor and understanding what this is. Count it:
from page load to "I know what this does and who it's for" — how many scrolls? More
than one and a half is a failure.

**REAL DEFECT.** Something a person notices: a visual break, a layout that jumps, a
button that does nothing, a wait with nothing on screen, text over an image you can't
read, a page that is broken at 375px. Not "could be more semantic".

**PROOF.** A screenshot or a command with its output. "It looks good" is not proof.
"I opened it" is not proof. A PNG in `shots/` is proof.

## HARD LIMITS

1. **Static HTML only.** `index.html` + `styles.css` + `app.js`. No React, no Next, no
   build step, no npm install, no bundler, no Tailwind CDN, no framework of any kind.
   It must open by double-clicking the file. This is not negotiable — 16 of these have
   to be opened and compared side by side in one sitting.
2. **No CDN for anything that matters.** Fonts: use Google Fonts `<link>` (allowed) or
   system stacks. Everything else — icons, images, video — lives in your own folder.
   The page must still be readable with the network off.
3. **No invented facts.** See `PRODUCT.md`. No fake logos, no fake numbers, no fake
   quotes, no fake case studies, no fake integrations. Ever.
4. **English.** All page copy in English (US market). Your `RESULT.md` may be English.
5. **No comments in the code** except where a line's *why* cannot be read from the line.
6. **Responsive to 375px.** Not "mostly". Open it at 375 and look. A hero composed for
   1440 that collapses into garbage at 375 is a failed deliverable, no matter how good
   the desktop is.
7. **Real product surface, never a fake dashboard.** If you show the product, show the
   real one (`assets/product-ui-live-call.json`, or the real webp screenshots). A
   made-up chart with made-up numbers is the single laziest thing on the internet.
8. **prefers-reduced-motion respected.** One media query. Non-optional.
9. **Do not touch anything outside your own project folder.** No edits to
   `/home/eder/Documentos/chris-timofi/`. Read-only there.

## DESIGN RULES

**Typography carries the page.** Pick a display face and a body face deliberately and
say why in `RESULT.md`. Inter for everything is the default answer and the default
answer is a failure. A utility/mono face for data and labels is almost always right for
this product, because the product outputs numbers.

**Colour has a job or it is deleted.** Name 4-6 hexes, each with a job — but pull those
hexes from the REFERENCE SITE you were assigned, read from its real CSS in `./ref/`, not
invented. Your `PROMPT.md` names a "palette territory" written before this correction —
if it tells you to move away from the reference's own colours, prefer the reference's
real colours instead and say in `RESULT.md` that you overrode it, per RULES.md's
2026-08-14 correction. The live card itself has its own fixed rule regardless of your
page palette: see `assets/product-ui-live-card-v2.json` — cyan `#06b6d4`/`#22d3ee` there
belongs on the live signal and nowhere else, because that is the real product's own
colour, not a page design choice.

**Warmth vs precision is the whole design problem.** See `MESSAGE.md`. The human layer
should feel warm, irregular, made. The product layer should feel cold, exact, numeric.
Put them next to each other. That contrast IS the brand — do not resolve it into one
comfortable middle tone.

**Motion serves meaning.** The one animation that is always justified on this page: the
live card *changing* — the readiness number stepping, the SAY THIS line replacing
itself, the HumanCue observation updating. That is literally what the product does.
Animate that and you have demonstrated the product without a video. Animate a background
gradient and you have wasted the visitor's GPU.

**Every wait gets a state.** Nothing over 200ms may show a blank area. And a spinner is
not information — say what is loading.

**Structure encodes meaning.** Do not number sections `01 / 02 / 03` unless they are
genuinely a sequence. (Here, the before/during/after story genuinely is one — so if you
number, number that.)

**Spend boldness once.** One signature. Everything around it disciplined and quiet.

## FORBIDDEN, specifically

Words: revolutionary · seamless · leverage · supercharge · unlock · game-changing ·
cutting-edge · next-generation · empower · 10x · "the only AI that…" · "the world's
first" · "trusted by thousands".

Visuals: 3D glass orbs · abstract neural-network node graphs · purple-to-blue gradient
mesh backgrounds · glowing chatbot avatars · robot hands · handshake stock photos ·
generic smiling office stock · four line-icons in a row as the entire feature section ·
a fake analytics dashboard with invented charts · animated starfields.

Structures: a testimonial carousel with invented quotes · a customer logo wall we cannot
back · a pricing table with invented prices · a "Trusted by" strip with placeholder
brands · a blog/resources grid with fake article titles.

## THE CHECKLIST (you must run through this before you say DONE)

Copy this into `RESULT.md` and answer each line literally.

```
[ ] opens by double-clicking index.html, no server needed
[ ] no framework, no build step, no npm install
[ ] readable and correct at 375px, 768px, 1280px, 1920px  (state which you actually opened)
[ ] every fact on the page traces to PRODUCT.md — list any claim you were unsure about
[ ] zero invented logos / numbers / quotes / customers
[ ] the message reads as humans + AI, without needing the headline to say it
[ ] a person appears on the page, and it is not stock-generic
[ ] something hand-made appears (texture, ink, paint, sketch) OR you state why not
[ ] the real product surface appears with the real numbers from PRODUCT.md
[ ] both buyers are served: the rep's unfair advantage AND the manager's arithmetic
[ ] one named SIGNATURE, stated in one sentence
[ ] the median named, and what you did instead
[ ] prefers-reduced-motion handled
[ ] keyboard focus visible on every interactive element
[ ] no console errors  (paste the console output)
[ ] screenshots in shots/ at 1440 and 375, full page
[ ] you named at least one thing still wrong with your own page
```

A checklist item you cannot honestly tick is the page telling you it is not finished.
Write `BLOCKED:` and the reason instead of ticking it. A caveat next to a tick is a lie.
