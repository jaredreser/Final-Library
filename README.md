# The Final Library

The Final Library is a hypothesis-space exploration system for mapping the space of human-articulable scientific hypotheses.

Its purpose is not to exhaust all possible ideas, all truths, or all meaningful forms of understanding. The narrower and more defensible claim is this:

> AI systems can systematically generate, test, organize, and retrieve the space of hypotheses that humans can state in language, formal notation, diagrams, models, and executable procedures.

That space is still enormous. It includes theories, mechanisms, causal explanations, mathematical conjectures, experimental designs, engineering principles, simulation models, and cross-domain analogies. The Final Library treats these as navigable objects rather than isolated texts.

## Core Premise

Human science advances by proposing articulable structures:

- A phenomenon exists.
- A mechanism explains it.
- A variable modulates it.
- A model predicts it.
- An intervention changes it.
- A measurement can detect it.
- A theory compresses many observations.

The Final Library is a machine-assisted attempt to generate and organize those structures at scale. It is best understood as a generative research engine over idea-space, with a library interface on top.

The system should not merely answer questions or store notes. It should maintain a standing population of candidate hypotheses: generating, pruning, improving, merging, ranking, and expanding them into conceptual trees.

## What It Stores

The library stores hypothesis records, not just documents. A hypothesis record contains:

- The claim.
- Its domain and subdomain.
- Its conceptual dependencies.
- The mechanism it proposes.
- The evidence that supports, weakens, or falsifies it.
- Its testability and required measurements.
- Its relation to other hypotheses.
- Its novelty relative to known literature.
- Its current epistemic status.

## What It Does

The system has four major functions:

1. Generate candidate hypotheses across scientific domains.
2. Evaluate candidates for coherence, novelty, plausibility, and testability.
3. Link hypotheses into maps of mechanisms, evidence, and implications.
4. Retrieve useful regions of the map for human researchers.

It also needs an agent institution that can operate at machine scale. Explorers generate ideas, scouts find prior art, critics identify weaknesses, verifiers check sources, synthesizers update canonical summaries, recombiners connect domains, and methodologists improve the protocols of the system itself.

## First Working Loop

The first useful version should implement one narrow loop:

1. Take a domain and seed idea.
2. Generate structured candidate hypotheses using explicit operators.
3. Normalize candidates into hypothesis objects.
4. Score them across multiple dimensions.
5. Generate predictions, tests, objections, and related concepts.
6. Cluster similar hypotheses.
7. Promote the strongest candidates into the library.
8. Expand promoted hypotheses into children.
9. Produce an idea map and frontier report.

The first goal is not to exhaust all ideas. It is to prove that one seed idea can produce a useful, ranked, expandable map of adjacent hypotheses.

## Boundary

The Final Library does not claim to replace empirical reality, lived experience, taste, practical judgment, institutions, or the discovery of phenomena that have not yet been observed. It maps what can be articulated, compared, and tested.

The library is strongest where ideas can be represented as claims, models, mechanisms, predictions, experiments, or formal objects. It is weaker where meaning depends on embodiment, culture, tacit skill, aesthetic value, moral salience, or historical contingency.

## Idea Fossils

The Final Library also needs a preservation layer for human-origin ideas that appear before the library can fully classify them.

An idea fossil is a clearly stated, dated, attributable, archived intellectual artifact. It may be a paper, essay, blog post, PDF, preprint, note, diagram, or dataset. It does not need to be famous, cited, institutionally endorsed, or already absorbed into a literature. Its value is that it remains intact enough for future systems to inspect, compare, attribute, and place.

This gives independent thinkers a route into the future record:

1. State the core claim.
2. Name the idea.
3. Define unusual terms.
4. Identify predecessors and adjacent literatures.
5. Separate evidence from speculation.
6. Explain what would falsify or weaken the idea.
7. Publish it in a stable public form.
8. Archive it with a timestamped copy.
9. Preserve links between versions.

The point is not to bypass rigor. It is to make future rigor possible.

## Initial Project Structure

- `docs/architecture.md` describes the system architecture.
- `docs/agent-infrastructure.md` describes the multi-agent research infrastructure.
- `docs/generation-operators.md` defines the first hypothesis-generation operators.
- `docs/hypothesis-lifecycle.md` describes how hypotheses move through the library.
- `docs/idea-fossils.md` describes how independent thinkers can preserve ideas for future discovery.
- `docs/implementation-roadmap.md` describes the staged build plan.
- `docs/retrieval-model.md` describes how users navigate the library.
- `docs/scoring-rubric.md` describes hypothesis evaluation and ranking.
- `schemas/contribution.schema.json` defines typed agent contributions.
- `schemas/hypothesis.schema.json` defines the first machine-readable hypothesis object.
- `taxonomies/scientific-domains.md` proposes a starter domain taxonomy.
