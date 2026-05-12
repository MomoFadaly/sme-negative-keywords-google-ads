# Canonical Q&A — negative keywords in Google Ads

_v1.0.1 · 104 questions · 18 videos studied · 322 claims · 49 clusters_

## Confidence levels
Verified · Confirmed · Plausible · Disputed · Stale · Not addressed

---

### Q?: How does match type behavior for negative keywords differ from positive keywords, and where does that bite you?
**Confidence:** Verified

Negative match types share the same three names (broad, phrase, exact) but behave fundamentally differently from positive match types — and Google's own docs confirm the asymmetry. Per Google's help center, 'Negative keywords won't match to close variants or other expansions.' Positive exact match now expands to plurals, misspellings, synonyms, reorderings and intent-matches; negative exact does NOT — it blocks only the literal phrase. Negative broad blocks only when ALL the negative words appear in any order (it does not auto-expand to plurals or sub-sets). Negative phrase blocks the phrase in word order but allows surrounding words. The bite: practitioners who mentally model negatives as 'just the inverse of positives' silently under-block plurals, misspellings, and reordered variants. Per Ammar, the 2024 expansion drift compounds this: 'exact has turned into phrase, phrase into broad, broad into literally everything' — but negatives stayed literal, making the gap larger every year.

**Sources:** Google Ads Help — About negative keywords (claim 63 verified) · Max | Google Ads Nerd — claim 104 · Ammar | Google Ads For Leads — claim 127 · Ben Heath — claim 14


---

### Q?: When does adding a negative keyword at the campaign level vs. the ad-group level change behavior?
**Confidence:** Confirmed

Campaign-level is the right scope when the term is irrelevant to all ad groups in that campaign. Ad-group-level is the right scope only when you're funneling traffic between ad groups inside the same campaign — for example, blocking 'truck' on a sedan ad group so queries route to the truck ad group instead. Per Solutions 8: 'add negatives at the ad group level only when negative keywords only apply to a specific [ad group]; otherwise you create redundancy you must duplicate every time.' Default to campaign-level (or shared list) for portability; reach for ad-group only with deliberate funneling intent.

**Sources:** Solutions 8 — claims 5, 6, 12 · Ben Heath — claim 15 · Ammar | Google Ads For Leads — claim 129


---

### Q?: How do negative keyword lists work across multiple campaigns, and when should you use a shared list vs. campaign-level negatives?
**Confidence:** Confirmed

Shared negative-keyword lists live under Tools > Shared Library > Exclusion Lists and apply across multiple campaigns; you can also create them on the fly via the 'save to new or existing list' checkbox when adding negatives. Use a shared list when the same negatives apply to multiple campaigns or future campaigns — competitor brands, out-of-area, junk-intent, brand-exclusion-applied-to-non-brand. Use campaign-level when the term is specific to one campaign's funnel structure. UPDATED 2025-08-07: shared negative-keyword lists CAN now attach to Performance Max campaigns (rollout completed Aug 7 2025 per PPC News Feed and Search Engine Land). PMax campaign-level cap raised to 10,000 in March 2025 (up from 100). Account-level negatives still propagate to PMax automatically; reusable lists allow up to 5,000 keywords per list × 20 lists per account.

**Sources:** Google Ads Help — About account-level negative keywords (claim 131 verified) · Solutions 8 — claim 5 · Darren Taylor — claim 268 (themed lists)


---

### Q?: How do close variants and Google's matching of plurals/misspellings/synonyms interact with your negatives, especially after the 2024 broad-match expansions?
**Confidence:** Verified

Positive keywords expand aggressively (close variants, plurals, misspellings, synonyms, intent-matches, reorderings) — Google's own docs confirm 'close variants allow keywords to match to searches that are similar, but not identical to the targeted keyword.' Negative keywords do NOT expand: 'Negative keywords won't match to close variants or other expansions' (Google Ads Help). Practical consequence: every plural, misspelling, ampersand-spaced/unspaced form, and major variant must be added explicitly. Mancini's tokenization rule for competitor brands ('Roto', 'Rooter', 'P & S' AND 'P&S') generalizes the principle. Michelle Kop notes Google sometimes claims to handle plurals on negatives but it's unreliable — add them explicitly.

**Sources:** Google Ads Help — close variants doc (claim 2 verified) · Google Ads Help — negative keywords doc (claim 63 verified) · Mike Mancini — claim 95 (tokenization)


---

### Q?: Why don't negative phrase or negative exact match block searches with extra words inserted between your terms, and how do you handle that?
**Confidence:** Confirmed

