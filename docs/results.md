# Results and Reporting Limits

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

## Platform-reported results

| Evaluation | Base | Adapted | Absolute change |
| --- | ---: | ---: | ---: |
| On-dataset win rate | 15% | **85%** | **+70 percentage points** |
| Market Analysis win rate | 27% | **73%** | **+46 percentage points** |

These are platform-reported win rates from the cited AutoScientist experiment. They measure comparative performance under that platform’s evaluations; they are not investment-return metrics and do not establish real-world financial performance.

## Interpretation

The experiment replaced LoRA with full fine-tuning. The adapted model achieved a large improvement on the target dataset and a positive gain on the broader Market Analysis evaluation. The narrower difference between adapted scores across the two evaluations is consistent with a more balanced result, but it does not by itself establish robustness across markets, time periods, source types, or research tasks.

## What is not claimed

This showcase does not claim:

- investment returns, alpha, price-target accuracy, or trading performance;
- an independent human evaluation or statistical significance test;
- public reproducibility from the restricted training corpus;
- that the result generalizes beyond the platform evaluations;
- that the model can replace analysts, primary-source review, or professional advice.

## Reproducibility path

A fuller public results release would require a release-eligible dataset, frozen evaluation definition, base and adapted outputs, evaluator details, error analysis, and permission to publish the relevant artifacts. Until then, this page is an experiment record rather than a complete reproducibility package.
