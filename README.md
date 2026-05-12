# Negative Keywords (Google Ads) SME

> Practitioner-voice expert on negative keywords in Google Ads — match-type asymmetry vs. positive keywords, search-terms-report mining cadence, n-gram analysis, scoping (account/campaign/ad-group/shared/PMax), AI-assisted classification, brand and competitor exclusions, lead-gen vs. e-commerce posture, the Smart-Bidding contrarian frame.

**Free. Apache 2.0. Bring-your-own-Claude.**

## What this is

A Claude skill bundle — a sanitized, attributed, downloadable subject-matter expert that runs inside Claude Code, Claude Desktop, or any Claude-API workflow. Drop it in, invoke it, get answers grounded in real practitioner content rather than generic LLM consensus.

Use when the question is about whether/when/how to add a negative keyword, what match type, what scope, what cadence, how to mine, how to automate, or how to audit existing lists.

## Install

```bash
# Claude Code plugin install (one-line)
claude plugin install sme-negative-keywords-google-ads --from https://fadaly.net/downloads/skills/sme-negative-keywords-google-ads.zip
```

Or clone this repo into your Claude skills directory:

```bash
git clone https://github.com/MomoFadaly/sme-negative-keywords-google-ads.git ~/.claude/skills/sme-negative-keywords-google-ads
```

Or download the zip from [fadaly.net/skills/sme-negative-keywords-google-ads](https://fadaly.net/skills/sme-negative-keywords-google-ads) and extract into `~/.claude/skills/`.

## What's in the bundle

| File | Size |
|---|---|
| `canon.md` | 83KB |
| `concepts.json` | 12KB |
| `mental-models.md` | 3KB |
| `SKILL.md` | 121KB |
| `thumb.png` | 1.32MB |
| `verification-results.json` | 19KB |
| `verification-targets.json` | 9KB |

Total: 1.56MB

## Sources

This SME's canon was built from these practitioners. Every claim in the canon is attributed.

- Google Ads Help (primary)
- Search Engine Land · Stackmatix · OptMyzr · Think with Google
- Ben Heath · Mike Mancini · Solutions 8 · Ammar (Google Ads For Leads)
- Daryl Mander (BigFlare) · Darren Taylor · Aaron Young
- Grow My Ads · Stew Schaefer (AI for PPC) · TMMI
- KeyCommerce · Loves Data · Michelle Kop · Max (Google Ads Nerd)

Primary sources (official documentation, peer-reviewed research) take priority over practitioner consensus, which takes priority over single-source claims. Confidence tiers are tagged inline.

## How it works

Claude reads `SKILL.md` as the system instructions for the skill. Supporting files (`canon.md`, `mental-models.md`, etc.) are loaded as reference material when the skill needs to answer off the cuff or cite a specific source.

When you ask a question this SME covers, Claude pulls the relevant canon entry, names its source, tags its confidence level, and pushes back if your question contradicts canon.

## Confidence levels

- **Verified** — primary source + practitioner corroboration. Treat as fact.
- **Confirmed** — practitioner consensus across credible voices, no primary contradiction. Defended best-practice.
- **Plausible** — single-source or thin evidence. Working hypothesis until validated.
- **Disputed** — credible voices disagree. The SME names the camps and gives you the lens to decide.
- **Stale** — once true, contradicted by current docs/data. Flagged for refresh.

## License

Apache License 2.0. See [LICENSE](LICENSE).

You are free to use, modify, redistribute, and build on this skill. Attribution to the original practitioners (named in `sources.md` or `SKILL.md`) is morally required even if not legally; their work made the canon possible.

## Built by

[Mo Fadaly](https://fadaly.net) — AI intrapreneur, runs Claude skills in production.

This is one of a series. See the [full skill catalog at fadaly.net/skills](https://fadaly.net/skills).
