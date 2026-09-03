# EBELA OBELA — Research-backed website plan

**Status:** Approved for implementation · implemented against this plan on 2026-09-03.

## 1. Evidence baseline

The site represents **EBELA OBELA** at **1/29 Brahmapur Shivmandir Road, Tagore Garden, Brahmapur, Kolkata, West Bengal 700096**. The current Google business listing reports **4.1/5 from 496 reviews**, phone **+91 98311 68763**, and hours of **11:00–23:00 Monday** and **10:00–23:00 Tuesday–Sunday**. Zomato currently reports **4.0 from 62.5K delivery ratings**, and identifies current top dishes including **Katla Kalia, Basanti Polau, Gondhoraj Chicken, Egg Thali, and Mutton Thali**.

The business's owner-controlled Facebook identity uses the line **“ওপারের স্বাদ এপারে”** and describes the restaurant as a destination for Bangal / Bengali-Bangladeshi food. Third-party editorial history also supports a home-style Bengali food identity and delivery-first positioning.

### Facts used in production copy

- Business name: EBELA OBELA
- Naktala/Brahmapur address above
- Phone: +91 98311 68763
- Current Google listing hours: Monday 11:00–23:00; Tuesday–Sunday 10:00–23:00
- Bengali/Bangladeshi identity; biryani and North Indian dishes also appear on current ordering platforms
- Delivery, takeaway, and indoor seating
- Current menu examples: Mini Bengali thalis, Katla Kalia, Shorshe Katla, Pabda preparations, Chicken Kassa, Chicken Chaap, Basanti Pulao combinations, Chicken Dum Biryani, party boxes
- Current social proof: Google 4.1 / 496 reviews; Zomato 4.0 / 62.5K delivery ratings (checked 2026-09-03)
- FSSAI number displayed by Zomato: 12818019004900 (displayed as platform-sourced; not independently regulator-verified)

### Claims deliberately omitted

No invented founder story, founding year, “best in Kolkata” claim, delivery-time guarantee, direct-order discount, sourcing claim, secret recipe claim, or unverified policy.

## 2. Audience

Primary audience: South Kolkata residents deciding what to eat now. Key motivations are Bengali comfort food, Bangal / East Bengal flavour nostalgia, dependable delivery, familiar thalis/fish curries, and generous meal formats. Secondary audiences include takeaway customers, nearby diners, and families ordering larger meals.

## 3. Conversion goals

1. **Order Online** — primary CTA to the current Zomato ordering surface.
2. **Call to Order** — `+91 98311 68763`.
3. **Get Directions** — Google Maps route to the Naktala/Brahmapur location.
4. Secondary: browse evidence-backed dish groups and visit the official Facebook page for more real imagery/updates.

Mobile receives a persistent **Order · Call · Directions** action bar.

## 4. Creative direction

### Concept: “Bangal Table, Kolkata Address”

Warm, editorial, Bengali, food-first, and approachable rather than fine-dining luxury. The core cultural line is **“ওপারের স্বাদ এপারে”**. Food photography carries the visual weight; ornament is restrained.

Avoid generic luxury black/gold restaurant styling, Kolkata clichés, fake heritage, pseudo-palace motifs, and decorative effects that compete with the food.

## 5. Color system

- **Kosha** `#8C2B24` — primary CTA / emphasis
- **Basanti** `#D89B2B` — highlights
- **Shaak** `#3E5B3C` — secondary accent
- **Bhaat** `#FFF8EC` — main canvas
- **Kagoj** `#F4E8C8` — editorial surfaces
- **Kalo** `#1F1915` — primary text

The palette is derived from recognizable Bengali food tones rather than an invented luxury identity.

## 6. Typography

- **Newsreader** — English editorial display
- **Noto Serif Bengali** — Bengali tagline and selected Bengali accents
- System sans-serif — UI/body fallback and performance safety

Fonts are loaded with swap behavior and the site remains usable if the external font request fails.

## 7. Image strategy

Use **actual EBELA OBELA photography** as the main visual material. For the prototype, images currently come from identifiable third-party restaurant/editorial sources already associated with EBELA OBELA. These are **demo/editorial references only** and must be replaced with owner-supplied originals or licensed copies before commercial launch.

Production preference order:

1. Original EBELA OBELA files supplied by the owner
2. Owner-controlled social originals with confirmed reuse rights
3. New commissioned restaurant shoot
4. Explicitly licensed editorial material

Ideal owner shoot: hero pulao + chicken, fish curry, thali overhead, food details, packing process, exterior/signage, dining space, real team/process.

The running site includes a visible photo-rights note and `PHOTO_RIGHTS.md` documents every prototype source.

## 8. Information architecture

Single conversion-focused page with anchored navigation:

- Home
- Signatures
- Menu
- Story
- Gallery
- Visit
- Order Online

This is intentionally compact; a separate About page is deferred until owner-approved origin/team material exists.

## 9. Section-by-section layout

