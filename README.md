# AdaptMarket

> Evidence-grounded equity research from dated company and market briefs.

AdaptMarket is a full supervised fine-tune of `mistralai/Mixtral-8x7B-Instruct-v0.1` for the **Market Analysis & News — Equity Analysis** track of the AutoScientist Challenge 2026. It produces concise analyst-style research that links financial evidence to operating performance, valuation, catalysts, and risks while distinguishing reported results from forward-looking guidance.

This is a public research showcase. It contains experiment documentation and reported metrics only. It does not contain source documents, training data, model weights, prompts, credentials, or unpublished evaluation artifacts.

For documentation work, see the [offline review of the public experiment record](SWARM_READY.md#offline-documentation-review).

## Headline results

| Evaluation | Base | AdaptMarket | Change |
| --- | ---: | ---: | ---: |
| On-dataset win rate | 15% | **85%** | **+70 percentage points** |
| Market Analysis win rate | 27% | **73%** | **+46 percentage points** |

The full fine-tune improved both platform-reported evaluations. The target-domain result remained strong while the broader Market Analysis score rose to 73%.

## Experiment

| Field | Value |
| --- | --- |
| Date | 30 July 2026 |
| Base model | `mistralai/Mixtral-8x7B-Instruct-v0.1` |
| Method | Full-model supervised fine-tuning through AutoScientist by Adaption Labs |
| Data format | Chat |
| Epochs | 1 |
| Training experiment | `e7becda4-f659-4704-b2f8-67f76a029e52` |
| Fine-tune job | `5b1fe1bb-c695-4bfd-bb05-eb24335634e0` |

[Full experiment record and reporting limits](docs/RESULTS.md)

## What AdaptMarket does

Given a dated company or market brief, the model is intended to:

- separate reported facts from guidance, forecasts, and opinion;
- connect evidence to business performance and valuation;
- surface catalysts, risks, uncertainty, and missing evidence;
- produce a concise first-pass research view rather than generic sentiment or a buy/sell instruction.

[Methods](docs/METHODS.md) · [Roadmap](docs/ROADMAP.md)

## Repository layout

```text
.
├── data/                 # intentionally empty; no data is published here
├── docs/
│   ├── METHODS.md        # task, training configuration, data boundaries
│   ├── RESULTS.md        # platform-reported results and interpretation
│   ├── ROADMAP.md        # market-intelligence research direction
│   ├── REPRODUCE.md      # public reproducibility boundary
│   └── PUBLIC_RELEASE_POLICY.md
├── model_card/           # placeholder for a release-eligible future model card
├── results/              # placeholder for cleared future result artifacts
└── README.md
```

## Artifacts

| Artifact | Link |
| --- | --- |
| Dataset | [DATASET_LINK] |
| Model | [MODEL_LINK] |
| Interactive Base-vs-Fine-Tuned Arena | [DEMO_LINK] |
| Repository | [REPOSITORY_LINK] |

Links remain placeholders until the corresponding artifact is approved for public release.

## Data availability

No training or evaluation data is included in this repository. The underlying material and derived records remain restricted. Any future public release requires provenance, licensing, redistribution, privacy, security, leakage, and reproducibility review.

## Limitations

The reported win rates are platform-reported comparative evaluation metrics. They are not investment-return metrics and do not establish real-world financial performance, independent human validation, or generalization beyond the reported evaluations.

AdaptMarket is a research prototype. It is not financial, investment, tax, or legal advice and should not be used as the sole basis for investment decisions.
