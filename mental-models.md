# Mental models & frameworks — negative keywords


## Mander's Smart-Bidding-bypass conditions
Manual negatives are LOW-leverage when ALL four hold: (1) Smart Bidding (tROAS/tCPA/MaxConv), (2) ≥50–100 conversions/month, (3) actual purchase/revenue tracked, (4) direct online e-commerce transaction Google can see. Outside ANY of these, manual negatives matter.

---

## Three-tier scope decision
Account-level: term is universally never wanted AND not brand-related. Campaign-level: term is irrelevant to all ad groups in this campaign. Ad-group-level: only when funneling traffic between ad groups in the same campaign.

---

## Match-type-by-shape rule
Single offensive word → broad. Multi-word phrase that should be killed in any context → phrase (default). Single ambiguous query you can't generalize → exact, surgical.

---

## Two-layer search-terms review (Heath)
Pass 1 (no data needed): scan for clearly irrelevant intent terms, negate immediately. Pass 2 (data accrued, ≥2 weeks): cull terms by bad CPA/ROAS at ~1–1.5x target spent without conversion.

---

## Pre-launch negative-mining workflow (Heath/Taylor)
(1) Keyword Planner > Discover new keywords on each main targeted term per ad group. (2) Use Refine keywords panel to surface brand/non-brand and category filters. (3) Set Keyword Planner geo to actual ad target, not the agency's home country. (4) Through hundreds of suggestions, flag obvious irrelevant categories.

---

## Three-tier AI-assisted NK stack (Grow My Ads)
Tier 1 — Claude chat + CSV: zero setup, fine for one-off small accounts. Tier 2 — Claude Project + skill file: per-client setup, one-command repeatable. Tier 3 — Claude Code + Google Ads API: fastest, no manual export, agency-scale. MCP is alternative to direct API but uses more tokens.

---

## Schaefer's four-bucket AI classification
Definite waste → auto-negate candidate. Likely waste → auto-negate at higher aggressiveness. Monitor → human review (Schaefer's preferred bias is to oversize this bucket). Optimal/keep → positive signal. Rationale should combine product/brand-fit reasoning with CPC vs. account-average.

---

## Themed shared-list taxonomy
At minimum: (1) universal junk-intent (free/cheap/jobs/DIY/used), (2) competitor brands, (3) out-of-area, (4) support/repair/complaint, (5) informational/research, (6) wrong-product (sub-segments you don't sell), (7) brand exclusion list applied to non-brand campaigns.

---

## Restrictive-then-loosen launch posture
Default: launch tight; relax once you have data. Inverts when (a) account has high signal volume, (b) campaign goal is growth/expansion, (c) running broad-match + Smart Bidding with ≥50 conv/mo.

---

## Competitor-brand tokenization (Mancini)
For every competitor brand: add singular, plural, partial tokens (Roto + Rooter for Roto-Rooter), and both spaced and unspaced ampersand forms (P & S, P&S). Negatives don't auto-handle these variants.

---
