# Reference design token and behavior extraction

Source inspected: the downloaded 11x.ai reference bundle in `./ref/`, including `index.raw.html`, `RENDERED.html`, `computed-styles.json`, the authored CSS/JS bundles, local media, and `INVENTORY.txt`.

This is an extraction of the reference implementation. It records visual and interaction rules useful for a static HTML/CSS reclothe; it is not a request to copy the reference’s product claims or page copy.

## 1. Source and implementation notes

- The reference is a Webflow-exported page for `11x.ai`.
- The captured page is static HTML plus authored CSS/JS and Webflow/vendor runtime code. There is no application framework in the page itself.
- The effective body stack is `ES Allianz, Arial, sans-serif`.
- The reference loads ES Allianz as local WOFF2 files in the CSS bundle. It uses regular, medium, light, and bold weights.
- The inline font-smoothing rule is `-webkit-font-smoothing: antialiased`.
- The fluid rem-scaling block is commented out in the HTML. Treat `1rem` as `16px` at the captured desktop size.
- The hero and several later sections use local or captured video/image assets. The local inventory contains hero MP4/WebM, Julian MP4/WebM, carousel/background videos, product screenshots, people images, logos, and footer/astronaut imagery.
- The source has Webflow-generated class names and duplicate responsive rules. Prefer the normalized tokens and computed values below over individual generated selector names.

## 2. Color system

### Core semantic colors

| Role | Token / source value | Hex / value |
| --- | --- | --- |
| Primary background | `--background-color--background-primary` | `white` |
| Primary text | `--text-color--text-primary` | `black` |
| Primary links | `--link-color--link-primary` | `black` |
| Alternate text | `--text-color--text-alternate` | `white` |
| Primary border | `--border-color--border-primary` | `black` |
| Secondary background | `--background-color--background-secondary` | `#f9f9f9` |
| Tertiary background | `--background-color--background-tertiary` | `#eaeaea` |
| Secondary text / muted gray | `--text-color--text-secondary` | `#929394` |
| Dark teal product background | `.section_product` | `#0b252a` |
| Deep teal brand token | `--base-color-brand--teal-800` | `#071b20` |
| Teal | `--base-color-brand--teal-600` | `#1e4b57` |
| Teal 700 | `--base-color-brand--teal-700` | `#10323b` |
| Warm workforce background | `.section_workforce-carousel` / brown 100 | `#d7cecc` |
| Warm beige 100 | `--base-color-brand--beige-100` | `#ede2d7` |
| Pale beige | `--base-color-brand--beige-150` | `#f5ece6` |
| Beige 200 | `--base-color-brand--beige-200` | `#e7d3bf` |
| Beige 300 | `--base-color-brand--beige-300` | `#d2b596` |
| Beige 400 | `--base-color-brand--beige-400` | `#cca57c` |
| Beige 500 | `--base-color-brand--beige-500` | `#c49867` |
| Beige 600 | `--base-color-brand--beige-600` | `#be905c` |
| Beige 700 | `--base-color-brand--beige-700` | `#af8251` |
| Beige 800 | `--base-color-brand--beige-800` | `#8c663c` |
| Dark brown | `--base-color-brand--beige-900` | `#4f3416` |
| Brown 100 | `--base-color-brand--brown-100` | `#d7cecc` |
| Brown 200 | `--base-color-brand--brown-200` | `#af9f9c` |
| Brown 400 | `--base-color-brand--brown-400` | `#95827d` |
| Brown 500 | `--base-color-brand--brown-500` | `#806965` |
| Brown 600 | `--base-color-brand--brown-600` | `#75635e` |
| Brown 700 | `--base-color-brand--brown-700` | `#6c5751` |
| Brown 800 | `--base-color-brand--brown-800` | `#4c312b` |
| Light blue | `--base-color-brand--blue-100` | `#d9dee5` |
| Blue 200 | `--base-color-brand--blue-200` | `#c5d5e8` |
| Blue 300 | `--base-color-brand--blue-300` | `#b2cbec` |
| Blue 400 | `--base-color-brand--blue-400` | `#8eaed6` |
| Blue 500 | `--base-color-brand--blue-500` | `#6386b2` |
| Blue 600 | `--base-color-brand--blue-600` | `#567aa6` |
| Blue 700 | `--base-color-brand--blue-700` | `#3c597e` |
| Blue 800 | `--base-color-brand--blue-800` | `#092245` |
| Light purple | `--base-color-brand--purple-200` | `#e4d6ff` |
| Purple 300 | `--base-color-brand--purple-300` | `#d9c5ff` |
| Purple 400 | `--base-color-brand--purple-400` | `#c6a7fe` |
| Purple 500 | `--base-color-brand--purple-500` | `#9f7be1` |
| Purple 600 | `--base-color-brand--purple-600` | `#6745a4` |
| Purple 700 | `--base-color-brand--purple-700` | `#371d68` |
| Purple 800 | `--base-color-brand--purple-800` | `#1b0a39` |
| Neutral light | `--base-color-neutral--lighter` | `#f6f5f5` |
| Neutral gray | `--base-color-neutral--neutral` | `#dcdcdf` |
| Neutral dark | `--base-color-neutral--dark` | `#c4c4c4` |
| Neutral darkest | `--base-color-neutral--darkest` | `#252525` |
| Error | system token | `#ce3a42` |
| Error bright | system token | `#ff5e41` |
| Success | system token | `#027a48` |
| Success light | system token | `#ecfdf3` |

