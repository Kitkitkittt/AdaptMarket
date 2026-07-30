# Methodology

## Research task

Given a dated company or market brief, the model produces a concise analyst-style response. The target behavior is to:

- identify the relevant reported facts and distinguish them from forecasts or guidance;
- connect financial evidence to operating performance, valuation, catalysts, and risks;
- state uncertainty and missing evidence rather than inventing support;
- avoid generic sentiment, unsupported recommendations, and individualized financial advice.

## Training approach

The latest experiment uses full-model supervised fine-tuning through AutoScientist by Adaption Labs.

| Parameter | Value |
| --- | --- |
| Base model | `mistralai/Mixtral-8x7B-Instruct-v0.1` |
| Training type | Full fine-tune |
| LoRA | Disabled |
| Epochs | 1 |
| Batch size | Maximum available |
| Learning rate | `0.00001` |
| Scheduler | Cosine; minimum learning-rate ratio `0.1`; `0.5` cycles |
| Warmup ratio | `0.1` |
| Maximum gradient norm | `0.5` |
| Weight decay | `0` |
| Evaluations | 5 |
| Train on inputs | False |
| Data format | Chat |

The configuration was selected to test whether full fine-tuning could preserve domain performance while strengthening behavior on the broader Market Analysis evaluation.

## Dataset design principles

The training corpus focuses on institutional-style equity research and market-analysis material. Its intended coverage includes:

- company financial and operating performance;
- valuation assumptions and changes;
- sector and industry developments;
- macroeconomic conditions;
- catalysts, risks, and outlooks.

The public showcase does not distribute the source material, derived training examples, or source-level metadata. Public release of any such artifact requires a separate review of provenance, licensing, and redistribution rights.

## Intended workflow

The model is designed as a first-pass research assistant. A researcher provides a dated brief; the model surfaces evidence-linked implications, uncertainty, and questions for further review. It does not replace primary-source verification, professional judgment, or investment due diligence.
