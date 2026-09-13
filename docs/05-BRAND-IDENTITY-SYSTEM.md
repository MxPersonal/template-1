# NOVIN — Brand Identity System

Status: Stage 1 design specification — pending visual approval before implementation.

## 1. Identity Objective
NOVIN must look like a real consumer brand rather than a generic e-commerce template. Its visual identity should communicate warm confidence, curation, tactility, usefulness and quiet premium quality. The system must work in Persian RTL and English LTR, from tiny mobile headers and favicons to campaign landing pages and admin surfaces.

## 2. Recommended Creative Direction — Crafted Orbit
The primary identity direction is **Crafted Orbit**: soft geometric typography combined with a controlled orbit/cut motif derived from the `O` and `N` letterforms. The geometry should imply discovery, curation and everyday objects moving into an ordered collection without becoming futuristic or cosmic.

### Core characteristics
- custom-drawn Latin NOVIN wordmark; never plain text set in a stock display font
- rounded geometric skeleton with selective humanist tapering
- distinctive `N` diagonal that can become a crop/frame device
- distinctive `O` with an offset inner orbit/cut usable as the primary graphic motif
- quiet asymmetry to avoid looking sterile
- strong kerning and compact small-size variant
- premium but approachable; no fashion-house coldness and no playful-kids aesthetic

## 3. Logo Family
Required production assets:
1. Primary horizontal `NOVIN` wordmark
2. Compact wordmark for narrow headers
3. `N` monogram for app icon/favicon/avatar
4. `O-Orbit` supporting mark for campaigns, loading states and image crops
5. one-color positive version
6. one-color reverse version
7. light-background full-color version
8. dark-background full-color version
9. motion-safe animated construction for campaign splash only

### Logo usage rules
- preserve generous clear space around the primary mark
- do not place the wordmark inside generic pills/cards
- do not recolor individual letters randomly
- do not add drop shadows, glass effects or uncontrolled gradients
- avoid stretching, condensing or re-typesetting the wordmark
- Persian UI may display the Latin NOVIN brand mark while Persian brand copy remains localized; do not invent a Persian transliteration logo unless deliberately designed later

## 4. Monogram
### `N` Monogram
Construction direction:
- one vertical stem remains stable
- diagonal stroke uses the same softened cut found in the wordmark
- negative space forms a subtle forward/open gesture
- must remain identifiable at 16px
- usable as favicon, account avatar, loading signature and social profile mark

### `O-Orbit` Supporting Mark
Not the primary favicon. Use selectively for:
- campaign imagery
- collection separators
- hover masks
- loading/progress animations
- packaging-style graphic patterns

## 5. Brand Geometry
The UI and graphic system derives from four shapes:
- **Soft Arch** — from the curved `N` terminal
- **Orbit Cut** — from the offset `O` counter
- **Crop Window** — rounded-rect product image frame with one asymmetric corner/cut
- **Contour Line** — thin warm-neutral line following product silhouettes or section boundaries

These motifs must appear subtly across the UI rather than as decoration everywhere.

## 6. Color System
Final palette values for implementation should be contrast-tested; the following is the Stage 1 brand palette.

### Foundation
- Canvas / Ivory 50 — `#FBF8F3`
- Canvas / Ivory 100 — `#F7F2EA`
- Surface / Sand 200 — `#E9DED2`
- Ink / Espresso 900 — `#332720`
- Ink / Espresso 800 — `#49382F`

### Brand
- Clay 600 — `#B96842`
- Clay 500 — `#C97A54`
- Taupe 500 — `#9C826D`
- Sage 500 — `#7E907D`

### Functional direction
- Success — deep muted green, selected after WCAG validation
- Warning — amber/ochre, selected after WCAG validation
- Error — brick red, selected after WCAG validation
- Info — desaturated blue-gray, selected after WCAG validation

### Color behavior
- Ivory is the dominant canvas.
- Espresso carries typography and high-contrast controls.
- Clay is the primary commerce accent for key actions and promotional emphasis.
- Sage is secondary/supporting and must not compete with primary CTAs.
- Product photography may introduce category color but should not redefine brand tokens.

## 7. Typography Direction
Typography must support multilingual commerce, data-heavy admin surfaces and native RTL/LTR behavior.

### Persian
Primary requirements:
- excellent Persian reading rhythm
- strong UI numeral legibility
- reliable variable/weight support
- clear compact forms for filters, tables and checkout

Current implementation uses Vazirmatn; it may remain the practical UI baseline during redesign, but Stage 3 should compare it against suitable Persian alternatives before locking the final pair.