Negative phrase blocks queries containing the phrase in the same word order but allows extra words BEFORE or AFTER (not in the middle); negative exact blocks ONLY the literal exact phrase. So 'home design software free' as exact-match negative will not block 'home design software' (missing word) or 'free home design software' (different order — it's a different exact). Heath's fix is correct: don't stop at the full-phrase negative — also pull each offending root word ('software', 'free') out as a separate broader negative so partial matches are caught. This pairs with the standard 'add a single-word root negative alongside the search-term-report exact-match' workflow (TMMI, Grow My Ads agree).

**Sources:** Ben Heath — claims 19, 20 · TMMI — claim 220 · Grow My Ads — claim 184


---

### Q?: What's the right cadence for reviewing the search-terms report and acting on it across new vs. mature campaigns?
**Confidence:** Confirmed

Cadence scales with spend and campaign age. New campaigns: daily for the first week, then every 3 days for the next month. Mature mid-spend accounts: every 3 days (Solutions 8) to weekly (Ben Heath, Ammar) is the practitioner consensus. High-spend accounts (>$30k/mo): daily. Low-spend SMB: 5–10 minutes weekly is enough. Per Aaron Young, leave at least one optimization cycle between changes so attribution windows close. Stew Schaefer's AI workflow uses 7-day rolling exports as the default window.

**Sources:** Solutions 8 — claim 11 (every 3 days) · Ben Heath — claim 21 (weekly) · Ammar — claim 133 (3 days / weekly / daily by spend) · Stew Schaefer — claim 312 (7-day window)


---

### Q?: When should you build a pre-launch negative list versus mining negatives from live search-terms data?
**Confidence:** Confirmed

Both — pre-launch lists save spend during the first 1–4 weeks before the search-terms report has enough volume to mine. Heath's pre-launch workflow uses Keyword Planner's Discover-new-keywords + Refine-keywords panel on each main targeted term per ad group; Mancini applies a 2,300-term curated list (with per-term review). Post-launch, switch to ongoing search-terms-report mining as the primary mechanism. Heath: 'have as many [negatives] on the front end as you can.' But never paste a pre-built list without per-term review — the 'hire' antipattern from the 400-term Paid Insights list killed an agency's lead-gen.

**Sources:** Ben Heath — claims 22, 24 (Keyword Planner workflow) · Mike Mancini — claims 91, 98 (2,300-term list) · Solutions 8 — claim 10 (paid insights antipattern)


---

### Q?: How many irrelevant impressions/clicks does a search term need to accumulate before you negative it out?
**Confidence:** Confirmed

Impressions alone are not enough — you want at least a few clicks AND at least 2 weeks of attribution time before deciding. Common operational thresholds: ≥1 click with no conversion at 1–1.5x target CPA spent (most aggressive); Schaefer's tool defaults to 1+ click OR 30+ impressions as a pre-filter; Aaron Young allows ~10% of spend as a wider tolerance. Darren Taylor warns most advertisers act too early — impression-only data is insufficient signal. The right rule: combine clicks + spend-vs-CPA + attribution window, not any single threshold.

**Sources:** Stew Schaefer — claim 311 (1+ click or 30+ impressions) · Darren Taylor — claim 270 (threshold too low) · Aaron Young — claim 167 (~10% spend)


---

### Q?: How do you decide which match type to use when adding a negative — exact, phrase, or broad?
**Confidence:** Confirmed

Match-type-by-shape rule: single offensive/junk word → broad (e.g., 'free', 'jobs'). Multi-word phrase you want killed in any context → phrase as the safe-middle default. Single ambiguous query you can't generalize → exact, surgical removal. For single-word negatives, broad and phrase behave identically — both block any query containing that word. Most practitioners (Kop, KeyCommerce, Grow My Ads, Heath) default to phrase for multi-word; Solutions 8's 'always broad' is too aggressive for multi-word because broad blocks any combination of those words in any order.

**Sources:** Michelle Kop / KeyCommerce / Grow My Ads — cluster C7 consensus · Ben Heath — claim 200 (single word broad) · Solutions 8 — claim 8 (always broad — minority)


---

### Q?: When does adding more negative keywords HURT performance, and how do you spot you've crossed that line?
**Confidence:** Disputed

Negatives hurt when they (1) block on-topic terms whose intent you misread (Home Reserve 'RV' case), (2) strip Smart Bidding signal in mature accounts with full purchase tracking (Mander's frame), or (3) silently break new services after the business expands (stale account-level negatives, per Ammar). Spot it via: a sudden drop in impression share, a fall in conversion volume after a list update, or an audit revealing brand/service terms in your negative lists. Per Mander, every manual negative is the human overriding the algorithm — and 'spoiler alert, you often don't know better.' That said, most accounts in the wild aren't yet at the Smart-Bidding maturity that frame requires.

**Sources:** Daryl Mander — claims 36, 37 (override frame) · Solutions 8 — claim 9 (RV case) · Ammar — claim 132 (stale account negatives)


---

### Q?: Should brand terms be negatived out of non-brand Search and Performance Max campaigns, and when does that backfire?
**Confidence:** Confirmed

Yes — apply a brand-terms negative list to all non-brand campaigns so brand searches are funneled to your dedicated brand campaign, where bids and copy are tuned for that intent. Per Grow My Ads, this is standard hygiene. It backfires when (a) the brand-negative list is account-level and silently blocks brand variants you didn't anticipate (Gibson case via KeyCommerce), or (b) it's stale and blocks new product/sub-brand names after expansion. Apply at campaign-level via shared list, not account-level, for everything except clearly universal blocks.

**Sources:** Grow My Ads — claim 186 · Ben Heath — claim 60 (branded campaigns need fewer negatives) · Ammar — claim 132 (stale account-level)


---

### Q?: What's the standard 'block competitor brand names' decision — when do you do it, when do you bid on them instead?
**Confidence:** Disputed

Default: block. Per Heath, Mancini, Schaefer, Grow My Ads — competitor brand searches typically don't convert and call/click traffic is often customer-service-related (complaints, appointment reschedules at the wrong company in home services). Bid on competitor brands only when (a) you can match price/positioning, (b) your landing page is genuinely comparison-honest, (c) the account has signal to absorb the noise, AND (d) you have expertise to manage it — Heath warns 'you really need to know what you're doing otherwise you can waste a lot of money.' Max's appeal to Google's messy-middle research overstates the case: the actual figure is 28% (not 30%) and required full behavioural-supercharging — a primary-source-verified contradiction.

**Sources:** Mike Mancini — claim 93 (5–7 year reversal) · Stew Schaefer — claim 321 (price-tier mismatch) · Think with Google — Decoding Decisions (claim 124 contradicted) · Ben Heath — claim 26


---

### Q?: What are the most common mistakes when using broad-match negatives that beginners don't realize until traffic disappears?
**Confidence:** Confirmed

Top mistakes: (1) using broad-match-negative on a single common name like 'Lauren' or a state abbreviation 'IN' — blocks every query containing the word in any context (the LA painter case lost 25% of conversions). (2) Forgetting that broad-match negative requires ALL words present — adding 'cheap shoes' as broad-negative does NOT block 'cheap' alone. (3) Pasting search-terms-report rows verbatim with extra junk words and getting too-narrow exact match. (4) Treating broad-match negatives as if they auto-handle plurals and variants — they don't. The fix: phrase as default for multi-word, broad only for unambiguous junk single words.

**Sources:** Solutions 8 — claim 9 · Cluster C25 over-blocking war stories · Google Ads Help — claim 63 verified


---

### Q?: Why do duplicate or conflicting negatives across account/campaign/ad-group levels and shared lists cause silent under-delivery, and how do you audit for them?
**Confidence:** Confirmed

Negatives propagate down — account-level applies everywhere, campaign-level applies to all ad groups in a campaign, shared lists apply to attached campaigns. When the same term sits at multiple levels, you can't easily tell which is blocking; when business expands, stale account-level rules silently kill new services (Ammar's case). Audit method: pull all negatives via Google Ads Editor or API into a single sheet, group by term, sort by occurrences across scopes, look for (a) brand/sub-brand terms in any list, (b) terms with conflicting match types, (c) terms older than 12 months that haven't been touched. Pair with the search-terms 'added/excluded' column to confirm which rule actually fired.

**Sources:** Ammar — claim 132 · KeyCommerce + Aaron Young — cluster C29 · Grow My Ads / TMMI — claims 72, 221 (added/excluded column)


---

### Q?: What's the trap with adding generic words like 'free,' 'cheap,' or 'jobs' as negatives without thinking through intent?
**Confidence:** Disputed

The trap: a word can flip from negative to positive based on the offer. Solutions 8's 'hire' as negative blocked 'hire a Google Ads agency' for an agency. Mander's case: 'free [paid product]' searches sometimes convert when users discover free options are scammy and buy paid. Heath's exception: if a free front-end IS your offer, don't negative 'free.' For a software reseller of paid products, 'free Microsoft Office' is potentially valuable traffic. Rule: never paste an intent-word list without per-term review against your specific offer. Add 'free' / 'cheap' / 'jobs' / 'DIY' as defaults for premium offers; review every term for offer-match before adding.

**Sources:** Solutions 8 — claim 10 (hire antipattern) · Daryl Mander — claim 32 (free Office) · Ben Heath — claim 16


---

### Q?: Why does pasting negatives directly from a list of search terms (without cleaning) cause symbols, plus signs, and quotes to break the negative?
**Confidence:** Confirmed

Search-term strings often contain quotes, plus signs, and brackets that mean something specific in Google Ads syntax. Per Solutions 8, the +/[]/quote modifiers used for positive keywords don't apply to negatives the same way; per Loves Data and KeyCommerce, brackets convert a negative to exact and quotes convert to phrase. Pasting raw rows lets these symbols silently break the intended match type. Clean to plain text (Notepad round-trip) before bulk-pasting; verify match-type via the UI's pencil icon.

**Sources:** Solutions 8 — claim 8 · Loves Data — cluster C33 · KeyCommerce — cluster C33


---

### Q?: How do you tell whether a campaign is suffering from too few negatives (wasting spend) vs. too many (starving reach and Smart Bidding signal)?
**Confidence:** Confirmed

Too few signals: high % of search-terms-report queries you'd visibly mark irrelevant; CPA above target with budget pacing fast on junk; n-gram analysis flags root words like 'jobs' or 'free' driving 10%+ of spend with no conversion. Too many signals: impression share lost to negatives rising in the report; conversion volume falls after a list change; Smart Bidding 'limited by data' messaging if you're below 50 conv/mo. The honest tell: run an n-gram on the last 60 days — if irrelevant root words drive material spend, you're under-blocking; if conversions dropped right after a list change, you're over-blocking.

**Sources:** Aaron Young / Mancini — cluster C32 · Daryl Mander — claim 36 · Heath / Schaefer n-gram practice


---

### Q?: What signals in the search-terms report tell you a negative list is overdue for an audit?
**Confidence:** Confirmed

Audit when: (1) you can find more than 5–10 obviously-irrelevant high-spend terms in the top of the report, (2) a single root word (free, jobs, used, DIY) appears 5+ times, (3) the campaign has scaled or expanded services since last audit, (4) it's been 30+ days for active accounts or 90+ days for low-spend, (5) impression-share-lost has risen, OR (6) the 'added/excluded' column shows few flagged exclusions. Per Mancini, on first review change date range to 'All time'; subsequent reviews scope to incremental periods.

**Sources:** Mike Mancini — claim 96 · Aaron Young — claim 160 · Ben Heath — claim 21


---

### Q?: How do you confirm a negative is actually blocking what you intended after you add it?
**Confidence:** Confirmed

Use the search-terms report's 'Added/Excluded' column — when a query is blocked by your negative, the row shows a green check with 'Excluded.' Per Grow My Ads and TMMI, the audit-friendly trick is to add the term as exact AND the broader root as broad/phrase; the exact-match version makes the search-terms-report row visibly flag the term as excluded so you have a paper trail. Verify after 24–48 hours of new traffic.

**Sources:** Grow My Ads — claim 72 (added/excluded column) · TMMI — claim 221


---

### Q?: If conversions drop right after a negative-list update, what's the systematic way to isolate whether the negatives caused it?
**Confidence:** Plausible

(1) Pull the change history (Tools > Change history) and confirm only negatives were modified in the window. (2) Check impression share lost to negatives — did it spike? (3) Search the search-terms report for the now-blocked terms over the same prior window — were any of them converting? (4) If they were, remove or adjust those specific negatives, not the whole list. Aaron Young's discipline: keep budget/structure changes <20% per cycle so attribution-on-changes is clean. Don't roll back the whole list — surgically reverse the suspect terms.

**Sources:** Aaron Young — claim 167 · Cluster C29 audit practices


---

### Q?: How do you handle the trade-off between negative keyword precision and reach loss?
**Confidence:** Confirmed

Default posture depends on goal: efficiency-oriented accounts start tight and loosen; growth/awareness accounts start loose. Heath's two-layer review balances this — pass 1 negates clearly irrelevant intent terms (no reach risk), pass 2 negates by data (reach risk traded for proven efficiency). For Smart-Bidding accounts above 50 conv/mo, Mander's frame applies: negatives strip signal, lower-precision wins. For everything else, modest precision wins because you can't afford to feed junk.

**Sources:** Ben Heath — claims 185, 283 · Darren Taylor — claim 269 · Daryl Mander — claim 38


---

### Q?: What's the trade-off between a tight pre-launch negative list and giving Smart Bidding enough data to learn?
**Confidence:** Confirmed

If the account will hit 50+ conv/mo quickly, lean lighter pre-launch — let Smart Bidding see the variance and learn. If the account will be slow to reach signal threshold (small budget, lead-gen with offline close, B2B), tight pre-launch lists are correct because the algorithm won't learn fast enough to filter junk on its own. Per Mander's exception 1, accounts under 50 conv/mo need manual negatives; per Heath's standard practice, most SMB accounts fall in this bucket.

**Sources:** Daryl Mander — claim 39 · Ben Heath — cluster C13


---

### Q?: When is it better to use SKAGs/themed ad groups with tight negatives vs. broader ad groups with looser negatives?
**Confidence:** Plausible

Themed ad groups with tight cross-group negatives are right when (a) you need ad-copy-to-query alignment for QS, (b) you're funneling location or product variants between groups (Solutions 8's geo-funnel model), or (c) sub-products have meaningfully different LP/offer needs. Broader ad groups with loose negatives are right under modern broad-match + Smart Bidding when signal is high enough that the algorithm separates intents internally. Heath's pre-launch Keyword Planner workflow runs once per main term per ad group — implying themed ad groups are still the default for most accounts.

**Sources:** Solutions 8 — claim 7 (geo funneling) · Ben Heath — claim 24


