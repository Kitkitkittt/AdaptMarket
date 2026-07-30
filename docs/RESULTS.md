# Results

## Experiment record

| Field | Value |
| --- | --- |
| Date | 30 July 2026 |
| Track | Market Analysis & News — Equity Analysis |
| Training experiment | `e7becda4-f659-4704-b2f8-67f76a029e52` |
| Fine-tune job | `5b1fe1bb-c695-4bfd-bb05-eb24335634e0` |
| Base model | `mistralai/Mixtral-8x7B-Instruct-v0.1` |
| Training method | Full-model supervised fine-tuning |
| Data format | Chat |

## Platform-reported evaluation

| Evaluation | Base | AdaptMarket | Absolute change |
| --- | ---: | ---: | ---: |
| On-dataset win rate | 15% | **85%** | **+70 percentage points** |
| Market Analysis win rate | 27% | **73%** | **+46 percentage points** |

The full fine-tune outperformed the base model in both platform-reported evaluations. The adapted model’s Market Analysis score increased by 46 percentage points while its target-dataset score reached 85%.

## Interpretation

The result supports the experiment’s narrow hypothesis: full fine-tuning can improve this task-specific evaluation while also improving performance on the broader platform Market Analysis evaluation. It does not establish robustness across markets, time periods, source types, research tasks, or real-world investment decisions.

## Reporting limits

These metrics are platform-reported comparative win rates. They are not investment-return, alpha, price-target accuracy, or trading-performance measures.

This repository does not claim:

- an independent human evaluation or statistical significance test;
- public reproduction from the restricted training material;
- generalization outside the reported platform evaluations;
- replacement of analysts, primary-source review, or professional advice.

## Future evidence

A complete public reproduction package would require a release-eligible dataset, frozen evaluation definition, base and adapted outputs, evaluator configuration, error analysis, and permission to publish every artifact. This repository will add those materials only after they are cleared for public release.
