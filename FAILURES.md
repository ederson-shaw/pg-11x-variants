# PitchGenius website failure log

This file is the anti-regression record for the next rebuild. It is intentionally blunt: these were process and design failures, not merely cosmetic preferences.

## Retired build: Variant M

Variant M is retired as a design base. Its commit remains in Git history for reference, but new work must start from Variant C. Do not copy M overrides, layout patches, or its hero composition into Variant N.

### What went wrong

1. **The hero thesis drifted without respecting the selected source.** M silently switched from L's CRM-versus-buyer question (`Your CRM knows the deal. But does it know the buyer?`) to C/B's buyer-signal thesis (`Your buyer is telling you more than they're saying.`). N's explicit rule is now: C supplies the visual system; L supplies the copy and voice; the PDF removes prohibited certainty and validates product facts. The L hero is restored.
2. **The wrong base was selected.** M was assembled from B and then populated with L/PDF content. That imported B's proportions and chrome instead of preserving C's editorial structure. The result looked like a hybrid rather than a deliberate system.
3. **Whitespace was treated as a missing panel.** Extra boards, rails, and feature bands were appended to sections to fill empty areas. This created duplicate explanations, longer pages, and generic dashboard-looking filler instead of fixing composition, scale, and hierarchy.
4. **The product surface was invented.** HumanCue received generic window chrome, fake metadata, and inconsistent proportions instead of one faithful HTML mockup based on the real desktop app. A screenshot or decorative card is not proof of a product.
5. **Forbidden certainty returned.** Copy implied mind reading, told the rep what the buyer was feeling, and presented an exact sentence as an answer. The PDF requires evidence, probabilistic language, and the seller as decision-maker.
6. **The platform order drifted.** `See Reality` and `Improve` were reversed in places. The canonical order is Understand → Prepare → Perceive → Measure → See Reality → Improve, followed by the learning loop.
7. **Visual QA was too shallow.** No-overflow, loaded-font, and no-console checks were mistaken for quality. They did not catch dead space, weak alignment, wrong type scale, pale borders, tiny product copy, or the hero proof gap.
8. **Responsive fixes were patches, not compositions.** `display: contents`, breakpoint-specific offsets, and clipped UI were used to force a desktop design into mobile/tablet. The hero image/proof relationship broke, and controls became unreadable.
9. **Motion was decorative or disabled.** Repeated reveal fades were used everywhere, then global overrides disabled the meaningful motion. Motion must explain one change in evidence, not decorate every section.
10. **Interactive states were not treated as design.** Learn-more/chevron states, HumanCue Next/Dismiss/End behavior, and menu semantics were patched late. Every state needs a visible, tested result at all widths.
11. **The deployed page was not the source of truth.** Local screenshots and public screenshots were not compared section-by-section before claiming completion. A build is not done until the public URL is tested after propagation.
12. **Quality claims came too early.** We reported a polished result while the hero, product mockup, typography, and section rhythm still had obvious defects. N must earn each claim through evidence.

## Variant N gates

- Start from `variant-c/site`, not M, B, or L overrides.
- Freeze the 16-section content map before styling. Each section gets one comprehension objective and one primary proof surface.
- Use the PDF as the product truth and L's CRM/buyer thesis as the messaging source. No invented feature names, UI chrome, metrics, certainty, or claims.
- Hero acceptance requires the approved headline, a single governed container/gutter, deliberate image crop, no bottom shelf/gap, no overlay panel covering the portrait, and readable type at 1440/1024/768/390/320.
- Keep the salesperson as the actor; AI is a guide. HumanCue language must be evidence-based and match the source-of-truth card.
- No duplicated feature bands. If a section needs more density, enlarge the real proof surface or improve the copy/layout; do not append a second generic board.
- Minimum readable type is 12px for secondary labels and 15px for meaningful product/body copy on mobile; labels may be smaller only when genuinely metadata.
- Use one intentional motion system plus reduced-motion behavior. Every animation must communicate a state change.
- Capture every section at desktop, tablet, and mobile in pairs; inspect the actual pixels for gaps, collisions, weak contrast, stretched assets, and broken icons before moving on.
- Run local and public QA: 0 horizontal overflow, 0 failed requests, 0 hidden critical content, 0 broken icons, valid focus/menu/disclosure states, and exact deployed-content verification.

### N defects found and closed during final pass

- HumanCue's question rows briefly inherited a three-column desktop grid on 320px, reducing the answer column to a narrow word-stack. The narrow breakpoint now keeps the timeline marker but gives each label and explanation a full readable measure.
- The HumanCue header lost `CHALLENGER` and truncated `Russell Pontone` on the smallest phone. The panel now widens within the governed gutter and preserves both pieces of source-of-truth identity without document overflow.
- A 768px tablet viewport was still using the desktop navigation and wrapped every label into a second row. Tablet now switches to the keyboard-tested compact menu before the desktop nav can break.
- The footer logo was allowed to diverge from the header mark. It now uses the same bounded SVG mark and canonical `PitchGenius.AI` wordmark; no baked raster logo or oversized `brand__mark` remains.
- HumanCue inherited a generic green status dot, glyph-based chevron, and plain `End` label. The final card now uses the supplied app's cyan ring, CSS chevron, listening bars, and square End affordance; the state line is explicitly single-line and clipped, never word-wrapped.
- The alignment screen drifted from L's CRM-versus-buyer example. Its source now keeps L's `Stage 4`, `Proposal delivered`, `Trust weakening`, and `Willingness declining` wording while retaining the PDF-safe evidence framing.
- HumanCue's context disclosure had no explicit open-state semantics. It now updates `aria-expanded`, `aria-label`, the hidden detail region, and the visual chevron together; ending a call preserves the square icon while changing the label and state.
- The transition had been carrying C's short slogan while the N content map was meant to inherit L's seller-timing explanation. The second line now uses the full L sentence with its own readable measure and the same clipped line-reveal, so it cannot collapse into a one-word stack.
