# NOVIN — Product Definition

## Product
NOVIN is a multilingual full-stack lifestyle commerce platform designed as a portfolio-quality implementation that can also serve as a reusable production foundation.

## Core Promise
A calm, trustworthy and premium shopping experience for carefully selected everyday products, with fast discovery, clear product information and a low-friction checkout.

## Base Markets and Locales
- Persian (`fa`) — primary RTL experience
- English (`en`) — primary LTR experience
- Additional locales must be addable through configuration + translations, not application rewrites

## Primary Audiences
- Customers browsing lifestyle, digital, home and accessory products
- Mobile-first shoppers who need fast discovery and checkout
- Returning customers managing addresses and orders
- Store administrators managing products, stock, orders, customers and campaigns

## Product Principles
1. Trust before novelty
2. Product clarity before decorative UI
3. Mobile UX is first-class
4. RTL and LTR are equally intentional
5. Server is authoritative for price, stock and order totals
6. Brand identity is visible in interaction, not only decoration
7. Accessibility and performance are product features

## Feature Priority
### MUST
- `fa` / `en` locale routing
- Native RTL / LTR
- Language switcher
- Localized navigation, validation and system messages
- Localized SEO metadata, sitemap, hreflang and structured data
- Localized product/category content model
- Product catalog, filtering, search and product detail
- Persistent cart
- Authentication and Google OAuth
- Customer profile and addresses
- Secure checkout
- Server-authoritative product/stock/total validation
- Order creation and order history
- Admin product/order/customer management
- Inventory controls
- Responsive/mobile UX
- Accessibility baseline
- QA, security and production build validation

### SHOULD
- Wishlist
- Recently viewed
- Product comparison
- Coupons and campaign discounts
- Search suggestions
- Featured/curated collections
- Shipping methods
- Order status timeline
- Better admin analytics
- Campaign landing-page templates

### LATER
- Reviews and ratings
- Recommendation engine
- Customer segmentation
- Advanced promotions engine
- Loyalty/rewards
- Multiple payment adapters
- Multi-currency presentation
- PWA/offline enhancements
- Advanced observability and analytics dashboards

## Key User Journeys
### Shopper
Home → Discover/Search → Product → Cart → Auth/Guest decision → Address → Shipping → Payment → Confirmation → Orders

### Returning Customer
Login → Account → Orders / Addresses / Wishlist → Reorder or continue shopping

### Admin
Admin Login → Dashboard → Products / Inventory / Orders / Customers / Discounts → Publish/update → Audit result

## Campaign Landing System
NOVIN may include reusable campaign landings for seasonal sales, product drops and category promotions. These pages must inherit NOVIN's design system while allowing campaign-specific art direction within defined brand limits.

## Success Criteria
- Persian and English flows feel equally native
- No important UI copy is hard-coded in feature components
- Core commerce calculations are server-authoritative
- Storefront is recognizably NOVIN and visually distinct from all other templates
- Main user journeys work on mobile, tablet and desktop
- Core public pages are indexable and correctly localized
- Private/transactional pages are protected appropriately
