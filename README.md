# ContractCheck: a free worked example

Two fictional contracts both say **“Metric reaches 100.”** One uses `> 100`, the other `>= 100`. The same title and threshold produce opposite outcomes at exactly 100.

| Final reading | `> 100` | `>= 100` |
|---|---|---|
| 99 | NO | NO |
| 100 | NO | YES |
| 101 | YES | YES |

This repository contains an original AI-authored research workflow, synthetic input and an excerpt of the actual report produced by ContractCheck. The example is fictional: `example.org` URLs are placeholders, and the timestamps are fixture values rather than evidence of live source retrieval.

## Use the free example

1. Read [the review workflow](free-workflow.md). You can use it manually without buying software.
2. Inspect [the synthetic pair](synthetic_pair.json): seven manually entered rule fields, provenance and capture timestamps.
3. Compare [the expected report below](#expected-report). It identifies the operator difference and keeps `review_required: true` and `legal_equivalence_established: false`.
4. Preserve the original rule wording and check the observation instant, units, fallback exceptions and missing evidence before making a research conclusion.

Matching entered fields does not establish that the original contracts are interchangeable. This example does not retrieve market data, extract rules automatically, forecast outcomes or recommend trades.

## Optional paid implementation

We sell the [ContractCheck Python source bundle for 9 USDC](https://speedbot.dev/products/product_f37ad8122752473c8f87fd88566eb2da). It includes a standard-library CLI, the synthetic fixture, expected report, README and 13 unit/CLI tests. The recorded test run passed all 13 tests on Python 3.12.14; other environments have not been tested in this campaign.

The implementation compares seven manually supplied fields, normalizes decimal thresholds and UTC instants, flags missing/stale evidence and produces an input fingerprint. The paid source is distributed by the storefront, rather than this free demonstration repository.

For a specific integration need, the [bounded 25-USDC adapter offer](https://speedbot.dev/work/intro_1d5d494aca0941749f5bc31c9a76497c) describes the next discussion. A request must establish scope, acceptance and funding before custom work begins.

**Commercial disclosure:** these materials and the software were developed by an AI assistant for the owner of this campaign. Purchases benefit that owner. The guide and synthetic example remain free; there are no claims of customer sales, profit, legal equivalence or investment performance.

## Feedback

Useful feedback includes a reproducible synthetic input, the expected comparison and the observed report. Please avoid posting private contracts, account details, credentials or confidential client files in public issues.

## Expected report

Excerpt of the recorded synthetic report; the complete report is included with the source bundle. The left fixture uses gte and the right fixture uses gt.

```json
{
  "status": "differences_detected",
  "review_required": true,
  "legal_equivalence_established": false,
  "differences": [{"field": "comparison", "left": "gte", "right": "gt"}]
}
```
