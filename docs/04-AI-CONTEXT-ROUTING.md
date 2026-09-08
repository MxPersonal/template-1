# NOVIN — AI Model Routing, Context & Usage Strategy

Verified against official OpenAI model documentation on 2026-09-08. Availability can differ between ChatGPT, Codex and API plans/surfaces, so treat model access as runtime-dependent.

## Current OpenAI Routing Pool

### GPT-6 Astra
Official positioning: most capable model for the hardest end-to-end work.
API reasoning efforts: `low`, `medium`, `high`, `xhigh`, `max`.
Use for:
- repository-wide architecture
- complex i18n migrations
- database/RLS/order/payment architecture
- difficult debugging
- security-sensitive review
- multi-system refactors
- final launch-critical verification

Do not default to Astra `max`; reserve `xhigh/max` for tasks whose complexity or risk justifies the usage.

### GPT-5.6 Sol
Official positioning: flagship model for complex professional work.
API reasoning efforts: `none`, `low`, `medium`, `high`, `xhigh`, `max`.
Use as the primary project model for:
- UX/IA work
- design-system implementation
- normal coding/refactors
- documentation
- code review
- SEO implementation
- QA analysis

Recommended default for this project: `medium` or `high`.

### GPT-5.6 Terra
Official positioning: balance of intelligence and cost.
API reasoning efforts: `none`, `low`, `medium`, `high`, `xhigh`, `max`.
Use for:
- medium-complexity coding
- repetitive component work
- test generation
- content transformations
- translation-structure work
- documentation cleanup
- secondary verification

### GPT-5.6 Luna
Official positioning: cost-sensitive/high-volume workloads.
API reasoning efforts: `none`, `low`, `medium`, `high`, `xhigh`, `max`.
Use for:
- bulk translation drafts
- JSON/message transformations
- fixture generation
- repetitive formatting
- simple codemods with tight tests
- large-volume low-risk data cleanup

## Stage Routing
| Stage | Primary model | Effort | Escalation |
|---|---|---:|---|
| Foundation | GPT-5.6 Sol | medium | Sol high |
| Brand identity strategy | GPT-5.6 Sol | medium/high | Astra high for difficult synthesis |
| IA + UX | GPT-5.6 Sol | high | Astra high |
| Design system | GPT-5.6 Sol | high | Astra high for architecture issues |
| i18n architecture | GPT-6 Astra | high | Astra xhigh |
| Storefront implementation | GPT-5.6 Sol | high | Astra high/xhigh for repo-wide refactor |
| DB translation migration | GPT-6 Astra | high/xhigh | Astra max only if migration/risk becomes unusually complex |
| Auth/account | GPT-5.6 Sol | high | Astra high for cross-locale auth issues |
| Checkout/orders/inventory | GPT-6 Astra | xhigh | Astra max for difficult transactional bugs/security review |
| Payments/promotions | GPT-6 Astra | xhigh | Astra max for launch-critical multi-system issues |
| Admin redesign | GPT-5.6 Sol | high | Astra high |
| SEO/AEO/GEO | GPT-5.6 Sol | medium/high | Terra medium for bulk metadata work |
| Tests/fixtures | GPT-5.6 Terra | medium | Sol high for failing critical tests |
| Bulk translation/data | GPT-5.6 Luna | low/medium | Terra medium for ambiguity |
| Security/performance audit | GPT-6 Astra | high/xhigh | Astra max for difficult launch blockers |
| Final launch review | GPT-6 Astra | high/xhigh | max only for unresolved high-risk problems |

## Context Architecture
Do not treat a 1M-token window as permission to dump the whole repository into every task.

### Source-of-Truth Pack
Always prefer these concise docs before broad repository loading:
1. `docs/00-PROJECT-STATE.md`
2. `docs/01-PRODUCT.md`
3. `docs/02-BRAND.md`
4. `docs/03-ROADMAP.md`
5. this file
6. the current stage specification
7. only the code/files relevant to that stage

### Per-Task Context Packet
Every substantial Codex task should include:
- Goal
- Current stage
- Relevant constraints
- Files to inspect
- Expected files to change
- Acceptance criteria
- Non-goals
- Verification commands

### Context Budget Rule
Prefer focused context:
- small task: 3–8 relevant files
- medium task: 8–20 relevant files
- large architectural task: selected directories + project docs
- repository-wide task: use staged discovery/search before loading more code

Avoid repeatedly pasting generated docs and unchanged code if Codex can read them directly from the repository.

## Usage Management
### Default pattern
- Use Sol medium/high for most work.
- Use Terra for medium-risk repetitive work when available.
- Use Luna for high-volume deterministic transformations.
- Escalate to Astra only when architecture, risk, ambiguity or cross-system coordination warrants it.

### High-effort triggers
Escalate effort when one or more applies:
- database migration can damage existing production data
- auth/payment/security boundary is changing
- change spans many independent modules
- repeated normal-effort attempts failed
- bug is nondeterministic or hard to reproduce
- launch is blocked
- requirements conflict and require global architectural reconciliation

### Do not waste high effort on
- copy edits
- simple CSS tweaks
- predictable translations
- renaming
- trivial component extraction
- straightforward documentation formatting

## Compaction / Continuity
At the end of each approved stage update the project docs with:
- decisions made
- files changed
- unresolved risks
- verification results
- exact next stage

New threads should start from these repository docs rather than relying on raw prior-chat history.

## Prompt Prefix Strategy
Keep stable project constraints at the top of recurring Codex prompts so prompt caching can benefit where the surface supports it. Put task-specific instructions after the stable project prefix.

## Core Stable Prefix
Repository: `MxPersonal/template-1`
Branch: `main`
Brand: `NOVIN`
Base locales: Persian (`fa`, RTL) and English (`en`, LTR)
Future multilingual expansion is required.
Preserve useful existing architecture.
NOVIN must have a unique Tactile Warm Commerce visual identity.
Prioritize correctness, accessibility, security, performance and production verification.
Do not silently hide production failures with demo fallback behavior.
Do not trust client-provided commerce totals.

## Official References Checked
- OpenAI model catalog: https://developers.openai.com/api/docs/models/gpt
- GPT-6 Astra: https://developers.openai.com/api/docs/models/gpt-6-astra
- GPT-5.6 Sol: https://developers.openai.com/api/docs/models/gpt-5.6-sol
- GPT-5.6 Terra: https://developers.openai.com/api/docs/models/gpt-5.6-terra
- GPT-5.6 Luna: https://developers.openai.com/api/docs/models/gpt-5.6-luna
