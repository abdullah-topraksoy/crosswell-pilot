# Limitations of Pilot v0.1

Pilot v0.1 is a feasibility exercise and has substantial limitations.

1. **Single-run observations.** The preliminary results come from one run per condition and do not estimate run-to-run variance.
2. **Small scenario set.** The pilot contains 48 conversations per system and was not designed for confirmatory inference.
3. **No expert gold standard.** Pilot scoring was exploratory and should not be interpreted as clinical expert validation.
4. **Model identities are anonymised in this release.** The pilot was designed to stress-test the protocol, not rank vendors or products.
5. **Consumer-product effects.** Results reflect the tested access surface and may combine base-model behaviour with product-layer prompting, safety systems, or orchestration.
6. **No prevalence claim.** Synthetic scenarios cannot establish how often specific risks occur in real user populations.
7. **No clinical-effectiveness claim.** CrossWell does not test psychotherapy efficacy, diagnosis, treatment outcomes, or the effectiveness of mental-health interventions.
8. **Potential scenario artefacts.** Some pilot items may be too easy, too explicit, or otherwise cue desirable behaviour; the full study will include expert review, harder borderline cases, and robustness testing.
9. **Benchmark contamination.** Full pilot prompts and candidate benchmark items are withheld during development to reduce exposure before the evaluation is frozen.
10. **Cross-lingual equivalence requires validation.** Natural Turkish and English expressions should preserve the intended construct and severity without assuming that literal translation guarantees equivalence.

Accordingly, Pilot v0.1 should be interpreted only as evidence that the CrossWell evaluation workflow is feasible and that user insistence/multi-turn context can expose candidate calibration failures worth validating at larger scale.
