# Methods

## Task

AdaptMarket turns a dated company or market brief into concise analyst-style research. The target response links financial evidence to business performance, valuation, catalysts, and risks while separating:

- reported results from forecasts, guidance, and opinion;
- direct evidence from inference;
- material uncertainty from unsupported certainty.

The intended role is a first-pass research assistant. It is not a source of individualized investment recommendations or a substitute for primary-source review.

## Training run

| Parameter | Value |
| --- | --- |
| Track | Market Analysis & News — Equity Analysis |
| Base model | `mistralai/Mixtral-8x7B-Instruct-v0.1` |
| Training method | Supervised fine-tuning (SFT) |
| Training type | Full fine-tune |
| Data format | Chat |
| Epochs | 1 |
| Batch size | Maximum available |
| Learning rate | `0.00001` |
| LoRA | Disabled |
| Scheduler | Cosine; minimum learning-rate ratio `0.1`; `0.5` cycles |
| Warmup ratio | `0.1` |
| Maximum gradient norm | `0.5` |
| Weight decay | `0` |
| Evaluations | 5 |
| Train on inputs | False |

The experiment changed the training method from LoRA to full fine-tuning. Its objective was to retain target-domain behavior while improving transfer to the broader Market Analysis evaluation.

## Corpus scope

The restricted training material is designed to cover:

- company financial and operating performance;
- valuation assumptions and revisions;
- sector and industry developments;
- macroeconomic conditions;
- catalysts, risks, and outlooks.

The corpus and derived examples are not distributed in this repository. No claim is made that the corpus is complete, representative of all markets, or suitable for public redistribution.

## Research direction

The long-term direction is thesis-conditioned event-impact analysis: evaluate a new event against the company’s historical thesis, operating sensitivities, forecasts, valuation assumptions, catalysts, risks, peers, and sector context. See [ROADMAP.md](ROADMAP.md).