Other authored palette values present in the CSS include `#b3cfd7`, `#5b8a97`, `#3b707e`, `#e5e5e5`, `#e2c9b6`, `#d7c5c1`, `#ae9a95`, `#f7f7f7`, `#f8f9f7`, and `#bac4c5`. They are used for secondary blue/teal, neutral, card, status, and tag treatments.

### Section-level color treatments

- Hero: dark video with a full-bleed black overlay at approximately `rgba(0,0,0,.5)` (`#00000080`), white type, and a transparent fixed navbar.
- Workforce carousel: flat warm gray-brown `#d7cecc`.
- Product block: flat dark teal `#0b252a`, white heading, low-opacity tag rows, and a light product-card surface.
- Pinned Julian section: black/white image-led treatment with a white rounded content card.
- Results: vertical gradient from approximately `#f8f9f7` to `#d7cecc`.
- Footer: warm brown/background image treatment with a white CTA card above it.
- Product tag pill: brown text `#4c312b` on `#d7cecc`, radius `9999px`, padding `.5rem 1rem`, weight 500.
- Light-blue tag pill: black at roughly 50% opacity on `#bac4c5`, radius `9999px`, padding `.5rem 1rem`, weight 400.
- Tag wrapper: translucent white on dark teal (`#f3f4f61a`), radius `.5rem`, padding `.5rem 1rem`, gap `.5rem`.
- Hero/header overlay: `linear-gradient(#00000080, #00000080)` over the media.
- Marquee edge fade in the dark product/tag area: `linear-gradient(90deg, #0b252a, #0b252a00 15% 58%, #0b252a00 85%, #0b252a)`; it has `pointer-events:none`.

## 3. Typography

### Font files and family

The authored CSS declares these ES Allianz faces with `font-display: swap`:

- Regular, weight `400`: `ESAllianz-Regular` WOFF2.
- Medium, weight `500`: `esallianz-medium-webfont` WOFF2.
- Light, weight `300`: `ESAllianz-Light` WOFF2.
- Bold, weight `700`: `ESAllianz-Bold` WOFF2.

Use the family as `ES Allianz, Arial, sans-serif`. The reference’s visual identity depends strongly on this humanist display/body face; do not replace it with a generic system font when a close reclothe can self-host it.

### Base scale and computed desktop values

The CSS uses rem values, with a 16px root in the captured page. The following are the main authored scales; computed values at the 1440px screenshot are included where useful.

