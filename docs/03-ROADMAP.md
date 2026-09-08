# NOVIN — Stage-Gated Roadmap

## Workflow Rule
Complete one stage, review it, get explicit user approval, then continue. Checklists are guidance only; the approval gate controls progression.

## Stage 0 — Foundation
Deliverables:
- Current-state audit
- Product definition
- Brand DNA
- Execution roadmap
- AI/model routing and context rules
Exit criteria:
- Scope is explicit
- Major risks are documented
- Next stage is unambiguous

## Stage 1 — Brand Identity
Deliverables:
- Final logotype direction
- Monogram
- Logo variants
- Brand geometry/motifs
- Image direction
- Typography candidates
- Refined accessible palette
Exit criteria:
- Visual identity is distinct, reusable and suitable for both Persian/English surfaces

## Stage 2 — IA + UX Architecture
Deliverables:
- Sitemap
- Shopper journeys
- Account/admin journeys
- Mobile-first interaction plan
- Search/filter/product/cart/checkout UX
- Error/loading/empty-state map
Exit criteria:
- Major flows have no structural ambiguity

## Stage 3 — Design System
Deliverables:
- Tokens
- Typography
- Spacing/radius/elevation
- Buttons/forms/navigation
- Product/card/sheet/dialog patterns
- Responsive rules
- RTL/LTR rules
- Motion rules
Exit criteria:
- Enough primitives exist to redesign the storefront consistently without creating a universal-looking template

## Stage 4 — i18n Foundation
Deliverables:
- Locale config for `fa` / `en`
- Locale route architecture
- RTL/LTR document direction
- Translation dictionaries
- Locale-safe links/navigation
- Locale-aware formatting for dates/numbers/currency
- Metadata alternates/hreflang foundations
Exit criteria:
- Same core page can render natively in both Persian and English

## Stage 5 — Storefront Redesign
Order:
1. Header/navigation
2. Home
3. Search/discovery
4. Shop/catalog
5. Product card
6. Product detail
7. Cart/drawer
8. Support/info pages
Exit criteria:
- Distinct NOVIN visual identity on mobile/tablet/desktop in both locales

## Stage 6 — Localized Catalog/Data Model
Deliverables:
- Separate invariant product data from translated fields
- Category keys + translation model
- Product translations
- Localized SEO fields
- Safe migrations preserving existing data
Exit criteria:
- New locale can be added without adding another hard-coded language column

## Stage 7 — Auth + Account Localization
Deliverables:
- Localized auth messages and redirects
- Locale-aware OAuth callback navigation
- Account/profile/address/order UI redesign
Exit criteria:
- Auth/account works in `fa` and `en` without route or direction leakage

## Stage 8 — Checkout + Orders + Inventory
Deliverables:
- Real checkout form
- Address selection/creation
- Shipping abstraction
- Server-authoritative price/stock calculation
- Atomic/transactional order creation path
- Inventory validation/update strategy
- Order confirmation/history
Exit criteria:
- Manipulating browser cart data cannot lower server-calculated total

## Stage 9 — Payments + Promotions
Deliverables:
- Payment adapter contract
- Payment initiation/verification states
- Coupon/discount model
- Campaign landing integration
Exit criteria:
- Payment business logic is isolated from storefront presentation

## Stage 10 — Admin Redesign
Deliverables:
- Branded admin shell
- Product/category/translation management
- Inventory
- Orders
- Customers/roles
- Promotions
- Useful operational dashboard
Exit criteria:
- Admin remains efficient and visually related to NOVIN without sacrificing density/readability

## Stage 11 — SEO / AEO / GEO
Deliverables:
- Localized metadata/canonical/hreflang
- Dynamic multilingual sitemap
- Product/Organization/WebSite/Breadcrumb structured data where appropriate
- Content/entity strategy
Exit criteria:
- Public indexed pages expose coherent locale-specific search metadata

## Stage 12 — Testing + Accessibility
Deliverables:
- Typecheck/lint/build scripts
- Unit/integration coverage for critical logic
- Playwright E2E for critical flows
- RTL/LTR visual/interaction QA
- Accessibility validation
Exit criteria:
- Critical customer/admin journeys pass defined QA scenarios

## Stage 13 — Security + Performance
Deliverables:
- Review CSP/headers
- RLS review
- input validation/rate-limit strategy for sensitive actions
- production error handling/observability
- image/font/bundle/caching review
- Core Web Vitals budget
Exit criteria:
- No known high-impact weakness or silent production fallback in critical flows

## Stage 14 — Production Launch + Handover
Deliverables:
- Environment checklist
- Supabase migration verification
- Vercel production validation
- SEO smoke test
- Auth/payment smoke test
- final README/docs
- rollback notes
Exit criteria:
- Production site is verifiably usable in both base locales
