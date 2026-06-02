# Hypothesis Lifecycle

Every hypothesis in the Final Library moves through a traceable lifecycle.

## Stage 1: Generated

A candidate claim is produced by a generation strategy. It may be rough, redundant, vague, or implausible.

Required fields:

- Claim text.
- Generation method.
- Source concepts.
- Domain guess.
- Timestamp.

## Stage 2: Normalized

The candidate is rewritten into a structured hypothesis record.

Normalization asks:

- What is the exact claim?
- What entities and variables are involved?
- What mechanism is proposed?
- What would be observed if it were true?
- What would count against it?
- Which assumptions does it require?

## Stage 3: Deduplicated

The system searches for equivalent or near-equivalent hypotheses.

Possible outcomes:

- New record.
- Merge into existing record.
- Add as alternate formulation.
- Mark as special case of a broader hypothesis.
- Mark as broad version of narrower hypotheses.

## Stage 4: Evaluated

The hypothesis receives provisional scores.

Core scores:

- Coherence.
- Plausibility.
- Novelty.
- Testability.
- Specificity.
- Importance.
- Tractability.
- Generativity.

Each score should include a rationale and evaluator identity.

## Stage 5: Linked

The record is placed into the graph.

Link types:

- Supports.
- Weakens.
- Contradicts.
- Depends on.
- Refines.
- Generalizes.
- Specializes.
- Predicts.
- Explains.
- Suggests experiment.

## Stage 6: Reviewed

Human or trusted machine reviewers inspect the record.

Review states:

- Needs review.
- Accepted as coherent.
- Rejected as incoherent.
- Already known.
- Insufficiently specified.
- Empirically contradicted.
- Promising but untested.
- Supported.
- Strongly supported.

## Stage 7: Tested

If testable, the system proposes or links to experiments, simulations, proofs, or observations.

Testing records should include:

- Method.
- Required data.
- Predicted result.
- Actual result.
- Interpretation.
- Confidence update.

## Stage 8: Archived or Active

Some hypotheses remain active. Others are archived.

Archive reasons:

- Duplicate.
- Incoherent.
- Uninteresting.
- Untestable with known methods.
- Empirically falsified.
- Superseded by stronger formulation.

Archived hypotheses remain searchable because failed paths help map the space.