| Style | Authored size / line-height | Weight | Tracking | Computed desktop note |
| --- | --- | --- | --- | --- |
| Hero display | `6.5rem`, `1` | 500 | `-.03em` | `120px / 120px` at 1440 due to the `min-width:1440` `7.5rem` override |
| Generic H1 | `5.5rem`, `1` | 500 | — | use sparingly; hero uses display style |
| H2 | `4rem`, `1` | 500 | `-.04em` in computed heading | common desktop section heading `64px / 64px` |
| H3 | `3.5rem`, `1.1` | 500 | — | product/result display variants are often `56px / 56px` |
| H4 | `2rem`, `1.2` | 500 | — | — |
| H5 | `1.5rem` | 500 | — | — |
| H6 | `1.25rem` | 500 | — | — |
| Hero display mobile | `2.625rem`, `1` | 500 | `-.03em` | remains large and compact on narrow screens |
| Medium body | `1.125rem`, `1.4` | 400 | — | — |
| Body | `1rem`, `1.4` | 400 | — | computed `16px / 22.4px` |
| Small body | `.875rem`, `1.4` | 400 | — | — |
| Tiny | `.75rem`, `1.4` | 400 | — | — |
| Header regular | `1.5rem`, `1.2` | 400 | `-.03em` | mobile becomes `1rem / 2` |
| Big number | `5rem` | 500 | `-.03em` | fluid result variant is `4.5cqw`; computed example `46.08px` |

Important computed values from `computed-styles.json`:

- Hero heading: `120px`, line-height `120px`, weight 500, letter-spacing `-3.6px`, white.
- “Meet our digital workers”: `64px / 64px`, weight 500, letter-spacing `-2.56px`, black.
- Alice/Julian card title: `32px / 38.4px`, weight 500, letter-spacing `-.64px`.
- “Digital workers transform your workforce”: `64px / 64px`, weight 500, letter-spacing `-2.56px`.
- Dark product heading: `56px / 56px`, weight 500, letter-spacing `-2.24px`, white.
- Product-card, pinned-section, and results display headings: generally `56px / 56px`, weight 500, letter-spacing `-2.24px`.
- Big results numbers: approximately `46.08px`, same line-height, weight 500, letter-spacing `-1.8432px`.

The reference favors short, tight display lines with negative tracking rather than oversized paragraphs. Body copy stays at 16px with generous section whitespace.

## 4. Geometry, containers, and spacing rhythm

### Global geometry

- Horizontal page gutter: `5vw` through `.padding-global` and related wrappers.
- Large container max-width: `90rem` (`1440px`).
- Medium container max-width: `64rem` (`1024px`).
- Other content caps include roughly `56rem` for wide content and `40rem` for copy blocks.
- Main horizontal grids commonly use `1rem` or `2rem` gaps.
- Global small spacing token: `1vw`.
- The reference uses large open sections rather than a dense app-shell rhythm.

### Vertical spacing tokens

| Utility | Desktop | At `max-width:991px` | At `max-width:767px` |
| --- | ---: | ---: | ---: |
| Small section padding | `2rem` | — | `2rem` |
| Medium section padding | `5rem` | `4rem` | `3rem` |
| Large section padding | `8rem` | `6rem` | `4rem` |
| XX-small gap | `.5rem` | — | — |
| X-small gap | `1rem` | — | — |
| Small gap | `1.5rem` | — | — |
| Medium gap | `2rem` | — | — |
| XX-large gap | `5rem` | — | — |

Common local rhythms:

- Digital-worker cards: `2rem` internal gap and a two-column landing row on desktop.
- Workforce carousel: large section padding; slide right padding `2rem`, reduced to `1.5rem` on mobile.
- Product tags: `.5rem` vertical/horizontal internal padding and `.5rem` inter-item gap.
- Product tabs: outer padding `1rem`; link padding `1rem 1.5rem 1rem 0`; menu gap `1rem`.
- Partner logos: `4rem` gap on desktop, centered/stacked on mobile.
- Results/user-case grid: `1rem` gap.
- Hero proof row: approximately `.5rem` column gap and `1.5rem` row gap when it wraps.
- CTA content: `3rem` padding desktop, `1.5rem` on mobile.

### Radius and controls

- Design-system large radius: `1.5rem`.
- Regular content/card radius: `1rem`.
- Medium radius: `0` in the base token; image panels and larger content surfaces opt into `1rem` or `1.5rem`.
- Pills/buttons: `999px` or `9999px`.
- Digital-worker card outer border is a light neutral and its base medium-radius card can be square; portrait media has a `1rem` radius.
- Buttons: 1px black border, black background, white text, `.75rem 1.5rem` padding, `1.2` line-height, pill radius.
- Small buttons: `.5rem` padding and `.25rem` gap.