### Header
Text wordmark, restrained nav, prominent Order Online button.

### Hero
Large real food image, Bengali brand line, concise factual proposition, Order Online + View Menu, quick Call/Directions links, and a secondary actual-food image. Subtle Three.js particles sit *behind* the typography only.

### Social proof
Current Google and Zomato rating signals, explicitly timestamped in metadata/documentation so stale values can be updated.

### Signature dishes
Editorial cards for current evidence-backed menu signals: Basanti Pulao combinations, Bengali fish curries, thalis, Chicken Kassa/Chaap, and Chicken Dum Biryani.

### Bangal identity
Short brand-story section built around the business-owned “ওপারের স্বাদ এপারে” line. It does not invent founder history.

### Menu explorer
Accessible category tabs/buttons with factual example dishes. Prices are intentionally omitted because platform pricing changes.

### Delivery/process
Delivery-first proof and packaging themes supported by current platform review descriptors. No delivery-time promise.

### Gallery
Actual EBELA OBELA photos with source labels and commercial-rights warning.

### Visit
Address, current Google listing hours, phone, directions, map link, Facebook, FSSAI platform disclosure.

### Closing CTA
Direct Order / Call / Directions actions.

## 10. Three.js / animation plan

Three.js is allowed only as a complementary atmospheric layer. On capable desktop/tablet devices, it lazily creates a low-density field of warm, softly moving particles behind the hero copy to suggest spice/aroma in the air. It never obscures food photography, captures no pointer input, and is removed for `prefers-reduced-motion`, small screens, low-power/device constraints, or load failure.

All other motion uses CSS opacity/transform reveals. There is no scroll-jacking, custom cursor, flying food, carousel, or game-like behavior.

## 11. Responsive behavior

Mobile-first. Hero becomes a single-column image/story composition; CTA appears early; sticky bottom actions remain thumb-accessible. Dish/menu sections collapse to one column. Tablet introduces two-column grids. Desktop uses editorial asymmetry and larger whitespace while preserving identical content and actions.

## 12. Accessibility

Semantic landmarks, one H1, logical heading order, skip link, visible focus states, 44px minimum touch targets, keyboard-operable category controls, descriptive alt text, non-color status cues, reduced-motion behavior, and WCAG AA contrast targets. Canvas is decorative and `aria-hidden`.

## 13. Performance

Static HTML/CSS/vanilla JS. No framework or build dependency. Three.js is dynamically imported only after first paint and only on capable devices. Images use responsive sizing attributes, lazy loading below the hero, explicit dimensions/aspect ratios, and graceful source failure states. Hero requests only the primary food image eagerly.

Targets: LCP ≤ 2.5s, CLS ≤ 0.1, INP ≤ 200ms on representative mobile conditions.

## 14. SEO / local discovery

Title: **Ebela Obela | Bengali Food in Naktala, Kolkata**

Meta description centers Bengali thalis, fish curries, pulao, biryani, Naktala/Brahmapur location, and ordering actions without unsupported superlatives.

`Restaurant` JSON-LD includes name, address, phone, verified current hours, geo coordinates, cuisine types, menu anchor, ordering URL, and official Facebook profile. Open Graph and canonical metadata use the GitHub Pages production URL.

Local themes: Bengali restaurant Naktala, Bengali food Brahmapur Kolkata, Bangal food Kolkata, Bengali thali Naktala, Bengali fish curry Naktala.

## 15. Rights / licensing notes

Prototype photography is real EBELA OBELA imagery but is currently sourced from third-party editorial/review pages. It is **not declared production-licensed**. The site and `PHOTO_RIGHTS.md` explicitly mark this. Replace or obtain written reuse permission before commercial launch.

No AI-generated food imagery is presented as restaurant food.

## 16. Implementation sequence

1. Verify current public facts and menu signals.
2. Document plan and photo rights.
3. Implement static semantic page.
4. Add mobile conversion controls.
5. Add accessible category interaction and reduced-motion behavior.
6. Add optional lazy Three.js ambience.
7. Add SEO/JSON-LD/Open Graph.
8. Run syntax and content checks.
9. Commit atomically to `main`.
10. Deploy with GitHub Pages Actions and verify deployment workflow.

## 17. Acceptance criteria

- Immediately reads as EBELA OBELA rather than a generic restaurant template.
- Food + Bangal identity + Naktala location + primary action are visible in the first viewport.
- Order Online is the dominant CTA; Call and Directions are always easy on mobile.
- No invented price, discount, founder history, service, review quote, or policy.
- Current menu examples are evidence-backed.
- Real photography remains dominant; Three.js is purely atmospheric and nonessential.
- Prototype photo rights are clearly flagged before commercial use.
- Mobile-first responsive layout.
- Keyboard navigation, focus states, alt text, reduced motion, and static fallback work.
- Restaurant JSON-LD, Open Graph, canonical URL, title, and description are present.
- No framework/build dependency is needed to serve the site.
- GitHub Pages deployment is automated from `main`.
