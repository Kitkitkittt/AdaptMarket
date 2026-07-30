# Equity-Researcher Model

> A public progress showcase for an AutoScientist Challenge 2026 submission in **Market Analysis & News**. This repository contains documentation only: no source documents, datasets, model weights, credentials, prompts, evaluation examples, or proprietary pipeline code.

## The project

The Equity-Researcher Model is a supervised fine-tuning experiment for producing concise, analyst-style market research from dated company or market briefs. The intended output connects financial evidence to business performance, valuation, catalysts, and risks, while separating reported facts from forward-looking guidance.

The goal is not to generate investment advice, price targets, or generic buy/sell answers. It is to support a research workflow with a first-pass analysis that identifies material changes, evidence gaps, and uncertainty.

## Latest experiment

| Field | Value |
| --- | --- |
| Track | Market Analysis & News — Equity Analysis |
| Date | 30 July 2026 |
| Base model | `mistralai/Mixtral-8x7B-Instruct-v0.1` |
| Method | Full-model supervised fine-tuning (SFT) through AutoScientist by Adaption Labs |
| Data format | Chat |
| Epochs | 1 |
| Training experiment | `e7becda4-f659-4704-b2f8-67f76a029e52` |
| Fine-tune job | `5b1fe1bb-c695-4bfd-bb05-eb24335634e0` |
| Platform model name | `adaption_mixtral_8x7b_instruc_equity_analysis_large_e7becda4` |

Full fine-tuning replaced LoRA in this run. The objective was to retain strong task-specific behavior while improving transfer to the broader Market Analysis evaluation.

## Results

| Evaluation | Base | Adapted | Change |
| --- | ---: | ---: | ---: |
| On-dataset win rate | 15% | **85%** | **+70 points** |
| Market Analysis win rate | 27% | **73%** | **+46 points** |

The adapted model outperformed the base model on both platform-reported evaluations. The results indicate a strong target-domain gain with improved performance on the broader Market Analysis domain.

See [results and reporting limits](docs/results.md) for interpretation and disclosure boundaries.

## Dataset strategy

The training material is grounded in institutional-style equity research and market-analysis documents. It covers company performance, valuation, sector developments, macroeconomic changes, catalysts, risks, and outlooks.

The aim is to teach evidence-grounded research writing rather than synthetic recommendations. Source documents and derived training data are not redistributed through this repository.

See [methodology](docs/methodology.md).

## Artifacts

| Artifact | Link |
| --- | --- |
| Dataset | [DATASET_LINK] |
| Model | [MODEL_LINK] |
| Interactive Base-vs-Fine-Tuned Arena | [DEMO_LINK] |
| Repository | [REPOSITORY_LINK] |

## Roadmap

The next stage expands from isolated company analysis toward thesis-conditioned, cross-company, and cross-sector impact reasoning:

1. Expand the market-research corpus across macroeconomics, industries, commodities, rates, currencies, credit, policy, company earnings, valuation, and timestamped news.
2. Connect company research into a market knowledge network spanning businesses, products, suppliers, customers, competitors, industries, and macro factors.
3. Model direct and higher-order cross-sector spillovers.
4. Evaluate new events against the existing investment thesis, not as isolated headlines.
5. Build a point-in-time market evidence graph to preserve temporal context and reduce leakage.

See the [detailed roadmap](docs/roadmap.md).

## Public-release boundary

This is a documentation-only showcase. It excludes restricted source text, private datasets, model weights, credentials, internal prompts, local paths, and unpublished implementation artifacts.

The model is a research prototype. Its outputs are not financial, investment, tax, or legal advice, and should not be used as the sole basis for investment decisions.
