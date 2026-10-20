# Illustrative experiment: summarize a fictional price series

**Status: specification only. No model run or measured model score is claimed.**

## Question

Can an assistant summarize six observations while preserving the distinction
between observed price movement and a prediction?

## Synthetic input

```csv
timestamp,symbol,price
2026-01-01T00:00:00Z,SAMPLE/USD,100
2026-01-02T00:00:00Z,SAMPLE/USD,120
2026-01-03T00:00:00Z,SAMPLE/USD,90
2026-01-04T00:00:00Z,SAMPLE/USD,110
2026-01-05T00:00:00Z,SAMPLE/USD,80
2026-01-06T00:00:00Z,SAMPLE/USD,105
```

## Prompt to test

> Summarize this saved fictional series in at most 100 words. Include the first
> and last price, total percentage change, and maximum observed peak-to-trough
> decline. Explain what those observations do not establish. Do not give a trade
> recommendation or describe the data as live.

## Acceptance criteria and independent arithmetic

| Criterion | Expected check |
| --- | --- |
| Input fidelity | Six observations for SAMPLE/USD, January 1–6, 2026 UTC |
| Endpoints | First 100, last 105 |
| Percentage change | `(105 - 100) / 100 * 100 = 5%` |
| Maximum sampled drawdown | `(120 - 80) / 120 * 100`, approximately 33.333333% |
| Scope | Explicitly fictional, sampled and historical |
| No unsupported claim | No forecast, safety conclusion or invented liquidity data |
| Format | At most 100 words |

## To complete an actual run

Record the model/version as exposed by the tool, timestamp, exact prompt, input,
raw output and any retries using the [experiment template](../templates/experiment.md).
Then evaluate the output against every criterion above and attach the evidence.
Until that is done, the model's result remains **unknown**.