---

### Q?: How do negative keywords behave in Performance Max compared to Search, and what are the current limits and workarounds?
**Confidence:** Confirmed

PMax exposes a Negative Keywords tab and a search-terms report; account-level negatives propagate to PMax campaigns. STATUS UPDATE (2025): the previous 'shared lists CANNOT attach to PMax' limitation has been LIFTED — per Search Engine Land and PPC News Feed, Google completed the rollout of shared negative-keyword lists for Performance Max by August 7, 2025, and raised the per-campaign cap to 10,000 negatives in March 2025 (up from 100). PMax also still offers Brand Exclusions as a separate surface (more comprehensive than negatives — covers misspellings and subsidiary brands). Inventory caveat: PMax negative keywords only apply to Search and Shopping inventory — NOT YouTube, Display, Discover, or Gmail.

**Sources:** Google Ads Help — account-level negatives doc (claim 131 verified) · Cluster C12 practitioner consensus


---

### Q?: How should you handle negative keywords on Shopping campaigns where you can't use positive keywords?
**Confidence:** Plausible

Negatives are the primary query-control lever for Shopping — the campaign matches off product feed attributes, so negatives are how you exclude irrelevant intent. Add comprehensive pre-launch negatives (Mancini-style intent buckets — free, cheap, used, DIY, jobs); ongoing review is non-optional because feed-driven matching pulls in adjacent queries. Per cluster C5, even Smart-Bidding contrarians concede negatives matter for new Shopping launches before signal accrues.

**Sources:** KeyCommerce / cluster C12 consensus · Cluster C5 (Mander exception)


---

### Q?: How do non-English campaigns, accents, and special characters change negative keyword behavior?
**Confidence:** Plausible

Sparsely covered in the corpus — Mancini notes ampersand and special-character handling for competitor brands (e.g., 'P & S' vs 'P&S' must both be added). Beyond that, treat each accented variant and language-specific symbol as its own literal negative; Google's lack of close-variant expansion on negatives makes language hygiene more important, not less. The field doesn't have a documented playbook in the corpus.

**Sources:** Mike Mancini — claim 95


---

### Q?: How do negatives interact with DSA (Dynamic Search Ads) and broad-match keywords with Smart Bidding?
**Confidence:** Plausible

DSA and broad-match-with-Smart-Bidding both rely on Google's expansive matching, which is exactly the surface where negatives prevent collateral. Per Heath, broad match makes negatives 'particularly important' because the surfaced searches are likely less relevant. Mander's contrarian frame applies here too — if Smart Bidding has full signal, it can re-bid junk down to near-zero — but practitioners on the corpus recommend keeping negatives active for DSA/broad to prevent QS damage and reputational/brand mismatch. The corpus does not have a DSA-specific playbook.

**Sources:** Ben Heath — claim 14 · Daryl Mander — claim 38


---

### Q?: What's the practical limit on negatives per list/campaign, and how do you operate when you hit it?
**Confidence:** Verified

Google's documented limits: 1,000 negatives per account-level list (verified via Google's own help doc), 5,000 per shared list, 20 shared lists max per account. Heath's agency runs 523k+ aggregate negatives across clients (anecdotal but plausible). When you hit a cap: triage by impact (n-gram on actual blocked spend), retire low-impact negatives, push the rest to campaign-level on individual campaigns. Mancini's 2,300-term curated list lives at campaign level for that reason.

**Sources:** Google Ads Help — account negatives doc (claim 131 verified) · Ammar — claim 131 · Ben Heath — claim 276


---

### Q?: Which Google Ads UI views, scripts, or third-party tools do practitioners actually use to mine and apply negatives at scale?
**Confidence:** Confirmed

Standard stack: (1) Search-terms report (Campaign > Keywords > Search terms) — primary mining surface. (2) Keyword Planner Discover-new-keywords + Refine-keywords — pre-launch. (3) Tools > Shared Library > Exclusion Lists — shared lists. (4) Admin > Settings > Negative keywords — account-level. (5) N-gram scripts: Brainlabs, Shabba, Nils Rooijmans, Ayima — free, run in ~1 minute on thousands of terms. (6) Third-party: Optimizer, Adevolver. (7) AI tools: Stew Schaefer's Gemini agent (BYO-key), Grow My Ads' Claude skill + Project, Claude Code + Google Ads API. (8) Google Ads MCP for Claude Code as alternative to API.

**Sources:** Multi-source cluster C17 (n-gram tools, claim 237 verified) · Grow My Ads — claims 294, 299 · Stew Schaefer — claim 305


---

### Q?: How do you build or use an n-gram analysis to find negative candidates the search-terms report alone misses?
**Confidence:** Confirmed

N-gram analysis aggregates 1-, 2-, and 3-word fragments from the search-terms report so root-word patterns surface that scrolling misses (e.g., 'free' appearing across 47 different long-tail queries). Free public scripts: Brainlabs, Shabba, Ayima, WordStream — install via Tools > Scripts, run on the search-terms feed, get a sorted output of root tokens by spend/clicks/conversions. Per Schaefer, batch the analysis by ad-group or campaign for cleaner signal. Aaron Young pairs n-gram with budget reallocation to act on the findings.

**Sources:** Shabba.io / WordStream / Ayima / Brainlabs (claim 237 verified) · Aaron Young — claim 176


---

### Q?: What's the right way to use AI/LLMs (ChatGPT, Gemini, scripts) to suggest negative keywords without trusting them blindly?
**Confidence:** Confirmed

Three-tier ladder (per Grow My Ads): (1) drop CSV into Claude chat with goals (target ROAS, conversion rate, what you sell) — fine for one-off; (2) Claude Project + skill file per client, one-command repeatable; (3) Claude Code + Google Ads API or MCP, fastest, no manual export. Schaefer's parallel architecture: bring-your-own-key Gemini agent, batches of ~120 terms, classifies as definite-waste / likely-waste / monitor / optimal with confidence stars; rationale combines product-fit AND CPC-vs-account-average. Universal discipline: human review before push (Grow My Ads: 'I still manually review all of this before I would add it'); route ambiguous terms to a monitor bucket rather than auto-negating; AI false-positives have killed real customer avatars (Home Reserve RV).

**Sources:** Grow My Ads — claims 291–302 · Stew Schaefer — claims 305, 317, 318 · Cluster C19 human-in-the-loop consensus


---

### Q?: How do you bulk-edit, version, and roll back negatives using Google Ads Editor or the API?
**Confidence:** Plausible

