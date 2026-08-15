# PRODUCT — the only facts you may put on the page

Everything below is real. Nothing below is aspirational. If you want to say something
that is not in this file, you may not say it. Inventing a feature, a customer, a
percentage or an integration is the one unrecoverable failure in this project.

## What it is

PitchGenius.AI — a real-time sales co-pilot. It listens to a live sales call and, while
the call is still happening, tells the rep what the buyer is feeling and the exact
sentence to say next.

It ships as a **desktop app** (a small always-on-top card floating over whatever video
call the rep is already in — Zoom, Meet, Teams). Not a Chrome extension. Not a
post-call report tool.

Domain: pitchgenius.ai — Staging: stage.pitchgenius.ai

## The three moments

### 1. Before the call — Buyer Blueprint
A profile of the person you are about to talk to, built before you dial.
- **Archetype** — e.g. "Strategic Visionary"
- **Personality read** — DISC-based, shown as e.g. `DOCI | D | S3 | C60`
- **Decision pattern** — e.g. "Fast • results-focused"
- **Social style** — e.g. "Driver"
- **Trust Triggers™** — the 3 things that make this specific person trust you
- **Resistance Signals™** — the 2-3 things that make this specific person shut down
- **Likely objection** — stated as a sentence, not a category

### 2. During the call — the live card

**⚠ THE REAL SCREEN CHANGED ON 2026-08-13. Read `../../assets/product-ui-live-card-v2.json`
in full before recreating this screen — it is read directly from the shipping app's
source code, not a screenshot, and it is CANONICAL. Do not use a gauge, signal bars,
stage tabs, a trust-trigger grid, or MEDDPICC chips on this screen — the founder cut
all of them after a cited usability study (SUS 82.1 → 72.5 with a richer interface),
and re-adding them contradicts the product's own stated design philosophy.**

The product's centre of gravity. ONE minimal card, plus a thin wave strip and a
plain-text stage row above it. The card shows exactly three labelled blocks:
- **NEXT BEST MOVE** — one instruction, e.g. *"Clarify the display behavior"*
- **SAY THIS** (or **SAY NOTHING**) — the literal sentence to say, in curly cyan
  quotes, e.g. *"The display scales to fit the screen. What are you seeing on your
  screen?"*
- **WHY NOW** — one flowing line, signal → reason, e.g. *"reading the room → this is
  the moment it costs him something"*

Plus, in the 44px header only (never a visual gauge): **HumanCue™** — a tiny live-state
word or sentence (e.g. "Listening", or a held/writing/failed state) — and, only when a
real reading exists, **"Readiness N · STAGE"** as small text (never a dial, never shown
as 0). A collapsed detail toggle reveals Trust / Willingness / Reached as plain text —
not a chart. Buttons: outline `Next`, plain-text `Dismiss`, and a `Why this, now?` link.

**Buyer Readiness Index™, Trust Triggers™, Resistance Signals™** are still real product
concepts — they just do not render visually on THIS screen anymore. They belong to the
pre-call Buyer Blueprint (unchanged, see below) and to the collapsed detail panel as
plain numbers, not a dashboard.

### 3. After the call — post-call analysis
- Evidence-linked call summary (every claim points at the moment it came from)
- Buyer Readiness Index™ with a written verdict
- **MEDDPICC gap analysis** — the 8 chips: Metrics, Economic Buyer, Decision Criteria,
  Decision Process, Paper Process, Identify Pain, Champion, Competition — each scored
  strong / neutral / weak
- Next Best Move recommendations for the following call
- `Update CRM →` action

### Cross-cutting — Rep Calibration
10 questions the rep answers once, privately, that tune how the co-pilot talks to them.
Example question: *"I am comfortable making stride decisions before I have all the
information."* on a 1-5 strongly-disagree-to-strongly-agree scale.

**The privacy promise is a product fact and it must appear on the page:** the rep's
calibration answers are private. Managers see usage and deal activity. They do not see
the rep's answers.

## Trademarked names — spell them exactly

`HumanCue™` · `Buyer Readiness Index™` · `Trust Triggers™` · `Resistance Signals™` ·
`Neuro-Script Live™` · `Pre-Call Buyer Intelligence™` · Buyer Blueprint

## Real numbers from one real call (use these, do not invent others)