## 5. Section order and composition

The captured homepage’s visual order is:

1. **Fixed navigation stack.** A black announcement strip sits above a transparent/fixed navbar over the hero. Desktop navigation contains Products, Platform, Solutions, Company, and the brand/CTA areas.
2. **Full-viewport video hero.** The hero is a minimum `100vh`, with the hero video covering the section, a black 50% overlay, centered white content, a large display heading, a proof row, a dark rounded/live-demo style CTA, and a case-study/marquee line inside the hero.
3. **Digital workers.** White section with the heading “Meet our digital workers.” The actual landing row contains exactly two portrait/video cards: Alice / AI SDR and Julian / AI Phone Agent. Each combines a tall media panel and text/meta copy.
4. **Workforce carousel.** Warm `#d7cecc` section with the heading “Digital workers transform your workforce” and a manually controlled slider of five content slides. It has a clipped horizontal mask, slide cards/media, arrows/dots, and generous bottom padding.
5. **Product block.** Dark teal `#0b252a` section headed “Amplify Intelligence, Accelerate Growth.” It includes pill/tag rows or marquees, a light product screenshot/tabs surface, the four product tabs Identify, Research, Personalize, Engage, and a “Partnered with” logo row.
6. **Pinned Julian / listen section.** A `200vh` wrapper creates a full viewport sticky image scene. A white rounded card overlays the lower content area with “Listen to Julian,” explanatory copy, an audio button/waveform, and a demo CTA.
7. **Results.** Gradient section from near-white to warm brown with a results heading/impact treatment and a four-column desktop user-case/stat grid. Cards mix stats, testimonials, and brand marks. Some card classes are prepared for a front/back flip.
8. **Footer CTA and footer.** A white rounded CTA card overlaps the footer section, followed by warm brown/image footer content with columns, locations, legal, social, and compliance links.

The page’s density is intentionally episodic: immersive dark video → spacious white people cards → warm editorial carousel → dark product proof → high-contrast pinned image break → gradient evidence grid → warm CTA/footer.

## 6. Responsive breakpoints

The authored Webflow styles use the following practical breakpoints:

### Desktop / wide

- Base styles are desktop-first.
- At `min-width:1440px`, the hero display override is `7.5rem` (the captured 1440 screenshot computes to `120px`).
- At `min-width:1920px`, the hero display override is `9.5rem`.
- The large container cap remains `90rem`.

### `max-width:991px`

- Navbar collapses from the desktop grid to a compact mobile/tablet arrangement and becomes a white responsive surface.
- Hero/general H1 reduces to about `3.25rem`; H2 to `2.75rem`; H3 to `2.25rem`.
- Large/medium section padding becomes `6rem / 4rem`.
- Workforce carousel mask becomes `50%`.
- User-case layouts move toward two columns.
- Product tabs switch from a horizontal desktop panel to a stacked/tablet arrangement.
- Product and proof grids simplify to one-column structures where needed.
- Hero video is intentionally deferred on mobile/tablet by the JS loader.

### `max-width:767px`

- Global heading scale is approximately H1 `2.5rem`, H2 `2.25rem`, H3 `2rem`, H4 `1.5rem`, H5 `1.5rem`, H6 `1.125rem`.
- Medium body becomes `1rem`; heading H2 remains `2.25rem`.
- Section padding becomes small `2rem`, medium `3rem`, large `4rem`.
- Digital-worker cards become one column and use `1.5rem` gaps.
- Workforce mask becomes `80%`; slide padding becomes `1.5rem`.
- Product tabs wrap/stack; user-case grid remains two columns until the phone breakpoint.
- Reveal animation stops line splitting at this breakpoint; mobile elements animate as whole blocks.
- Header content and hero display reduce; regular header style becomes `1rem / 2`.

### `max-width:479px`

- User-case grid becomes one column.
- Workforce mask becomes roughly `95%`.
- Global outlined container gutters can reduce to `1rem`.
- Mobile navbar min-height is `4rem` with `5%` horizontal padding.
- Hero extra top padding reaches `8rem`; hero display remains approximately `2.625rem`.
- Mobile CTA/footer overlap uses a larger negative-margin adjustment (about `-3rem`).

