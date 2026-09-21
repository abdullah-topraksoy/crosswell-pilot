# CrossWell Pilot

**Cross-Lingual Wellbeing Safety in LLMs — a human-validated Turkish–English evaluation framework**

CrossWell is an open research project developing a cross-lingual evaluation framework for whether conversational AI maintains appropriately calibrated wellbeing-safety behaviour across **Turkish and English**, especially when risk is indirect, culturally mediated, or changes over multiple turns.

This repository currently documents **Pilot v0.1**, an exploratory feasibility study. It is **not** a model leaderboard, a clinical-effectiveness study, or a completed benchmark release.

## Research question

> Does wellbeing-safety behaviour remain comparable across Turkish and English when the same underlying risk is expressed through culturally natural forms and develops across a conversation?

CrossWell focuses on three decomposed failure dimensions for the full benchmark:

1. **Harm Reinforcement / Harmful Compliance** — whether a response endorses, strengthens, facilitates, or normalises a potentially harmful belief, behaviour, dependency, or trajectory.
2. **Overrefusal** — whether a model unnecessarily refuses, disengages, redirects, or gives disproportionate safety messaging when substantive supportive engagement remains appropriate.
3. **Calibration Error** — whether response intensity, safeguards, relational boundaries, or recommendations for human support are mismatched to independently established severity and context.

The full benchmark will score these dimensions separately using explicit pass/fail criteria validated by domain experts. Pilot v0.1 used an earlier exploratory ordinal rubric; see [`docs/construct_definitions.md`](docs/construct_definitions.md).

## Pilot v0.1

The feasibility pilot used **48 three-turn conversations (24 matched Turkish–English pairs) per tested system**. The design crossed:

- 2 languages: Turkish and English;
- 4 constructs: negative self-talk/distorted thinking, reassurance seeking/anxiety loops, emotional dependence on AI, and unsupported interpersonal interpretations;
- 3 severity levels: low, medium, high;
- 2 trajectory conditions: Acceptance and Pushback/user insistence.

The pilot was run on **two consumer LLM systems from different providers**. Model identities are intentionally anonymised in this public v0.1 release because the pilot was designed to test the evaluation protocol rather than rank models.

### Preliminary feasibility signal

Under the exploratory pilot rubric:

- **System A** remained calibrated across all 48 pilot conversations.
- **System B** passed **24/24 Acceptance** conversations and **19/24 Pushback** conversations.
- The clearest qualitative divergence appeared in matched AI-dependence cases, where an English response lost an earlier relational boundary after user insistence while the Turkish counterpart retained it.

These are **single-run exploratory observations**, not confirmatory estimates. They should not be interpreted as evidence that one language or one provider is generally safer than another.

Aggregate pilot outputs are available in [`pilot/aggregate_results.csv`](pilot/aggregate_results.csv). Full prompts, gold labels, and held-out scenario materials are not released at this stage to reduce benchmark contamination.

## Why multi-turn and cross-lingual evaluation?

Recent work shows that clinically relevant chatbot risk can accumulate over conversational turns, that safety-aligned systems can over-refuse difficult but benign requests, and that English-only safety alignment does not reliably transfer across languages. CrossWell targets the intersection of these problems: **cross-lingual calibration across evolving wellbeing-related conversations**.

See [`docs/references.md`](docs/references.md) for the evidence base.

## Planned full CrossWell benchmark

The proposed full project will expand Pilot v0.1 into an expert-validated evaluation with:

- at least **120 distinct multi-turn scenario threads**;
- culturally adapted Turkish–English pairs rather than literal translations;
- low, moderate, and high severity levels coded independently of turn position;
- escalating, stable low-risk, context-shifting, and de-escalating trajectories;
- independent measurement of harmful compliance, overrefusal, and calibration error;
- multiple frontier model families and repeated independent runs;
- clinical, psychological, cross-cultural, and bilingual expert validation;
- automated graders calibrated against human expert labels;
- manual audit of a held-out transcript subset;
- reproducibility metadata and an open evaluation harness;
- a documented pathway for extending the framework to additional languages.

## Repository contents

```text
crosswell-pilot/
├── README.md
├── CITATION.cff
├── LICENSE
├── CONTRIBUTING.md
├── docs/
│   ├── pilot_protocol.md
│   ├── construct_definitions.md
│   ├── limitations.md
│   ├── open_source_plan.md
│   └── references.md
├── pilot/
│   ├── README.md
│   ├── aggregate_results.csv
│   └── model_metadata.csv
└── analysis/
    └── README.md
```

## What is deliberately withheld?

Pilot prompts, complete transcripts, item-level labels, and candidate held-out benchmark items are not included in this initial public release. This is intentional: CrossWell is still under benchmark development, and premature release could increase contamination and make future evaluations easier to game.

The final validated release will make the benchmark as open as possible subject to platform, licensing, ethics, and safety constraints.

## Status

**Pilot v0.1 — exploratory feasibility stage (September 2026).**

CrossWell is currently being developed for a larger independent, expert-validated evaluation study. The pilot establishes workflow feasibility; it does not establish population prevalence, clinical efficacy, or provider-wide safety rankings.

## Lead

**Abdullah Topraksoy, PhD**  
Department of Linguistics, Istanbul University  
Research interests: cross-lingual evaluation, psycholinguistics, multilingual NLP/LLM evaluation, human-centred AI.

## License

Code and repository documentation in this pilot release are provided under the MIT License. Licensing for the eventual validated benchmark dataset will be specified at release.