### English
Direction:
- refined humanist/grotesk rather than futuristic geometric SaaS typography
- moderate width and excellent UI legibility
- compatible x-height and perceived weight with the chosen Persian face

### Display typography
Use hierarchy, size, spacing and composition rather than an unrelated decorative font. Campaigns may use a controlled editorial display companion only if it remains consistent with Crafted Orbit.

## 8. Icon Language
- rounded but not cartoonish
- consistent optical stroke weight
- simple silhouettes
- direction-sensitive arrows automatically mirror in RTL where semantics require it
- custom commerce glyphs may echo the Orbit Cut geometry
- avoid mixing multiple icon packs visibly in the final UI

## 9. Image System
### Photography
- natural directional light
- warm ivory, wood, ceramic, textile and stone surfaces
- realistic material detail
- calm shadows
- product-first composition
- restrained lifestyle context
- generous copy-safe negative space

### Product isolation
Packshot and catalog images should remain consistent in scale, crop and shadow language.

### Image treatment
- Crop Window motif can frame hero/editorial imagery
- avoid heavy overlays
- no neon gradients
- no random AI-surreal backgrounds on core commerce pages

## 10. Motion Identity
Motion vocabulary:
- tactile press: 90–140ms
- interface transition: 160–240ms
- drawer/sheet: 220–320ms
- campaign reveal: 350–600ms, used sparingly

Motion behaviors:
- 1–2% scale/tactile feedback rather than dramatic zooms
- subtle product image crossfade/reframe
- cart add confirmation with restrained spatial feedback
- `O-Orbit` may rotate/resolve once for loading or campaign reveal, never continuously
- full support for `prefers-reduced-motion`

## 11. Surface & Shape Personality
- radii should feel crafted, not universally pill-shaped
- primary product surfaces: medium radius with one optional asymmetric crop detail
- forms: calm, high readability, strong focus state
- drawers/bottom sheets: tactile layered surface using ivory/sand values
- borders: low-contrast warm ink rather than cool gray defaults

## 12. Brand-to-UI Mapping
The identity must visibly influence implementation:
- Header — compact wordmark + clean navigation rhythm
- Hero — large editorial product imagery using Crop Window
- Product Cards — warm surface, controlled image frame, tactile add action
- Buttons — Clay primary action with Espresso text/control hierarchy as needed
- Search — large discovery surface, not a tiny generic header input
- Cart — layered sheet with Orbit Cut detail only as subtle brand signature
- Checkout — visually calmer and more utilitarian than campaign pages
- Account/Admin — related palette and typography, less decorative and more information-dense

## 13. Landing / Campaign Identity
NOVIN should support campaign landing pages without creating a second brand. Campaign pages may increase:
- display scale
- photography drama
- Orbit/Crop geometry
- editorial composition
- motion intensity

But core color, type, logo and interaction language must remain NOVIN.

## 14. Accessibility & Localization Requirements
- every foreground/background pairing must be WCAG-checked before Stage 3 implementation
- do not encode meaning by color alone
- minimum touch targets must remain usable on mobile
- logo clear-space and compact variants must survive both RTL and LTR header layouts
- icon direction, spacing and animation origin must be tested in `fa` and `en`

## 15. Anti-Repetition Guardrails
Do not reuse NOVIN's signature identity in template-2 through template-10:
- no reuse of Crafted Orbit as another project's logo motif
- no identical palette relationships
- no clone of NOVIN product card anatomy
- no copy of its campaign crop language
- no universal shared branded component layer across the portfolio

Engineering utilities may be shared; visual identity components may not.

## 16. Stage 1 Visual Approval Gate
Before Stage 2 begins, approve one final visual direction for:
- primary wordmark
- `N` monogram
- `O-Orbit` supporting mark
- primary palette feeling
- Crafted Orbit geometry

After approval, the selected concept becomes the fixed visual reference for UX architecture and the later design system.

## AI Routing for This Stage
- Brand strategy/specification: GPT-5.6 Sol, medium/high reasoning
- identity critique and constraint reconciliation: GPT-5.6 Sol, high reasoning
- difficult multi-system brand/UI consistency review: use the project's highest-capability reasoning route only when necessary
- image/logo concept generation: specialized image generation, followed by human approval rather than treating generated lettering as production vector artwork

## Important Production Note
Generated visual concepts are art-direction references. The final production logo should be rebuilt as controlled vector paths/SVG so kerning, geometry, small-size behavior, accessibility and consistency are deterministic.
