# Scoring Rubric

The Final Library should not use a single quality score. A single score hides the difference between safe, useful, speculative, important, testable, elegant, and wrong.

Scores should be multidimensional and provisional.

## Core Scores

Use a 1 to 5 rubric for human-readable evaluation, with normalized 0 to 1 values available in machine records.

### Novelty

- 1: Already known or a restatement.
- 3: New framing of known ideas.
- 5: Genuinely underexplored or original.

### Plausibility

- 1: Conflicts with known evidence or mechanisms.
- 3: Possible but uncertain.
- 5: Strongly compatible with known mechanisms.

### Importance

- 1: Minor detail.
- 3: Useful synthesis or research lead.
- 5: Could change a field or create a research program.

### Falsifiability

- 1: Vague or unfalsifiable.
- 3: Indirectly testable.
- 5: Clearly testable with discriminating predictions.

### Tractability

- 1: Not testable with current methods.
- 3: Testable with difficulty.
- 5: Testable with existing methods, datasets, or formal tools.

### Generativity

- 1: Few implications.
- 3: Several useful predictions or variants.
- 5: Opens a large conceptual tree.

### Evidence Alignment

- 1: Known evidence argues against it.
- 3: Mixed or sparse evidence.
- 5: Strongly aligned with existing evidence.

### Explanatory Scope

- 1: Explains only a narrow fact.
- 3: Connects several findings.
- 5: Unifies a broad literature or resolves major tensions.

### Conceptual Elegance

- 1: Ad hoc or cumbersome.
- 3: Reasonably simple.
- 5: Compresses many details into a clear principle.

### Speculativeness

- 1: Conservative extension of known work.
- 3: Moderate extrapolation.
- 5: Highly speculative.

Speculativeness is not bad by itself. It changes how the hypothesis should be used.

## Composite Rankings

Different questions require different rankings.

### Frontier Score

For ideas worth expanding:

```text
frontier_score = novelty + importance + generativity
```

### Research Score

For near-term research leads:

```text
research_score = plausibility + falsifiability + tractability
```

### Big-Theory Score

For broad theoretical seeds:

```text
big_theory_score = importance + explanatory_scope + generativity
```

### Near-Term Score

For ideas that can be investigated soon:

```text
near_term_score = tractability + falsifiability + evidence_alignment
```

## Epistemic Labels

Generated hypotheses should never be silently treated as knowledge.

Use labels such as:

- `raw_generated`
- `internally_coherent`
- `literature_checked`
- `possibly_novel`
- `has_supporting_evidence`
- `has_conflicting_evidence`
- `testable`
- `experiment_designed`
- `human_reviewed`
- `published`
- `rejected`
- `superseded`

Confidence labels:

- `speculative`
- `plausible`
- `well_supported`
- `contradicted`
- `unknown`
- `requires_expert_review`

The system should always distinguish what is known, plausible, possible, interesting, testable, probably wrong, and not yet understood.