## 7. Interaction and motion behavior

### Hero and media loading

- The hero `<video>` is `autoplay loop muted playsinline`, covering the hero.
- A mobile media script detects `max-width:991px`, removes/defer-loads hero video sources, shows the poster, then restores sources and calls `play()` after load/idle or a roughly 1200ms timeout. This prevents heavy video from blocking the first mobile render.
- Other `.w-background-video video` elements lazy-load through `IntersectionObserver` with a `300px 0px` root margin. Sources move from `data-src` to `src`, then `load()` and `play()` are called. The hero is excluded from this generic observer.

### Scroll reveal

The active inline script initializes a one-shot IntersectionObserver reveal system rather than the older commented GSAP ScrollTrigger version.

- Selectors include `[data-text-reveal]` and `[slide-fade]`.
- Default stagger step by `data-reveal-order` is `.175s`.
- Heading duration `.5s`; text duration `.4s`; slide duration `.35s`.
- Heading stagger `.17s`; text stagger `.12s`.
- Initial vertical offsets are approximately `2rem` for headings, `1.25rem` for text, and `1rem` for slide elements.
- Easings are `power3.out` for headings and `power2.out` for text/slides.
- Text observer root margin is `0 0 -15% 0`; slide observer root margin is `0 0 -10% 0`; threshold is `.01`.
- Each target reveals once and is then unobserved.
- On desktop, SplitType-like line splitting wraps each line in a `.reveal-line-mask` with hidden overflow, `.15em` bottom padding, and `-.15em` bottom margin.
- At or below 767px, line splitting is disabled and the whole element fades/slides as one unit.
- The script runs settle passes around 1200ms and 3000ms to force visible/above-fold elements complete. It waits up to about five seconds for GSAP and one second for fonts; a fallback makes elements visible if dependencies fail.

### Marquee and hover cards

- Marquee rows use a flex track with `width:max-content` and a `30s linear infinite` horizontal animation from `translateX(0)` to `translateX(-50%)`.
- The DOMContentLoaded script duplicates the track contents to create the loop and inserts four fake cards into the real set. Treat those inserted cards as decorative placeholders, not product facts.
- Hovering a marquee line pauses the animation.
- Marquee case cards start at `max-height:0`, `overflow:hidden`, and `pointer-events:none`; a hovered trigger expands its following card to `max-height:500px` over `1.25s` with `cubic-bezier(.2,1,.3,1)`.
- The inner hover card scales from `.5` to `1` over `1.5s` with the same easing family.
- `[data-hover-swap]` elements transition opacity in `.35s`; from/to states cross-scale between `1` and `0`.
- A dark marquee edge gradient masks the start/end of the tag rows.

### Audio waveform

- Audio wires are beige `#d2b596`, `4px` wide, roughly `50%` of the waveform panel height, with `2px` left/right margins and rounded ends.
- `@keyframes animateUpDown` varies wire height from about 30% to 90%; the animation is paused until audio plays.
- JS assigns random initial delays from `[50,150,300,450,600]ms` and random initial heights from `[33,20,17,44,50,66,70,88,100]%`.
- Play behavior pauses other audio, toggles the current play/pause icon, and resets the wire animation/icon on `ended`.

### Navbar and navigation

- The navbar is fixed with `z-index:99`, full width, and top inset 0. Desktop min-height is `4.5rem`; phone min-height is `4rem`.
- Desktop container max-width is `90rem`, with a three-column grid approximately `.375fr 1fr .375fr` and a `1rem` gap.
- Dropdowns use Webflow hover interactions with roughly 200ms delay. Navigation links soften to about 70% opacity over `.2s` on hover.
- Mobile menu is a full-height (`100dvh`) panel with a roughly `.5s` height transition. Accordion rows use borders, padding, and `.2s cubic-bezier(.165,.84,.44,1)` background/height transitions.
- A small inline `pulse` keyframe scales/changes opacity over 3s infinite; three instances are staggered at 0/1000/2000ms for status-dot style indicators.

### Sliders and tabs

