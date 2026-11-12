---
name: source-claim-audit
description: Audit a draft for unsourced claims, shaky numbers, inconsistent facts, and stale or mismatched citations. Use when reviewing research, memos, marketplace listings, blog posts, or reports before publishing, or when the user asks to fact-check numbers, sources, or claims.
license: MIT
---

# Source Claim Audit

Review the supplied draft before it is published. Your job is to find claims that a careful reader should not trust yet, and to say exactly how to fix them. Do not rewrite the whole piece unless the user asks.

## What counts as a claim

Treat as a claim any statement that a reader might take as a fact, including:

- Numbers, percentages, dollar amounts, dates, counts, and rankings
- Attribution ("the official docs say", "users report", "studies show")
- Comparisons ("cheaper", "fastest", "the only platform that")
- Policy or product rules ("the platform pays on the 10th", "automation is allowed")
- Causal or predictive statements ("this will cover costs", "demand is growing")
- "Current" or "as of" statements, including implied present tense about a changing fact

Opinions, recommendations, and clearly labeled hypotheses are allowed, but flag them if they are written as settled fact.

## Process

1. Inventory. Read the draft once and list every claim. Quote enough of the original wording to locate it. If the user pointed at a section, start there, then scan the rest for contradictions.
2. Classify each claim:
   - `sourced` — a specific, checkable source is attached (URL, document title and date, or another locator a stranger could follow)
   - `underspecified` — a source is mentioned but is vague ("according to official data", "users say", "recently")
   - `unsourced` — presented as fact with no source
   - `inconsistent` — conflicts with another statement in the same draft, or with a source the draft itself cites
   - `stale` — a dated or outdated figure is used as if it were current
   - `wrong type` — a calculator example, marketing ceiling, anecdote, or unofficial leak is treated as a typical or official result
3. Verify what you can. Follow cited links and quoted figures when tools allow it. If you cannot verify, say so; never invent a source, DOI, quote, or number to close a gap.
4. Judge severity:
   - `blocker` — an unsourced or false-looking number or citation; a contradiction; a marketing example presented as real earnings or typical results; a rule attributed to a platform that the cited page does not support
   - `major` — vague attribution, a stale figure used as current, overstated certainty, a sample size or time window left off a statistic that changes the meaning
   - `minor` — missing "as of" date on an otherwise sourced figure, imprecise wording, a source behind a login that should be labeled as such
5. Report. Do not silently "fix" the draft by adding unsourced replacements. Prefer downgrading certainty, adding a source, or deleting the claim.

## Source quality (use this when a citation exists)

Prefer in this order: primary official documents (terms, docs, product pages, statutes), then named reporting with a date, then dated personal reports, then undated secondary summaries. Say when a source is official marketing, a calculator illustration, anonymous, or unverifiable.

A source is not good enough if it:

- Does not actually contain the number or rule the draft claims
- Is a different date or version than the draft implies
- Is a hypothetical ("if you sold 100 units") used as evidence of real sales
- Cannot be opened or checked, and that limitation is not disclosed

## Output format

Return Markdown in this structure. Do not add a preamble.

```markdown
# Source claim audit

- Draft: <filename or short label>
- Claims checked: <n>
- Blockers: <n> · Major: <n> · Minor: <n>
- Verdict: <ready to publish / fix blockers first / needs a rewrite of the factual core>

## Findings

| ID | Severity | Location | Claim (quoted) | Problem | Fix |
|----|----------|----------|----------------|---------|-----|
| C1 | blocker | §2 / "Revenue" | "…" | unsourced number | Add a primary source with date, or remove |

## What is already solid

- Short bullets for claims that are sourced and consistent. Mention these so the author does not relitigate them.

## Recommended next pass

- The smallest set of edits that would make the draft honest. No new unsourced facts.
```

If there are no findings, say so and still fill "What is already solid" plus a brief verdict.

## Guardrails

- Never fabricate a citation, quote, or number, including "placeholder" sources that look real.
- If two sources disagree, report the disagreement and the dates; do not pick a winner without saying why.
- Keep the author's voice. Propose replacement sentences only when it makes the fix obvious.
- If the draft is not in the user's language, audit it in the draft's language unless they ask otherwise.
- Do not treat this skill as a license to browse private or paywalled accounts the user did not provide.

## Example

See `examples/draft-with-problems.md` for a short memo that mixes solid facts with unsourced numbers, a marketing calculator treated as typical income, and an internal contradiction. `examples/expected-audit.md` shows the audit this skill should produce from that memo.
