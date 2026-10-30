# Features from annual reports

A shortlist of what to read in a 10-K, 10-Q, or earnings release if the goal is future excess returns. The ranking follows published return evidence, then a second pass on the primary tables. The long write-up is [Report features for excess returns](reports/Report%20features%20for%20excess%20returns.md). Source notes are in `research_notes/`.

## The result in one paragraph

The feature that holds up is how much this filing’s language changed from the firm’s own previous filing. Firms that rewrite the 10-K or 10-Q subsequently underperform firms that keep the language stable, and there is no jump on filing day. A large-cap book should underwrite about **2.9% a year** for that spread (Research Affiliates, top 1,000 US stocks, through September 2025). The academic broad sort, 1995–2014, is about **34–58 basis points a month**. The famous **188 basis points a month** is one cell only: equal-weighted Jaccard similarity on the risk-factor section. On that same design the MD&A is **11–22 basis points**. Two other filing features pay as risk premia rather than as slow reading: Item 1A cybersecurity exposure, and narrative debt-market constraints. Large language models are useful for pulling a customer name, a recurring addback, or a year-over-year edit out of a long file. No published horse race shows an LLM filing score beating section-level overlap. The two well-known ChatGPT-reads-the-disclosure papers were withdrawn in 2025.

## What to extract

Scores are for the period after the filing is public. Drift means the price catches up later. Premium means higher average return as compensation for risk, so the long side should lose when that risk shows up.

| Rank | Feature | Kind | Where to read | Direction | Number to cite |
| --- | --- | --- | --- | --- | --- |
| 1 | Year-over-year section change | Drift | Item 7, Item 1A, Item 3, officer language; 10-Q Item 2 | Stable language, higher later return | Large-cap Jaccard: **2.9%/yr**. Broad sort: **34–58 bp/month**. Risk-factor tail: **188 bp/month** equal-weighted |
| 2 | Item 1A cybersecurity exposure | Premium | Attack-like risk-factor language, not the word “cyber” | Higher average return | FF5 alpha **0.66%/month** equal-weighted, **0.57%** value-weighted (Mar 2008–Mar 2019) |
| 3 | Narrative debt constraints | Premium | Liquidity, capital resources, and debt discussion in the MD&A | Constrained firms earn more | Annualized FF5 alpha **6.5%** (debt), **3.7%** (external finance), **3.0%** (equity) |
| 4 | Disclosed major customers | Drift, haircut hard | Customer names and sales shares in Item 1 | Customer’s prior return predicts the supplier | Paper: **~1.5%/month**. A later correction says the alpha is overstated by more than 70% |
| 5 | Concluded SOX 302 material weakness | Drift | 10-Q Item 4, 10-K Item 9A | Weakness, lower later return | Own BHAR **~3%** over 60 trading days and **~6%** over 120. Gap vs effective controls **5.3–6.2%** |
| 6 | Change in current deferred revenue | Mispricing, draft magnitude | Balance-sheet liability and the revenue note | High increase, higher later return | Conference draft: nearly **9%** abnormal over the next year. Published abstract does not repeat the 9% |
| 7 | MD&A tone change vs the prior filing | Drift | Item 7 and 10-Q Item 2, as a change | Incremental drift past accruals and the earnings surprise | No verified portfolio percent |
| 8 | Recurring costs labeled non-recurring | Drift, old sample | “Other exclusions,” historically from I/B/E/S | Higher exclusions, lower later return | **29.9%** over three years, only **4.4%** in year 1. Sample 1988–1999, before Regulation G |

Rank 1 is the one to build first. Rank 4 is a link the filing discloses. The return input is the customer’s stock return, which is not in the prose. Rank 8 is the sign to keep. It is not a test of today’s earnings-release reconciliation.

## Worth scoring, with weaker or different evidence

These are real results. They are short-window, old, numeric rather than prose, or easy to confuse with a known accounting factor.