- Announcement/top-bar slider: autoplay, infinite, `4000ms` delay, `outin` animation, `500ms` duration, arrows hidden.
- Workforce slider: `500ms` slide animation, manual rather than autoplay, infinite false, navigation dots, and source-configured arrows. The captured inline script can activate a matching dot and initially triggers a third slider item.
- Product tabs: current tab is tracked with `data-current`; desktop in/out durations are `300ms / 100ms`. Active links gain a black top border and full opacity; inactive links sit at roughly 50% opacity. Tablet/mobile copies are stacked or wrapped versions of the same content.

### Pinned image section

- The listen-to-Julian scene is primarily CSS-driven: outer section height `200vh`, inner content `position:sticky`, `top:0`, height `100vh`, with a full-cover image and an absolutely positioned lower content wrapper.
- The overlay card is white, rounded `1.5rem`, and padded `3rem` desktop / `1.5rem` mobile.

## 8. Flip-card readiness

The CSS contains a reusable user-case flip setup:

- `.user-cases_product.is-flipping` communicates click/hover affordance with `cursor:pointer`.
- Front/back faces use `backface-visibility:hidden`.
- The back face is rotated around the Y axis by `-180deg`.
- The front/back wrappers are positioned for a 3D reveal, with the card’s transform/transition handled by the generated interaction layer.

The current landing DOM also includes `.is-front-new` testimonial variants. The captured inline authored JS does not contain a simple standalone flip handler, so the behavior is likely Webflow interaction/runtime-driven. For a static reclothe, a small class toggle can reproduce the same front/back reveal without changing the surrounding results-grid layout.

## 9. Component-specific notes for a close reclothe

- Preserve the fixed nav/announcement overlay relationship: the nav is part of the hero composition, not a separate tall block above it.
- Preserve the hero’s strong media layer and black overlay; white hero typography is intended to sit on dark, moving imagery.
- Keep display copy short enough to form compact blocks. The reference uses very large type with tight line-height and negative tracking, then returns to 16px body copy.
- The two digital-worker cards are editorial portrait cards, not a dense feature grid. Use tall `47:65` media proportions and rounded image panels.
- The workforce section is a warm, low-contrast editorial carousel. Its mask and generous blank space are as important as the slide content.
- The product section is the main dark proof surface. Tags are not standalone UI chips; they form horizontal movement and atmospheric edge-faded rows behind/around the tabs card.
- The light product card and partner logos provide the contrast reset after the dark product background.
- The pinned image section is a pacing break. It should remain visually simple: one image, one white card, one audio interaction.
- Results cards can mix testimonials and quantitative/statistical blocks, but keep the outer grid consistent and use the existing flip-ready affordance only where a second side is meaningful.
- The CTA card intentionally overlaps the footer with a negative bottom margin. Keep that overlap rather than flattening it into normal flow.
- The footer background image is full-bleed and object-positioned around `50% 80%`; foreground footer content needs a readable contrast treatment.
- Do not carry over Webflow/vendor noise such as icon fonts, analytics, voice-widget runtime, or remote video URLs when a static local equivalent is sufficient.
- For a close static implementation, reproduce the layout rhythm, responsive hierarchy, color contrast, and motion timing first; treat captured copy, claims, logos, and customer facts as separate content decisions governed by the project brief.

## 10. Minimal token starter set

```css
:root {
  --ref-white: #fff;
  --ref-black: #000;
  --ref-off-white: #f9f9f9;
  --ref-neutral-light: #f6f5f5;
  --ref-neutral-dark: #929394;
  --ref-teal-deep: #0b252a;
  --ref-teal-800: #071b20;
  --ref-teal-600: #1e4b57;
  --ref-beige-100: #ede2d7;
  --ref-beige-200: #e7d3bf;
  --ref-beige-300: #d2b596;
  --ref-brown-100: #d7cecc;
  --ref-brown-800: #4c312b;
  --ref-results-start: #f8f9f7;
  --ref-radius-card: 1.5rem;
  --ref-radius-media: 1rem;
  --ref-radius-pill: 999px;
  --ref-gutter: 5vw;
  --ref-container: 90rem;
  --ref-body-size: 1rem;
  --ref-display-size: 7.5rem;
  --ref-section-large: 8rem;
  --ref-section-medium: 5rem;
  --ref-section-small: 2rem;
  --ref-font: "ES Allianz", Arial, sans-serif;
}
```

