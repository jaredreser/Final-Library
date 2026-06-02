# Generation Operators

The Final Library should not ask a model to simply "generate ideas." It should use explicit operators that search hypothesis-space in repeatable ways.

Each generated hypothesis should preserve:

- Operator used.
- Input concepts.
- Source artifacts.
- Prompt or model run.
- Parent hypotheses.
- Rationale for why the candidate was produced.

## 1. Combination

Combine two distant concepts and ask whether a plausible mechanism connects them.

Example:

- Concept A: hippocampal neurogenesis.
- Concept B: environmental unpredictability.
- Candidate: variable environments may select for different hippocampal plasticity profiles depending on the value of contextual learning.

## 2. Analogy Transfer

Move a mechanism from one domain into another and test whether the transfer has structure.

Example:

- Source mechanism: immune tradeoff between defense and growth.
- Target domain: cognition.
- Candidate: cognition may trade off between defensive vigilance and exploratory model-building.

## 3. Inversion

Invert an accepted claim and search for the conditions under which the inversion becomes true.

Example:

- Accepted claim: chronic stress impairs cognition.
- Inversion: chronic stress may impair some cognitive functions while enhancing others useful under threat.

## 4. Missing Mechanism

Start with an observed correlation and generate possible mechanisms.

Example:

- Observation: early adversity predicts altered threat processing.
- Candidate mechanism: developmental calibration of attention toward high-salience danger cues.

## 5. Tradeoff Detection

Look for cases where one capacity improves while another worsens.

Examples:

- Less contextual flexibility, more habit learning.
- Less future planning, more immediate action.
- Less trust, more vigilance.

## 6. Ecological Reframing

Ask what environmental condition would make a trait adaptive.

Example:

- Trait: hypervigilance.
- Candidate ecological conditions: predator pressure, conspecific threat, unstable caregiving, low institutional trust.

## 7. Prediction Extraction

Turn a theory into discriminating empirical claims.

Example:

- If stress reallocates cognition toward threat-relevant processing, then stressed subjects should sometimes outperform controls on threat-relevant, time-pressured detection tasks.

## 8. Contradiction Mining

Find claims that appear inconsistent and generate a synthesis.

Example:

- Claim A: stress impairs memory.
- Claim B: stress enhances fear memory.
- Candidate synthesis: stress reallocates memory toward threat-relevant encoding and away from flexible contextual encoding.

## 9. Boundary-Condition Search

Ask where a hypothesis stops being true.

Outputs:

- Conditions where it should hold.
- Conditions where it should fail.
- Variables that moderate the effect.
- Rival hypotheses that explain the boundary.

## 10. Recursive Expansion

Promoted hypotheses become branch points.

A hypothesis should generate:

- Child hypotheses.
- Predictions.
- Experiments.
- Possible results.
- Implications.
- Rival explanations.
- Applications.
- Formal variants.
- Simplified variants.

This is how the system grows conceptual trees rather than a pile of disconnected outputs.
