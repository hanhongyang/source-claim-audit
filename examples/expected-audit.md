# Source claim audit

- Draft: examples/draft-with-problems.md
- Claims checked: 8
- Blockers: 3 · Major: 3 · Minor: 1
- Verdict: fix blockers first

## Findings

| ID | Severity | Location | Claim (quoted) | Problem | Fix |
|----|----------|----------|----------------|---------|-----|
| C1 | blocker | para 2 | "Typical sellers earn about $2,030 per month — that is 100 sales at $29, after the platform share." | wrong type: a hypothetical calculator (100 × $29) is presented as typical seller income. The draft also implies this is already net of the platform share, which the arithmetic does not establish. | Remove or relabel as a worked example. Do not call it typical without a primary source that reports a median or similar. |
| C2 | blocker | para 3 | "The same terms say refunds are not allowed, so revenue is booked as soon as a sale clears checkout." | inconsistent / unsupported: the previous paragraph cites terms that include a 30-day hold; this sentence contradicts that hold and attributes a "no refunds" rule to the same document without a quotation. | Re-read the cited terms. If refunds exist, delete this sentence. Do not forecast income as if there were no hold. |
| C3 | blocker | para 3 | "We should forecast January income using December's gross sales, with no hold." | inconsistent: follows from C2 and ignores the 30-day hold already stated in paragraph 1. | Forecast only amounts that will have cleared the stated hold and minimum payout; or drop the forecast. |
| C4 | major | para 4 | "Users report that approved listings start selling the same day." | underspecified: "users report" is not a checkable source (who, where, when, how many). | Cite a dated, named report, or downgrade to an unverified anecdote. |
| C5 | major | para 4 | "Demand is exploding" | unsourced causal/trend claim written as fact. | Delete, or replace with a sourced metric and a date (for example, listing or sales counts from an official page). |
| C6 | major | para 4 | "we will cover our token costs in the first week" | unsourced prediction stated as a plan-ready fact; no cost figures or sales evidence. | State it as a hypothesis, or add both a cost estimate and a sourced sales assumption. |
| C7 | minor | para 2 | "This is a reliable income stream." | overstated certainty given that no typical-income source is provided. | Soften to a goal or an unknown, pending evidence. |

## What is already solid

- Paragraph 1's payout mechanics (70% of net revenue, 30-day hold, paid on the 10th, $50 minimum, PayPal / Payoneer / bank transfer, terms updated 5 November 2026) are specific enough to verify against the cited creator terms. Keep them, and attach the URL in the published version if it is not already linked.

## Recommended next pass

- Delete or relabel the $2,030 "typical" income example.
- Align the refund and forecasting sentences with the 30-day hold in the terms you already cited.
- Either source the demand and time-to-first-sale claims, or drop them.
- Do not add any new numbers unless they have a primary source and a date.