These all come from one coherent moment. If you show a live-call card anywhere on the
page, use this data. Two different readiness numbers on one page is a bug.

```
contact         Russell Pontone
archetype       CHALLENGER
stage           DISCOVERY
readiness       45 / 100
humancue        buyer is still describing the screen display
next best move  Clarify the display behavior
say this        "The display scales to fit the screen. What are you seeing on your screen?"
why now         reading the room → this is the moment it costs him something
```

Second coherent moment, from the approved comp — use this one OR the one above, never
halves of both. **The `signals` line below is data, not a layout instruction — do NOT
render it as a bar chart or gauge on the live card.** That visual (comp-A's gauge + 4
bars) is exactly what the founder cut on 2026-08-13 — see `product-ui-live-card-v2.json`.
If you want to show these numbers visually, they belong in the live card's collapsed
detail panel (plain text, Trust/Willingness/Reached only) or on the post-call screen,
which is unchanged.

```
contact         Judd Barakove  (RevSymphony)
archetype       CHALLENGER
stage           VALUE
readiness       25 / 100
signals         In no hurry · Trust 45 · Urgency 20 · Pain scale 60 · Willingness to move 30
next best move  Buyer has no champion pushing this internally.
say this        "Before we get into the mechanics, Judd — who on your team is actually
                pushing for a change to how you handle these calls, and what are they
                hoping to see happen differently?"
post-call       MEDDPICC 65% · acceptance High
```

## Who competes and what they actually do

| who | what they do | what they do not do |
|---|---|---|
| Gong | records calls, transcribes, coaches after the fact, revenue intelligence | say anything during the call |
| Clari / Clari Copilot | forecasting, revenue ops, call recording | live in-conversation coaching |
| Chorus (ZoomInfo) | call recording + analytics | live in-conversation coaching |
| Salesforce / HubSpot | store what already happened | tell you what to do next |

Checked: none of them claim live psychological reading during the conversation. That is
the wedge. State it as a fact about the category, never as an insult to a competitor.

## What we do NOT have (do not imply otherwise)

- No customer logos. The comps show ramp / Vanta / Census / Clari / miro / Neo4j —
  those are **placeholders from a mockup**, not customers. Do not put them on a page.
- No published win-rate, ramp-time or revenue numbers. No case studies. No testimonials.
- No G2 rating, no SOC2 badge, no "trusted by 500 teams".
- No public pricing.
- No integration logo wall.

If a section of your reference site is a customer logo wall or a testimonial carousel,
you must **replace that section with something we can actually back**, not fill it with
invented names. Suggested honest replacements, pick one and say which:
- a "how it works in one call" strip using the real numbers above
- the category comparison table (what conversation intelligence does vs what this does)
- the privacy/trust statement for reps
- a founder statement, one paragraph, signed

## Calls to action

Primary: **Book a pilot** (this is the real motion — pilots, not self-serve signup)
Secondary: **See the live call** / **See how it works** — opens the product demo

Do not write "Start free trial", "Sign up free" or "Get started in 30 seconds". There
is no self-serve product.

## Existing real assets you can use

- Real product screenshots (webp):
  `/home/eder/Documentos/chris-timofi/pitchgenius-landing2/reference/`
  → `buyer-blueprint.webp`, `post-call-analysis.webp`, `rep-calibration.webp` — still
    accurate, those screens did not change.
  **⚠ `live-copilot.webp` is STALE (captured 2026-08-08) and shows the OLD live-call UI
  — do not use it anywhere on the page.** The live-call screen was redesigned
  2026-08-13; see `assets/product-ui-live-card-v2.json`. Recreate that screen in real
  HTML/CSS instead of embedding this image. This exact mistake cost multiple projects
  several correction rounds because CSS fixes to a component do nothing when the
  rendered pixels are actually a static `<img>` of the old screen — grep your own
  `site/index.html` for `live-copilot.webp` and remove every hit.
- Logos: `/home/eder/Documentos/chris-timofi/pitchgenius-landing2/public/brand/`
  → `logo-black.png`, `logo-white.png`, `mark.png`, `hero-photo.jpg`
- Generated brand imagery (people, textures): `pg-landing-lab/shared/assets/`
  See `shared/assets/MANIFEST.md` for what each file is.