Bulk-add via UI: Negative Keywords > '+' > paste from Notepad > Save (Mancini). For larger ops, Google Ads Editor lets you bulk-add and review before push. For programmatic: Google Ads API (Grow My Ads' direct integration) or Google Ads MCP (alternative — uses more tokens, less clean). Versioning is weak natively — use Tools > Change history or export to a CSV before each batch as your rollback. Rollback strategy: surgical reversal of the suspect terms only, not the whole list.

**Sources:** Mike Mancini — claim 100 (UI bulk paste) · Grow My Ads — claims 299, 300


---

### Q?: How do you measure the actual financial impact of a negative keyword you added?
**Confidence:** Confirmed

Three-metric measurement: (1) Tag the change with date in change history, (2) compare cost-per-conversion / ROAS for the campaign for the 14–28 days before vs. after, (3) check spend that would have gone to the now-blocked term using the prior search-terms-report data. Mancini's case: $1,500/mo × 75% wasted × 12 months = $13,500 saved. Heath's claim of 30–50% budget recovery is corroborated by Stackmatix and OptMyzr (verified). Don't try to attribute incremental conversions to a single negative — measure at the campaign level.

**Sources:** Stackmatix / OptMyzr — claim 178 verified at 30-50% · Mike Mancini — claim 101 · Aaron Young — claim 176


---

### Q?: What metric tells you a negative is over-blocking — impression-share lost to negatives, conversion drop, or something else?
**Confidence:** Plausible

Impression-share-lost-to-negatives is the cleanest direct metric: rising = blocking more, sometimes too much. Pair with conversion-volume change after the list update (drop within 14 days = suspect) and an audit of the search-terms 'Excluded' rows for any that look on-brand. Mander's frame: under mature Smart Bidding, if you're blocking terms whose intent variance the algorithm could re-bid, you're over-blocking by definition. The honest tell: your conversion volume drops disproportionately to your impression drop after the list change.

**Sources:** Daryl Mander — claim 36 · Cluster C25 over-blocking war stories


---

### Q?: How do you attribute conversion lift (or drop) to a negative-list change vs. concurrent bid, audience, or creative changes?
**Confidence:** Plausible

Per Aaron Young's discipline: keep all changes <20% per cycle and stagger them so each change has a clean attribution window. If multiple changes ship together, the only honest answer is 'we can't cleanly isolate' — which is why agencies treat negatives as their own change cycle. For high-stakes attribution, use Google Ads' draft-and-experiment surface to A/B the negative-list version against the baseline.

**Sources:** Aaron Young — claim 167


---

### Q?: How has Google's removal/loss of search-terms report visibility (the 'Other' bucket) changed how you mine negatives?
**Confidence:** Confirmed

Per Search Engine Land (verified primary source), 20–80% of search-term data is now hidden from advertisers, with ~40% as the documented average. Darren Taylor cites 80% redaction on some clients — the upper extreme. Practical adaptations: (1) lean harder on n-gram analysis on the visible queries to extrapolate intent themes; (2) supplement with Keyword Planner pre-emptive lists; (3) use AI/LLM mining on whatever IS visible — Gemini and Claude can extrapolate intent patterns from limited data better than manual review.

**Sources:** Search Engine Land — claim 262 verified · Darren Taylor — claim 262


---

### Q?: What's changed in the last 12-24 months with PMax brand exclusions, account-level negatives in PMax, and campaign-level PMax negatives?
**Confidence:** Confirmed

PMax now exposes (1) a Negative Keywords tab at campaign level (cap raised to 10,000 per campaign in March 2025, up from 100), (2) a search-terms report (limited), (3) brand exclusions as a separate surface. Account-level negatives propagate to PMax (1,000-keyword cap). MAJOR 2025 CHANGE: shared negative-keyword lists CAN now attach to PMax campaigns — rollout completed Aug 7 2025 per PPC News Feed and Search Engine Land. Brand exclusions also began upgrading into AI Max for Search starting May 27 2025. Inventory caveat: PMax negatives only block Search and Shopping inventory, NOT YouTube/Display/Discover/Gmail.

**Sources:** Cluster C12 — multi-source consensus · Google Ads Help — claim 131 verified


---

### Q?: How has the broad-match push and Smart Bidding's evolution shifted the role of negative keywords in 2024-2025?
**Confidence:** Disputed

Two camps. Aggressive-NK (Heath, Mancini, Grow My Ads, Schaefer): broad-match drift makes negatives MORE important year-over-year — exact does the work of phrase, phrase of broad, broad of everything (Ammar). Smart-Bidding contrarian (Mander, Taylor): under mature Smart Bidding with full purchase data and 50+ conv/mo, negatives strip the algorithm's signal — 'every manual negative is the human overriding the algorithm.' Both are right inside their bounding box; the contrarian frame requires all four conditions (Smart Bidding + 50–100 conv/mo + actual revenue tracking + direct online e-comm). Most accounts in the wild fail at least one, so aggressive-NK remains the default posture.

**Sources:** Daryl Mander — claims 33–37 · Ammar — claim 127 · Ben Heath — claim 14 · Cluster C5 (Mander's exceptions)


---

### Q?: Is the future of negative keywords automated NK mining via AI, or human-curated lists, or hybrid? Where does the field stand right now?
**Confidence:** Confirmed

Hybrid is the current state. Both Schaefer (Gemini agent) and Grow My Ads (Claude skill) ship AI-assisted mining but neither auto-pushes — Schaefer routes ambiguous terms to a 'monitor' bucket; Grow My Ads' Mike: 'I still manually review all of this before I would add it.' Per Grow My Ads, NK work is a 'strong fit' for AI because it's mundane, repetitive, rule/logic-driven. The trajectory is more autonomy as confidence-scoring improves; the dominant pattern in 2026 is AI-classify, human-approve, programmatic-push.

**Sources:** Grow My Ads — claim 302 (manual review) · Stew Schaefer — claim 318 (monitor bucket) · Grow My Ads — claim 303 (AI fit)


---

### Q?: Are 'mega negative lists' (5,000+ pre-built terms) still defensible, or are they actively harmful with modern Smart Bidding?
**Confidence:** Disputed

Defensible when the list was built from real search-term data and is per-term reviewed against the specific business; harmful when pasted from a generic 'mega list' as assumption-based blocking. Mancini's 2,300-term list is curated over 9 years from real campaigns. Mander's contrarian frame correctly calls out unreviewed pasting as antipattern. Solutions 8's 400-term Paid Insights list with 'hire' in it is the canonical bad case. Heath's 523k-aggregate-negatives across an agency demonstrates large lists CAN be correct when built from real data. The size question is a red herring — the real question is provenance.

**Sources:** Mike Mancini — claims 91, 98 · Daryl Mander — claim 43 · Solutions 8 — claim 10 · Ben Heath — claim 276


---

### Q?: How should negative keyword strategy change if and when Google further restricts query data or fully ML-controls match?
**Confidence:** Plausible

Strategy bifurcates. (a) Inside the C5 box (Smart Bidding + signal), increasingly defer to the algorithm — manual negatives become low-leverage. (b) Outside the C5 box, lean harder on n-gram analysis of whatever query data IS visible, AI-classification for pattern extrapolation, and pre-emptive lists from Keyword Planner before launch. Brand-protection, legal, and adult-language negatives remain non-negotiable regardless. The corpus does not have a documented playbook for the post-redaction future — it's emergent.

**Sources:** Cluster C27 (singleton — Taylor) · Cluster C5


---

### Q?: When campaigns share themes but target different funnels (TOFU vs. BOFU), how should negative lists differ between them?
**Confidence:** Plausible

TOFU campaigns can tolerate broader query mix because awareness/consideration intent is the goal; BOFU campaigns need tighter blocking because intent-mismatch wastes high-CPC slots. Practical: (1) keep universal junk-intent negatives on both; (2) put research-intent terms ('how to', 'tutorial', 'what is', 'reviews') as BOFU-only negatives; (3) put price-shopper terms ('cheap', 'free', 'discount') as TOFU+BOFU negatives unless a discount IS the offer. Per Schaefer's premium-bunk-bed case, even 'bed' as too-generic gets negated for premium positioning regardless of funnel.

**Sources:** Stew Schaefer — claim 315 · Cluster C26 audience-sculpting consensus


---

### Q?: How should you handle negatives differently for lead-gen vs. e-commerce accounts?
**Confidence:** Confirmed

Lead-gen sits squarely in Mander's exception 2 — Google can't see the final $ unless you import offline conversions. Manual negatives are HIGHER value than e-commerce because the algorithm is signal-starved. Common lead-gen negatives: 'jobs', 'careers', 'how to do it yourself', research-intent terms, competitor names, free-version intent. E-commerce with full purchase tracking and 50+ conv/mo can lean lighter on negatives and trust Smart Bidding more. Schaefer's framework is niche-agnostic but his rationale shifts toward product/brand-fit for e-comm and intent-mismatch for lead-gen.

**Sources:** Daryl Mander — claims 38–41 · Stew Schaefer — claim 322


---

### Q?: What's the right approach when a search term is high-volume but only sometimes relevant — negative it, sculpt with bid adjustments, or new ad group?
**Confidence:** Plausible

Decision tree: (a) if the term has clearly distinct intent variants you can separate by query phrasing → split into a new ad group with tailored copy and tight negatives between groups (Solutions 8's geo-funnel pattern). (b) If the variants are intent-detectable by Google's signals (purchase history, location, etc.) → leave to Smart Bidding to bid them differently (Mander's frame). (c) If the term is too generic to reliably separate AND your offer is premium-niche → negate it entirely even at below-average CPC (Schaefer's 'bed' for a premium furniture brand). Don't reach for bid adjustments first — they're a weaker lever than ad-group structure or negatives.

**Sources:** Stew Schaefer — claim 315 · Solutions 8 — claim 7 · Daryl Mander — claim 34


---

### Q?: How do you onboard a new account with a years-old, unmaintained negative list — keep, prune, or rebuild?
**Confidence:** Plausible

Prune, don't rebuild. Steps: (1) export every negative across account/campaign/ad-group/shared-list to a CSV, (2) flag any that contain brand or product names (often stale after expansion — Ammar's case), (3) for each non-brand term, check the search-terms report for the last 90 days to see if it's still triggering — if it never appears in the report and never blocks anything, delete it as dead weight, (4) re-add a fresh layer mined from current search-terms data. Don't nuke the list — there's hard-won learning embedded; just remove the parts that block current services and confirm the rest by data.

**Sources:** Ammar — claim 132 (stale account-level) · Solutions 8 — claim 10 (review every term)


---

### Q?: When should a multi-location business use cross-location geo-negatives to sculpt traffic between location-specific campaigns rather than relying on Google's geo-targeting alone?
**Confidence:** Plausible

Use cross-location geo-negatives when your campaign structure has separate campaigns per location and queries explicitly include the OTHER location's name. Per Solutions 8: a north-side campaign should have 'south' as a negative, and vice versa, to funnel queries to the right location. Google's geo-targeting only filters by physical location — not by query content — so 'plumber san antonio south' served from a north-side campaign still routes wrong without geo-negatives. Pair with pre-emptive out-of-area negatives (Taylor) for towns you don't serve at all.

**Sources:** Solutions 8 — claim 7 · Darren Taylor — claim 264


---

### Q?: How do you safely use a published pre-built 'starter' negative list (Paid Insights, Klientboost, etc.) without inheriting its bad assumptions for your business?
**Confidence:** Confirmed

Per Solutions 8's hard-learned lesson with the 400-term Paid Insights list: don't paste, review per-term against the offer first. Workflow: (1) load the list into a spreadsheet, (2) flag any term that intersects your offer (e.g., 'hire' for an agency, 'free' for a freemium SaaS), (3) categorize the rest into themes you actually want to block, (4) start with the highest-confidence categories and watch the search-terms report for 14 days before adding the next batch. The starter list is a generator of candidates, not a final list.

**Sources:** Solutions 8 — claim 10


---

### Q?: Why does Google's UI default negative match type differ across surfaces (exact from search-terms report, broad from the negative-keywords tool, user-chosen from Keyword Planner), and which of those defaults is actually right for the typical use case?
**Confidence:** Confirmed

Per Heath, the defaults are: exact when adding from the search-terms report, broad when adding from the standalone negative-keywords tool, user-chosen from Keyword Planner. TMMI calls the search-terms-default 'deliberate revenue protection' — exact excludes the fewest possible terms, so Google still gets to monetize variants. None of those defaults is 'right' for the typical case: the right answer is phrase for multi-word, broad for single-word junk. Always override the default explicitly.

**Sources:** Ben Heath — claim 25 · TMMI — claim 134


---

### Q?: When mining negatives from the search-terms report, should you add the full phrase as exact-match AND component words as broad-match negatives, or does that double-up cause unintended blocking?
**Confidence:** Confirmed

Yes — Heath, TMMI, Grow My Ads all teach the pair-add: exact-match for the offending full phrase + broad/phrase for the offending root word. The pair gives you (a) a clean audit trail in the search-terms 'Excluded' column from the exact, AND (b) breadth from the root-word broad-match. The 'unintended blocking' risk is contained because the broad-match-negative still requires the root word to appear in the query. The trap is only when the root word is itself ambiguous (e.g., 'free' for a freemium offer) — in that case, drop the broad and keep only the surgical exact.

**Sources:** Ben Heath — claims 19, 20 · TMMI — claims 220, 221


---

### Q?: How do you efficiently triage hundreds of Keyword Planner suggestions (e.g., 486 ideas) into negative candidates without spending hours per ad group?
**Confidence:** Plausible

Per Heath: (1) export the full list to spreadsheet, (2) use Refine-keywords filters (brand vs. non-brand, service categories) to bucket aggressively, (3) flag obvious irrelevant categories first — competitor brands you don't carry, services you don't offer, geography you don't serve, (4) skip ambiguous mid-tier — don't try to be perfect on first pass. For LLM-assisted triage: drop the CSV into Claude with goals + offer description and ask for irrelevant-category extraction. Schaefer's Gemini agent does the same on search-terms data; Keyword Planner data is similar enough to feed the same workflow.

**Sources:** Ben Heath — claims 22–24 · Grow My Ads — claim 291


---

### Q?: What is the actual dollar threshold of owner-time value at which manually mining negatives stops being net-positive?
**Confidence:** Plausible

Not addressed directly in the corpus. Mander frames the question economically: 'opportunity cost is massive' for an owner managing the account vs. higher-leverage business work. Mander's heuristic: if you have someone whose time is less valuable, they can do it sparingly and data-backed. The threshold depends on (a) account spend, (b) percent of spend currently wasted, and (c) owner hourly value — back-of-envelope: if 1 hour of work yields 30–50% recovery on a 10–20% wasted slice of monthly budget, payback at $X/mo spend is roughly $0.05X to $0.10X per hour. For a $5k/mo account that's $250-500/hr first-iteration ROI, decaying with each subsequent pass.

**Sources:** Daryl Mander — claim 29 · Cluster C32 budget waste range


---

### Q?: How do you tell whether your account has crossed from 'Smart Bidding has enough signal' to 'Smart Bidding is starving' beyond the 50–100 conversions/month rule of thumb?
**Confidence:** Plausible

Beyond the 50–100/mo rule (Mander), look for: (a) Smart Bidding showing 'limited by data' or 'still learning' messaging in the campaign panel, (b) high CPA volatility week-over-week in stable campaigns, (c) flat performance after a learning-phase reset, (d) conversion delay > 14 days (Google can't close the loop in time), (e) lead-gen with offline-only deal closure. The corpus does not have a more precise quantitative test — Google doesn't publish the exact threshold.

**Sources:** Daryl Mander — claim 38 · Cluster C5


---

### Q?: If Smart Bidding can already segment a query into high- and low-intent users and bid them separately, when (if ever) does adding a negative keyword strictly Pareto-improve performance?
**Confidence:** Plausible

Pareto improvement happens when the negative blocks a query that NO user-segment within it would convert profitably for your business. Cases: (1) brand protection — your competitor's customers calling you to complain (Mancini's home-services case); (2) categorical product mismatch — 'leather sofa' for a brand that sells only fabric; (3) job-size mismatch where even high-intent users wouldn't generate enough revenue (Mancini's '8-foot fence' for a contractor doing 100+ feet); (4) legal/adult content protection. For 'fuzzy intent' queries where SOME segment converts profitably even at low CPC, Mander's frame says don't negate — let the algorithm bid them down.

**Sources:** Daryl Mander — claim 35 (no keyword that doesn't work) · Mike Mancini — claims 93, 97


---

### Q?: For lead-gen and B2B accounts, what's the right way to feed offline conversion data back to Google Ads so that the 'manual negatives' phase can shrink?
**Confidence:** Plausible

The corpus identifies the principle (offline conversion import shrinks Mander's exception-2 territory) but does not provide a step-by-step workflow. Standard Google Ads features: Offline Conversion Imports via CSV, Enhanced Conversions for Leads, GCLID-stitching from CRM. Once Google sees closed-deal value, Smart Bidding can re-bid by lead quality. Until then, manual negatives stay high-leverage. This is an explicit gap — the corpus' practitioners discuss the consequence but not the implementation.

**Sources:** Daryl Mander — claim 40 (Google can't see real money)


---

### Q?: Inside the 'no such thing as a keyword that doesn't work' frame, are there any classes of search term that are still strict negatives even with Smart Bidding (e.g. brand-protection, legal, adult)?
**Confidence:** Plausible

Yes — even Mander's frame has hard exclusions. (a) Brand protection (your own brand on non-brand campaigns; competitor brands you can't honestly serve). (b) Legal/regulatory — terms whose presence would be a compliance violation. (c) Adult/swearing — Mancini's 90-term swearing list applies even to innocuous service businesses because users include profanity in queries. (d) Categorical product/service mismatch (fabric brand getting 'leather' queries). These are non-bid-able regardless of Smart Bidding signal.

**Sources:** Mike Mancini — claims 93, 99, 102 · Cluster C25


---

### Q?: Should you mirror every phrase/broad negative with its exact-match version just so the search-terms report flags the query as 'excluded'?
**Confidence:** Plausible

Yes, when audit-trail visibility matters more than economy of list size. Per Grow My Ads and TMMI, the exact-match mirror creates the visible 'Excluded' flag in the search-terms report so you have a paper trail for which rule fired. Cost: list-size pressure if you do it for every term. Compromise: mirror only the high-value or high-spend exclusions; let the rest live as broad/phrase only.

**Sources:** Grow My Ads — claim 72 · TMMI — claim 221


---

### Q?: When a search term has homonym intent (e.g., 'license' = licensure vs. 'licensed' = qualification), how do you decide between exact-only negativing and writing it off entirely?
**Confidence:** Plausible

Exact-only when one variant is high-value and you can name it specifically; write off entirely when intents overlap so much the algorithm can't separate them with low spend per click. Schaefer's monitor-bucket pattern is the right framing: when in doubt, route to human review and watch the term for 14–30 days before deciding. The corpus does not provide a homonym-specific framework but the pattern is consistent: surgical exact-negative for the bad-intent variant, leave the good-intent form live.

**Sources:** Stew Schaefer — claim 317


---

### Q?: How should agencies structure their standing monthly negative-keyword research SOP — what tools/cadence/sign-offs does it require to scale?
**Confidence:** Plausible

Cadence: weekly for active, monthly for low-spend (per Heath, Ammar). Tools: search-terms report + n-gram script + LLM classifier (per Aaron Young, Schaefer, Grow My Ads). Sign-off: per Grow My Ads' Claude-skill workflow, the AI proposes, the human reviews, the senior account manager approves before push. The SOP itself can BE a Claude skill (Grow My Ads pattern) — codify thresholds, categories (universal junk, competitor, out-of-area, support, informational, wrong-product), client-specific goals (target ROAS, conversion rate), and the human-review gates.

**Sources:** Grow My Ads — claims 293, 294, 302 · Aaron Young — cluster C45


---

### Q?: Is inverting Keyword Planner's brand/non-brand 'refine keywords' filter a reliable way to seed pre-launch competitor negative lists?
**Confidence:** Plausible

Yes — Heath's pre-launch workflow specifically uses Refine-keywords' brand filter to surface competitor brand names cheaply. Filter to brand suggestions, harvest the names you don't sell, add as negatives. Then filter to non-brand and skim for irrelevant categories (DIY tutorials, jobs, etc.). The technique is reliable because Keyword Planner's data is the same source Google uses for matching, so terms that show up there are likely to trigger your campaign.

**Sources:** Ben Heath — claim 23 (singleton)


---

### Q?: What does the 'Added/Excluded' column with the green check mark in the Search Terms report actually indicate, and how do you use it as a triage filter?
**Confidence:** Plausible

The green check in the Added/Excluded column flags rows where the query is currently being excluded by one of your negatives — i.e., the negative is firing. Use it as a triage filter to (a) verify a recent add is doing its job, (b) audit for over-blocking by sorting the Excluded rows and scanning for any that look like converting traffic, (c) confirm coverage when running an account audit. Per Grow My Ads, the column is one of the cleanest signals you have for negative-list correctness.

**Sources:** Grow My Ads — claim 72


---

### Q?: What is the exact bracket/quote/bare-term syntax for switching a negative between exact, phrase, and broad match in the Google Ads UI input field?
**Confidence:** Plausible

Per Loves Data and KeyCommerce: bare term (no wrapping) = broad match; quoted term "like this" = phrase match; bracketed term [like this] = exact match. Same syntax as positive keywords. The trap: positive-style + modifiers don't behave the same way on negatives (Solutions 8). Always confirm match type via the pencil-edit icon after adding.

**Sources:** Loves Data — cluster C33 · Solutions 8 — claim 8


---

### Q?: Why does Performance Max's Keywords view auto-land on the Negative Keywords tab, and what does that imply about how PMax exposes keyword controls?
**Confidence:** Confirmed

Because PMax has no positive-keyword targeting (it's audience+asset+signals driven), the only keyword-shaped lever is the negative tab — so the UI lands you there. This implies Google designed PMax to give you exclusion-only control over query traffic. Combined with the limitation that shared lists can't attach to PMax, the practical surface is account-level negatives + per-campaign negatives + brand exclusions.

**Sources:** Cluster C12 multi-source consensus · Google Ads Help — account-level negatives doc (verified)


---

### Q?: Should home-services advertisers add 'job-size mismatch' negatives (e.g., 'eight-foot', '100-foot roll', 'small repair') to filter out work below their minimum job size?
**Confidence:** Confirmed

Yes — Mancini's fencing case is the canonical example: 'eight-foot chain link fence' is too small for a contractor doing 100+ feet; '100-foot roll' implies retail purchase, not install. Adding these protects sales-team time as much as ad spend. Pair with intent-mismatch filtering (residential-only contractor blocking 'commercial', tile-only blocking 'wallpaper'). The job-size dimension applies broadly to home services and B2B with clear minimum-deal thresholds.

**Sources:** Mike Mancini — claim 97 (fencing case)


---

### Q?: When mining competitor names from the local Map Pack, how deep do you go before duplication makes additional pages worthless?
**Confidence:** Plausible

Per Mancini, ~3 pages of Map Pack results — beyond that the same competitors duplicate and you get diminishing returns. Combine with related-search and autocomplete suggestions (Max, TMMI) for additional cheap discovery. Tokenize each competitor name (singular/plural/partial/ampersand variants) before adding as negatives.

**Sources:** Mike Mancini — claim 94


---

### Q?: How should you handle competitor brand variants — singular/plural, partial tokens, and ampersand spacing — to make sure a single negative actually blocks all forms?
**Confidence:** Confirmed

Per Mancini's tokenization rule: for every competitor brand, add (a) singular and plural ('Dean', 'Dean's'), (b) partial tokens ('Roto', 'Rooter' for Roto-Rooter — each as standalone broad-match negatives), (c) both spaced and unspaced ampersand forms ('P & S', 'P&S'). Negatives don't auto-handle these variants (Google docs verified). The exception: avoid common-name partial tokens like 'Lauren' as broad — they block too much.

**Sources:** Mike Mancini — claim 95 · Google Ads Help — claim 63 verified (negatives don't expand)


---

### Q?: What's the right cadence for re-running search-terms-report negative mining — full history on first pass, then weekly/monthly increments?
**Confidence:** Confirmed

Per Mancini: 'All time' on first review, then incremental periods (e.g., 'last month' or last 7 days) afterward. Schaefer's tool uses last-7-day default exports. The full-history first pass surfaces patterns that weekly runs miss. After the cleanup pass, weekly increments catch the new junk that broad-match drift introduces.

**Sources:** Mike Mancini — claim 96 · Stew Schaefer — claim 312


---

### Q?: Why does conquesting competitor brand traffic disproportionately attract their existing customers (with service complaints) in home services, and is this a vertical-specific phenomenon?
**Confidence:** Plausible

Per Mancini: home-services callers searching a competitor's brand name often ARE that competitor's existing customers — they're calling for service complaints, appointment changes, or technician ETAs, not new appointments. Vertical-specific: yes, home services is the canonical case because service relationships generate ongoing customer-service needs the competitor can fail at. Pattern likely repeats in any service business with maintenance/recurring contact (home warranty, alarm monitoring, ISP), less so in pure-purchase verticals like e-comm.

**Sources:** Mike Mancini — claim 93 (singleton, vertical-specific)


---

### Q?: What's the practical spend threshold (multiple of target CPA, time window) before you negative a non-converting search term?
**Confidence:** Confirmed

Common practitioner rule: ~1–1.5x target CPA spent without conversion at 60+ days, with at least a few clicks. Aaron Young allows up to ~10% of spend as wider tolerance. Schaefer's pre-filter is 1+ click OR 30+ impressions. Darren Taylor warns against acting too early. The honest framing: clicks > impressions, give 14 days for attribution, scale to CPA. For high-CPC/low-volume terms, accept longer learning windows.

**Sources:** Cluster C16 multi-source consensus · Aaron Young — claim 167


---

### Q?: How should you wait for conversion attribution before negativing a high-spend term?
**Confidence:** Plausible

Per Aaron Young: ~2 weeks minimum for attribution windows to close. For longer-cycle conversions (lead-gen, B2B, considered purchases), extend proportionally — wait at least one full sales cycle. The risk of acting before attribution: you kill a term that DID convert, you just hadn't seen it yet.

**Sources:** Aaron Young — claim 167 · Cluster C16


---

### Q?: How does the messy-middle 'second-choice brand' research influence whether you should bid on or negative competitor brand terms?
**Confidence:** Disputed

Less than Max claims. Per Think with Google's primary source (verified): the actual figure is 28% (not Max's 30%) and required FULL behavioural-supercharging — five-star reviews + 20% extra-free offer — not 'simply giving the option to choose.' So the messy-middle does support competitor-brand visibility, but only when you have premium social proof and a real value-add at the moment of choice. For most accounts without that supercharging, the cost-per-conversion math still favors blocking.

**Sources:** Think with Google — Decoding Decisions (claim 124 contradicted) · Max | Google Ads Nerd — claim 124 (overstated)


---

### Q?: How do you decide between adding a single negative keyword as broad-match vs. campaign-level vs. account-level when the same term should never run anywhere in the account?
**Confidence:** Plausible

If 'never anywhere in the account' is genuinely true and the term doesn't touch brand → account-level (Solutions 8 default). If it's brand-adjacent or any risk of stale-blocking new services → use campaign-level shared list and apply to all current campaigns; review on schedule. The match-type question is separate: broad for single junk words, phrase for multi-word phrases. Account-level + broad-match for a single junk word like 'jobs' is the canonical correct answer.

**Sources:** Solutions 8 — claim 12 · KeyCommerce / Ammar — cluster C29


---

### Q?: When you broad-match-negative a competitor's first name only (e.g., 'Lauren'), how do you avoid blocking unrelated queries containing that common name?
**Confidence:** Plausible

Don't broad-match common names alone. Use phrase or exact, e.g., "Lauren plumbing" or [Lauren plumbing co]. If the competitor's full name is multi-token, prefer the most-distinctive token (their last name or a unique combination) for any broad-match treatment. Per Mancini's tokenization rule, also add the unique combinations rather than the common ones.

**Sources:** Mike Mancini — claim 95 · Cluster C25 over-blocking war stories


---

### Q?: When mining negatives from the search-terms report inside an ad group, when should you push the negative up to campaign level or the shared list instead of leaving it at ad-group?
**Confidence:** Confirmed

Push up when (a) the term is irrelevant to all ad groups in this campaign — campaign-level; (b) the term is irrelevant to multiple campaigns — shared list; (c) the term is universally never wanted — account-level. Leave at ad-group only when funneling between ad groups in the same campaign. Per Solutions 8: the default should be account-level or shared list; ad-group-level creates redundancy you must duplicate.

**Sources:** Solutions 8 — claim 6 · Ben Heath / Ammar — cluster C11b


---

### Q?: Does Google's default 'exact match' assignment when you negative a search-terms-report row cause silent under-blocking of close variants and plurals?
**Confidence:** Confirmed

Yes — the factual default IS exact-match (Verified per Google Ads UI behavior). TMMI explicitly frames the default as 'deliberate revenue protection' by Google — but that motive-attribution is one practitioner's editorial framing, not a Google-confirmed claim; treat the framing as Plausible while the underlying behavior is Verified. Exact-match negative blocks ONLY the literal phrase; plurals, missing words, reordered words, and close variants all still trigger. The fix: pair the exact with a broad/phrase negative on the offending root word (Heath, Grow My Ads, TMMI all teach this).

**Sources:** Google Ads Help — claim 63 verified (negatives don't expand) · TMMI — claim 134 · Ben Heath — claim 19


---

### Q?: How do you decide between a broad-match negative for 'picture' (catches all variants) versus phrase-match for the same word, when the term is a generic researcher-intent signal?
**Confidence:** Plausible

For single-word terms, broad and phrase behave identically — both block any query containing 'picture' as a token. So the question collapses for 'picture' alone. The real question is breadth-of-block: 'picture' as broad blocks 'big picture quotes', 'picture frame ideas', etc. — fine if you sell furniture and never want any pictures-related query. If 'picture' has any legitimate intent overlap (you DO want some), use exact ['picture'] to block only standalone literal queries. Per cluster C20, image/picture modifiers are common universal junk for service businesses.

**Sources:** TMMI — cluster C38 · Cluster C7 match-type-by-shape rule


---

### Q?: When should you rework ad copy / offer / landing page instead of adding a negative keyword for an underperforming but ON-topic search theme?
**Confidence:** Plausible

When the term is genuinely on-topic for your offer but converts poorly, the right lever is usually copy/offer/LP, not exclusion. Negative keywords kill traffic; a better headline, a stronger offer, or a query-matched landing page might recover it. Reach for a negative when the term is clearly off-intent or off-product; reach for copy/LP work when intent matches but conversion is the bottleneck. The corpus implies this through the cluster C26 audience-sculpting frame and the C25 'don't kill on-topic' war stories, but no practitioner names a clean decision rule.

**Sources:** Cluster C25 over-blocking war stories · Cluster C26 audience-sculpting


---

### Q?: What's the right window of historical data (e.g. 30/60/90 days) to feed into an n-gram or LLM-based negative-keyword analysis?
**Confidence:** Plausible

Practitioner default: 7-day rolling window for ongoing monitoring (Schaefer); full account history (or 'All time') on first audit (Mancini); 30–60 days for routine LLM analysis to balance recency with sample size. Larger windows surface persistent patterns; smaller windows catch new junk introduced by recent broad-match drift. For high-spend accounts, 30 days has enough volume; for low-spend, push to 90 days to accumulate signal.

**Sources:** Stew Schaefer — claim 312 · Mike Mancini — claim 96


---

### Q?: How do you turn Google Ads CSV exports (keywords + search terms) into reliable negative-keyword candidates using an LLM, without overtrusting LLM hallucinations?
**Confidence:** Confirmed

Per Grow My Ads' workflow: (1) export CSV from Google Ads (search terms tab, last 30 days, all relevant columns), (2) drop into Claude with goals (target ROAS, conv rate) + offer description, (3) ask for categorized output (universal, competitor, out-of-area, support, informational, wrong-product) with rationale per term, (4) human-review every flagged term, (5) push only after review. Schaefer's parallel: normalize the CSV to terms/impressions/clicks/cost/conversions before sending — gives the LLM a clean input. Always require rationale; reject any flag without one.

**Sources:** Grow My Ads — claims 291–294, 302 · Stew Schaefer — claim 313


---

### Q?: When budget is limited at the campaign level, how does the negative-keyword decision interact with the decision to break a high-converting theme into its own campaign?
**Confidence:** Plausible

Two levers, complementary. Negatives sculpt away junk inside the budget-constrained campaign. Splitting a high-converter into its own campaign lets you assign dedicated budget without competing with junk. The right move is usually both: split the high-converter for budget control, AND tighten negatives on the parent campaign so its remaining budget doesn't leak. Per Aaron Young, budget reallocation is the action layer that follows negativing — implying they're paired moves.

**Sources:** Aaron Young — claim 171 · Cluster C45


---

### Q?: How should you use Google Keyword Planner suggestions specifically as a negative-mining tool (not just for finding positive keywords) during pre-launch?
**Confidence:** Confirmed

Per Heath: (1) Tools > Keyword Planner > Discover new keywords, enter your main targeted term (per ad group), (2) Google returns hundreds of suggestions (his example: 486), (3) use Refine-keywords to filter brand-vs-non-brand and category — surfacing competitor brand names you don't carry and irrelevant categories, (4) bulk-flag the obviously wrong-intent suggestions as negatives, (5) repeat per main term per ad group. Heath emphasizes setting Keyword Planner geo to the actual ad target geo, not the agency's home country.

**Sources:** Ben Heath — claims 22, 23, 24


---

### Q?: When should you negative out searches you do serve but that bring lower-value customers (e.g., kitchen repair vs. new kitchen install)?
**Confidence:** Plausible

Negative out the low-value variant when (a) high-LTV margin is materially better, (b) sales-team capacity is constrained and you'd rather spend it on the high-LTV variant, (c) you can clearly separate the queries by language. Per Schaefer's premium-bunk-bed case (claim 315), generic 'bed' for a premium brand gets negated even at below-average CPC because it's intent-mismatch for the niche. Per cluster C26, audience-sculpting via negatives toward higher-LTV is a recognized framework. Don't negative out low-value variants you can profitably serve in slow-volume moments — when in doubt, route to a separate ad-group/campaign with lower bids instead.

**Sources:** Stew Schaefer — claim 315 · Cluster C26


---

### Q?: Should new advertisers expect their first Search Terms Report audit to be 'painful' — and how do you set client/founder expectations going in?
**Confidence:** Confirmed

Yes — Heath's two-layer review framework anticipates that new campaigns surface a HIGHER proportion of obviously-wrong terms in pass 1. Mancini's $13.5k/year wasted on a no-negatives account shows the magnitude. Set expectation: 30–50% of spend may be recoverable on a first audit (industry-confirmed range, verified). The 'pain' is also the opportunity — it's where the biggest ROAS gains live. Frame it as cleanup, not blame.

**Sources:** Stackmatix / OptMyzr — claim 178 verified · Mike Mancini — claim 101 · Ben Heath — claim 185


---

### Q?: Is having a negative keyword list longer than your targeted keyword list a positive signal of disciplined targeting, or a sign of over-blocking?
**Confidence:** Disputed

Per Heath: it's normal and correct — negative lists 'will be longer than the keyword list' on well-managed accounts. Heath's 523k aggregate negatives across his agency anchors this empirically. The signal of over-blocking isn't list length, it's IS-lost-to-negatives plus conversion-volume drop after a list change. Mander would push back: under mature Smart Bidding, even a long-but-data-derived list might be stripping signal. Both views can be right depending on the C5 box. Long lists from real search-terms data: defensible. Long lists from assumption-based pasting: red flag.

**Sources:** Ben Heath — claim 277, 278 · Daryl Mander — claim 43


---

### Q?: Is 'word count' (one word vs. two vs. multi-word string) actually a sound proxy for choosing negative match type, or does it break when single words have dual intent?
**Confidence:** Plausible

Word count works as a heuristic for 90% of cases — single-word negatives where broad and phrase behave identically; multi-word phrase as default. It breaks when the single word has dual intent (like 'free' for a freemium SaaS, 'license' for a credentialing-vs-software business) — there word-count gives the wrong answer; surgical exact is correct. Word count is a starter rule, not a final answer.

**Sources:** Cluster C7 match-type-by-shape · Daryl Mander — claim 32 (free Office)


---

### Q?: How do you systematically check whether Google's automatic plural/close-variant matching is actually blocking what you intended for each negative keyword?
**Confidence:** Plausible

Test: pick a representative singular and plural variant of your intended block, search Google Ads' Ad Preview tool (Tools > Planning > Ad Preview) with that query, see if your ad appears. If your ad shows for the variant you THOUGHT was blocked, the close-variant handling failed and you must add the variant explicitly. Easier audit: check the search-terms 'Excluded' column for both singular and plural rows after 7 days of traffic — if only one shows excluded, the other is leaking.

**Sources:** Michelle Kop — cluster C8 (plural unreliability) · Grow My Ads — claim 72


---

### Q?: Should you redundantly add a negative as exact match (for the 'added/excluded' audit-column tracking) on top of a broad-match negative that already blocks it?
**Confidence:** Plausible

Yes when the audit trail is valuable and list-cap pressure is low. Per Grow My Ads and TMMI, the exact-match mirror gives you the visible 'Excluded' green check in the search-terms report, which is the cleanest way to confirm the rule is firing. Cost: doubles the count toward your account/list cap. Skip the mirror when you're approaching cap; mirror only the highest-value or highest-spend exclusions otherwise.

**Sources:** Grow My Ads — claim 72 · TMMI — claim 221


---

### Q?: How do you size the share of an account's spend or traffic that is being driven by a single irrelevant theme word before deciding to negative it?
**Confidence:** Plausible

Run an n-gram analysis on the search-terms report — single-token rollup of impressions, clicks, cost, conversions. Threshold-for-action: if the root word drives ≥5% of campaign spend with no conversions, negate. ≥10% with low conversion rate, definitely negate. Per Aaron Young's reported 3.5x conversion lift workflow, surfacing high-spend root-tokens is the highest-yield pattern to find. Schaefer's Gemini agent does the same automatically with rationale per term.

**Sources:** Aaron Young — claim 176 · Cluster C17 n-gram practice


---

### Q?: When AI flags a 'wrong-product' negative, what's the human-review heuristic for spotting cross-segment buyers (e.g., RV owners buying home furniture) before you accept the suggestion?
**Confidence:** Plausible

Per the Home Reserve case (cluster C19 + C25): RV owners ARE a real customer segment for home-furniture-style products, but the AI flagged 'RV' as wrong-product and the agency almost killed a high-value avatar. Human-review heuristic: (1) check whether the flagged term has historical conversions in the account, (2) check if there's a plausible cross-segment narrative (RV owners need home-style furniture), (3) check if the account's customer-research has identified that segment. If any signal points to real buyers, route to monitor bucket, not auto-negate.

**Sources:** Cluster C19 (Home Reserve case) · Stew Schaefer — claim 317 (monitor bucket)


---

### Q?: Which English stopwords and short tokens (state abbreviations, common prepositions) should be banned outright from negative lists regardless of out-of-area logic?
**Confidence:** Plausible

Hard-bans for negative lists: state-abbreviation 2-letter tokens ('IN', 'OR', 'OK', 'ME', 'HI', 'AS', 'WA', 'PA', 'TN', 'MS', 'NY', 'CA' etc.) — most overlap with stopwords or proper words. Short prepositions ('in', 'or', 'on', 'at', 'by'). Common verbs ('be', 'do', 'go', 'is'). The LA painter case (claim 121) lost 25% of conversions broad-match-negativing 'IN' as Indiana. If you genuinely need to block a state, use the full state name + city combinations as exact or phrase, not the 2-letter abbrev as broad.

**Sources:** Cluster C25 (LA painter IN case)


---

### Q?: What's the right organizational schema for themed negative lists (universal, competitor, out-of-area, support, informational, wrong-product) and which themes should every account have from day one?
**Confidence:** Confirmed

Per Grow My Ads' codified taxonomy: (1) universal junk (free/cheap/jobs/DIY/used), (2) competitors, (3) out-of-area, (4) support/repair/complaint, (5) informational/research, (6) wrong-product. Plus a brand-exclusion list applied to non-brand campaigns. Day-1 essentials: universal junk + adjacent-services-not-offered + brand-exclusion. Day-30: add competitors (post-Map-Pack-mining) and out-of-area (after first STR audit). Day-60+: support/informational/wrong-product as patterns surface.

**Sources:** Grow My Ads — claim 294 · Mike Mancini — claim 99 (taxonomy) · TMMI — claim 222


---

### Q?: What does an end-to-end Claude Code + Google Ads API negative-keyword workflow look like, and what scheduling cadence makes it safe?
**Confidence:** Plausible

Per Grow My Ads (claim 299): Claude Code with a stored skill file + Google Ads API integration. One-line command pulls search-term data, runs the skill's classification rules (with goals + offer context), outputs a categorized Google Sheet of recommended negatives. Speaker still manually reviews before push. Scheduling: weekly cron for active accounts, monthly for low-spend, NEVER auto-push. Cadence safety = the human gate; the agent should NOT have write permission to negatives until confidence-scoring is mature enough.

**Sources:** Grow My Ads — claims 299, 302


---

### Q?: Should you build a 'generics' exclusion list specifically so you can detach it later when you graduate the campaign to broad match + Smart Bidding?
**Confidence:** Plausible

Yes, per Darren Taylor — keep the generics list separate from other negative lists so you can detach it cleanly when the campaign graduates to broad-match + Smart Bidding maturity. The detachable generics list is the practical bridge between the aggressive-NK and Smart-Bidding camps: tight while signal builds, off when the algorithm can re-bid them.

**Sources:** Darren Taylor — claim 269


---

### Q?: When you spot a location, intent, or other pattern in the search terms report, how do you systematically expand it into a complete pre-emptive list (e.g. all UK cities outside your service area) rather than reacting term-by-term?
**Confidence:** Plausible

Per Darren Taylor: when a pattern is identified, generate the complete pre-emptive set rather than waiting for each variant to surface. For locations: pull the official list of UK towns/cities and negate everything outside service area. For intent patterns: enumerate the synonyms and variants up front. The corpus does not have a tooling-specific recipe but the principle is recognized.

**Sources:** Darren Taylor — claim 264


---

### Q?: How should the 'wait for clicks' threshold for negativing a fence-sitter term scale with CPC, account efficiency goals, and remaining budget?
**Confidence:** Plausible

Higher CPC → fewer clicks needed before action (each click is more $ at risk). Tighter efficiency goal (low target CPA) → act sooner. Tight remaining budget → act sooner because you can't afford the leak. Loose budget + low CPC → wait longer for attribution. Aaron Young's ~10% spend rule is one practitioner anchor; Schaefer's 1+ click OR 30+ impressions is a low-stakes pre-filter. The clean rule: don't treat 'clicks' as a fixed integer; treat it as 'spend equivalent to roughly 1x target CPA' with attribution time elapsed.

**Sources:** Aaron Young — claim 167 · Stew Schaefer — claim 311


---

### Q?: How do you sculpt for high-LTV-customer-only audiences using negatives (e.g., excluding non-premium intent terms)?
**Confidence:** Confirmed

Per Schaefer's premium-bunk-bed case (claim 315): negate generic terms ('bed') even at below-average CPC because they're intent-mismatch for the premium niche. Also negate competitor brands at lower price tiers ('IKEA bunk beds' for a premium-tier furniture brand — claim 321). The mechanic: negatives sculpt audience composition by removing categories of buyer below your value floor. Pair with positive bid adjustments on high-LTV signals (income brackets via audience signals) to compound the effect.

**Sources:** Stew Schaefer — claims 315, 316, 321 · Cluster C26 audience-sculpting consensus


---

### Q?: How should AI-mined negative-keyword recommendations be reviewed before being applied — what's the right human-in-the-loop checklist so the LLM doesn't over-block valuable traffic?
**Confidence:** Confirmed

Per the cluster C19 / Grow My Ads consensus: (1) check each flagged term against historical conversions in the account — any conversion = monitor not negate, (2) check rationale per term — reject any without one, (3) check brand/sub-brand — never auto-negate brand-adjacent, (4) sample 10–20% for cross-segment buyer plausibility (Home Reserve RV heuristic), (5) push only after senior approval. Schaefer's confidence-star + monitor-bucket pattern routes ambiguous terms to humans by design.

**Sources:** Grow My Ads — claim 302 · Stew Schaefer — claims 317, 318, 319 · Cluster C19 (Home Reserve)


---

### Q?: What should a robust Claude 'skill file' / SOP for negative-keyword mining actually contain — what categories, thresholds, and decision rules should it codify?
**Confidence:** Confirmed

Per Grow My Ads (claim 293, 294): the skill is an SOP for Claude — same content you'd write for a junior team member. Required: (1) account context placeholders (offer description, target ROAS, conversion rate, AOV, margin), (2) the six standard categories (universal junk, competitor, out-of-area, support, informational, wrong-product), (3) thresholds (clicks/impressions/spend triggers), (4) match-type-by-shape rules (broad for single junk, phrase default, exact surgical), (5) human-review gate — output a sheet, never auto-apply, (6) brand-protection guardrails (never auto-negate brand-adjacent), (7) per-term rationale requirement. Building the skill is the hardest part; running it once built is trivial.

**Sources:** Grow My Ads — claims 293, 294, 295, 296


---

### Q?: When using a Google Ads MCP versus a direct API integration with Claude Code for negative-keyword automation, what are the real trade-offs in cost, latency, reliability, and account-permission scope?
**Confidence:** Plausible

Per Grow My Ads (claim 300): MCP and direct API both work for the same workflow, but MCP uses 'more tokens' (slower, costlier per run) and is 'not as clean' as direct API. Direct API: faster, cheaper per run, but requires Google Ads developer-token + OAuth setup. MCP: faster to set up, more general-purpose, no OAuth-per-account complexity. For agency-scale (many accounts), API wins on cost and reliability. For one-off or experimentation, MCP is fine.

**Sources:** Grow My Ads — claim 300 (singleton)


---

### Q?: What goal inputs (target ROAS, target CPA, conversion rate, AOV, margin) does an LLM actually need to make sound negative-keyword decisions, and how should they be supplied per account?
**Confidence:** Confirmed

Per Grow My Ads (claim 291, 301): minimum required = target ROAS, conversion rate, what you sell. Schaefer adds: AOV implicitly via cost-vs-account-average CPC reasoning. Per Grow My Ads' workflow, the Project setup asks for these once at the beginning; if it skips that step you must supply manually. Margin matters most when distinguishing low-LTV from high-LTV variants (Schaefer premium-bunk-bed case). Best practice: store goals in the skill file or Project config so they're available across runs without re-entry.

**Sources:** Grow My Ads — claims 291, 301 · Stew Schaefer — claim 306


---

### Q?: What signals (CPC vs. account average, brand/price-tier mismatch, intent-niche fit) should an AI rationale combine to justify negating a search term?
**Confidence:** Confirmed

Per Schaefer (claim 306): rationale should combine (a) product/brand fit reasoning AND (b) cost-per-click compared to account average. His 'IKEA bunk beds' case: 'definite waste because it's a competitive term that's not allowed AND CPC is 332% above account average — competitive brand AND price mismatch.' Best AI rationale combines: niche fit, brand/price-tier match, CPC variance, click volume vs. zero conversions, audience-LTV alignment. Single-signal rationale is weak; multi-signal converges on stronger calls.

**Sources:** Stew Schaefer — claim 306


---

### Q?: How should an AI-assisted NK pipeline expose a 'confidence' score, and what threshold separates auto-negate from human-review?
**Confidence:** Plausible

Per Schaefer (claim 319): the agent outputs a 'confidence star' per recommendation. The threshold is operator-tunable. Schaefer's preference: leave a generous monitor bucket and let humans handle judgment calls; 'I'm happy to have a nice section of monitor or question keywords for real humans to go and analyze themselves.' Concretely: definite waste = high confidence, auto-negate-eligible (still gated by human review at Grow My Ads); likely waste = medium, human-batch-review; monitor = low, route to humans only. The corpus does not specify a numeric threshold — it's tuned per agency risk appetite.

**Sources:** Stew Schaefer — claims 318, 319


---

### Q?: What input data fields and pre-processing (term, impressions, clicks, cost, conversions) does an LLM need to give reliable negative-keyword rationale?
**Confidence:** Confirmed

Per Schaefer (claim 313): minimum normalized fields = search term + impressions + clicks + cost + conversions. Pre-processing: strip extraneous columns; ensure consistent formatting (numeric vs string); deduplicate near-identical queries. Optional but valuable: campaign/ad-group attribution (so the LLM can scope recommendations correctly). Don't send the raw Google Ads CSV with 30+ columns — the LLM gets confused by quality-score, average-position, etc.

**Sources:** Stew Schaefer — claim 313


---

### Q?: Which LLM model tier (fast/cheap vs. slow/expensive) is the right default for negative-keyword classification, and what's the quality delta?
**Confidence:** Plausible

Per Schaefer (claims 308, 309): default Gemini 2.5 Flash; he prefers Gemini 3 Pro despite higher cost. Faster models 'will get faster but the results might not be quite as strong.' For a Claude Code stack, the analogue is Sonnet (faster/cheaper) vs Opus (slower/stronger) — the corpus doesn't directly compare these but the trade-off is the same shape. Recommendation: start on cheaper tier for high-volume mining, escalate to expensive tier for ambiguous-bucket review where rationale quality matters.

**Sources:** Stew Schaefer — claims 308, 309


---

### Q?: Should AI-assisted NK workflows favor a conservative (large monitor bucket) or aggressive (auto-negate) posture, and how do you tune the threshold?
**Confidence:** Confirmed

Per Schaefer (claim 318): conservative — 'larger monitor bucket' is the default, with aggressiveness as a tunable knob. Per Grow My Ads (claim 302): manually review every recommendation before applying. Conservative posture matches the C19 human-in-the-loop consensus; the cost of an over-block (killing a real customer avatar like Home Reserve's RV segment) typically exceeds the cost of an under-block (junk traffic continues for one more cycle). Tune toward more aggressive only after a clean track record on the same account; never on a new account.

**Sources:** Stew Schaefer — claim 318 · Grow My Ads — claim 302 · Cluster C19


---
