# NOVIN — Project State

## Scope
`template-1` is the flagship production-grade multilingual e-commerce project in the MxPersonal template portfolio.

## Product Direction
- Brand: NOVIN
- Type: Full-stack lifestyle e-commerce
- Base locales: Persian (`fa`, RTL) and English (`en`, LTR)
- Future locales: architecture must allow adding more locales without redesigning the application
- Brand direction: Tactile Warm Commerce
- Deployment target: Vercel
- Data/Auth: Supabase

## Existing Working Foundation
- Next.js + React + TypeScript
- Supabase SSR client/server integration
- Email/password authentication
- Google OAuth flow
- Login, registration, forgot-password and password update flows
- User account/profile and addresses
- Role-aware customer/admin access
- Admin areas for products, orders and customers
- Product catalog and product detail pages
- Persistent local cart
- Product JSON-LD
- Sitemap, robots, manifest and Open Graph foundations
- Basic CSP/security headers
- Supabase RLS and performance indexes

## Current Gaps
### Internationalization
- Root layout is hard-coded to Persian RTL
- UI copy is largely hard-coded in Persian
- Route structure is not locale-aware
- Metadata, sitemap and structured data are not fully localized
- Product/category model is not translation-normalized

### Commerce
- Checkout is currently a controlled preview
- No production order-creation transaction from cart
- No server-authoritative price/stock validation in checkout
- Payment abstraction/verification is not complete
- Inventory decrement/reservation flow is not complete
- Coupon/discount architecture is not complete

### Product Data
- Current product model mixes localized and invariant data
- `english_name` exists, but descriptions/features/categories are not modeled as true translations
- Category values are localized strings rather than locale-independent identifiers

### Quality
- No first-class project test scripts yet for unit/integration/E2E
- Observability/error reporting is limited
- Production data fallback behavior can hide Supabase failures

### Design
- Existing UI will be redesigned into a unique NOVIN identity
- NOVIN must not reuse the visual language of template-2 through template-10
- Brand identity must extend beyond logo into typography, tokens, graphic language, component geometry and motion

## Preserve
Do not throw away useful working code. Preserve and improve:
- Supabase SSR architecture
- Auth flows
- RLS policies and admin guard strategy
- Product/cart logic that remains compatible with the new locale/data architecture
- Existing SEO/security foundations where technically sound

## Main Risks
1. Adding i18n after more features would create unnecessary rework.
2. Checkout must never trust client-provided prices or totals.
3. Locale-aware database changes must preserve current data safely.
4. Redesign must not regress auth/admin/store functionality.
5. RTL and LTR must be tested as first-class layouts, not mirrored as an afterthought.

## Stage-Gated Workflow
1. Project Foundation
2. Brand DNA + Visual Identity
3. Information Architecture + UX
4. Design System
5. i18n Architecture
6. Storefront Redesign
7. Catalog/Data Translation Layer
8. Auth + Account Localization
9. Checkout + Orders + Inventory
10. Payments + Discounts
11. Admin Redesign
12. SEO/AEO/GEO
13. Testing + Accessibility
14. Security + Performance
15. Production Launch + Handover

Each stage is completed, reviewed, and explicitly approved before moving to the next stage. Checklists are guidance, not blockers; user approval is the stage gate.