- **Positive-language similarity only.** Low overlap outperforms, the opposite sign of rank 1. About **5.5%/yr** in a blog backtest of large names through May 2020.
- **Going-concern language.** In the US, a five-factor twelve-month result of about **−10.6%**, and **−25.8%** for lottery-like names. The rest of the sample is about **−4.8%** and insignificant.
- **Customer-concentration change.** Patatoukas reports a trading strategy. The readable magnitude is a regression slope of about **0.10** next-year return per unit change, from the author’s slides.
- **Pension underfunding.** Lower later returns in the original footnote result, then mostly a distress mix. A secondary write-up quotes **43 bp/month**.
- **Whole-document cyber embedding.** A different object from rank 2. About **6.9%/yr**, and much larger before the premium was written up in November 2020. One later cyber-text score turns negative after that posting.
- **Physical climate sentences in Item 1A.** A May 2023 working paper: **1.5–2.9%/yr**. Call-based climate exposure is weaker. Transition and opportunity language do not share this result.
- **Aggregate manager sentiment.** A market state, not a stock pick. One standard deviation of optimism lines up with **−1.26%** of next-month market excess return.
- **A disclosed covenant violation.** Later operating and stock performance is positive. No verified stock-return percent. This is creditor intervention.
- **Context-adjusted profitability.** A transformer uses the filing to separate persistent profit from transitory profit. The June 2023 draft cuts the small-growth alpha from **−0.51** to **−0.13** without labeling the units.
- **Forward-looking MD&A tone against accruals.** When tone and accruals disagree, the accrual return shuts off. No standalone long-short.
- **Filing complexity.** A weight on the filing’s own news. Complex 10-Ks drift longer in the direction of the initial reaction. No hedge percent.
- **Loughran–McDonald negative words.** A days **[0, 3]** filing reaction. Not a twelve-month factor. A student re-test finds the four-day pattern gone after 2008.
- **Return-weighted tone.** The relation to filing-period returns lasts up to two weeks.
- **Piotroski F-score and Beneish M-score.** Numeric scores in the statements. F-score: about **23%/yr** inside high book-to-market, 1976–1996. High M-score: just under **1%/month** risk-adjusted (Beneish, Lee, and Nichols 2013).

## Worth extracting, not yet a return

Use these as structured fields. Do not put them in a portfolio until they beat section-level overlap.

- New severe risks versus risks that were actually retired, inside Item 1A.
- Specific risk language (a named customer, lawsuit, covenant, or number) as a weight on other scores. The published result is a larger three-day absolute reaction.
- Walked-back targets and redefined KPIs, this MD&A against the prior one and the earnings release.
- Multi-year changes in useful lives, residuals, and reserve methods.
- Contradictions among Item 1A, the MD&A, and the notes.
- Core earnings from a procedural read of the 10-K. This predicts next year’s earnings. It has no stock long-short.
- AI language only when headcount, product, revenue, or backlog backs it. Keyword introductions have an insignificant three-day filing return.
- Firm-specific political and regulatory risk in the filing. The canonical political-risk measure is an earnings-call result about volatility and investment.

## How to build it

Difference each section against the firm’s own prior filing, then check that peers did not all rewrite at once. Emit separate scores for Item 1, Item 1A, Item 3, Item 7, and the notes. Start the holding period only after the filing is public. For the language-change portfolio, formation is the month after the filing, and the gap is still widening at twelve months.

Freeze model weights before any backtest. Telling a model to ignore the future does not stop it. On late-2019 calls, Llama 2 produced “COVID-19” in **6.8%** of generations. Keep a new score only if it still predicts the next return after section-level Jaccard, the Loughran–McDonald change, accruals, asset growth, profitability, distress, and the latest earnings surprise.

## Left off on purpose

Fog and file size, moat adjectives, green-word counts, and Harvard word lists. Remaining performance obligations and net retention, which predict revenue and have no published return here. Restatement announcements: the **−9.2%** is the two-day window (Palmrose, Richardson, and Scholz 2004), not a drift after the news. Industry booms in competitive SIC industries (Hoberg and Phillips 2010) are a real return result and not a text feature. The withdrawn Kim, Muhn, and Nikolaev financial-statement and bloated-disclosure papers. Their surviving paper scores earnings calls.

## Sources for the corrected figures

Cohen, Malloy, and Nguyen, “Lazy Prices,” Journal of Finance, 2020, and NBER w25084 Table VII (September 2018 revision). Nguyen and Shim, Research Affiliates, June 2026. Florackis, Louca, Michaely, and Weber, Review of Financial Studies, 2023. Buehlmaier and Whited, Review of Financial Studies, 2018. Ghosh, Ikäheimo, Myllymäki, and Sihvonen, Journal of Business Finance & Accounting, 2026. Doyle, Lundholm, and Soliman, Review of Accounting Studies, 2003. Cohen and Frazzini, Journal of Finance, 2008. Prakash and Sinha, Contemporary Accounting Research, 2013.
