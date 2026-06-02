# Implementation Roadmap

Start with one domain, one schema, one loop, and one map.

The first goal is not to exhaust all human ideas. The first goal is to prove that the system can take a seed idea and produce a useful, structured, ranked, expandable map of adjacent hypotheses.

## MVP 1: Hypothesis Generator and Evaluator

Goal:

> Given a domain and a seed idea, generate structured hypotheses, evaluate them, cluster them, and produce top idea cards.

Example input:

```text
Domain: cognitive neuroscience
Seed concepts: stress, PFC, hippocampus, amygdala, neuroecology
Generation mode: ecological reframing
```

Example output:

- Candidate hypotheses.
- Scores.
- Critiques.
- Predictions.
- Possible tests.
- Related concepts.
- Top-ranked cards.
- Idea graph.

## MVP 2: Retrieval

Connect generated hypotheses to external knowledge.

Initial sources:

- OpenAlex metadata.
- arXiv metadata and abstracts.
- PubMed metadata and abstracts.
- Local PDFs.
- User essays and notes.
- Web articles.

For each hypothesis:

1. Generate search queries.
2. Retrieve related works.
3. Summarize closest literature.
4. Identify nearest existing ideas.
5. Estimate novelty.
6. Add citations and rival theories.

## MVP 3: Graph Memory

Store hypotheses, concepts, sources, and relationships.

Minimum graph should include:

- Hypothesis nodes.
- Concept nodes.
- Source nodes.
- Prediction nodes.
- Experiment nodes.
- Contradiction nodes.
- Edges for support, contradiction, generalization, specialization, prediction, testing, analogy, derivation, and domain membership.

## MVP 4: Recursive Expansion

Promoted hypotheses generate children.

```text
Hypothesis -> predictions
Prediction -> experiments
Experiment -> possible results
Result -> implications
Implication -> new hypotheses
```

This is where the system begins to feel like the Final Library.

## MVP 5: Human Steering

The user should be able to:

- Expand this.
- Merge these.
- Reject this.
- Find analogies.
- Make it more empirical.
- Make it more mathematical.
- Find the strongest objection.
- Find related work.
- Generate a paper outline.
- Generate variants.

The system should learn from these choices.

## MVP 6: Autonomous Exploration

Let the system run searches over selected domains and produce frontier reports.

Autonomous runs should remain auditable:

- Inputs.
- Operators.
- Model outputs.
- Evaluations.
- Sources.
- Promotions.
- Rejections.
- Graph changes.

## First Command-Line Target

A first working command could be:

```bash
final-library generate \
  --domain "cognitive neuroscience" \
  --seed "working memory as iterative updating" \
  --operators analogy,inversion,mechanism,prediction \
  --n 25
```

Then:

```bash
final-library evaluate --run latest
final-library map --run latest
```

Expected artifacts:

- `hypotheses.json`
- `ranked_hypotheses.md`
- `idea_graph.json`
- `frontier_report.md`

## Practical Repository Structure

The eventual implementation can grow toward:

```text
final_library/
  core/
    models.py
    scoring.py
    statuses.py
  generation/
    operators.py
    prompts.py
    generator.py
  evaluation/
    novelty.py
    plausibility.py
    skepticism.py
    falsifiability.py
    importance.py
    synthesis.py
  retrieval/
    openalex.py
    arxiv.py
    pubmed.py
    local_docs.py
    web_search.py
    embeddings.py
  graph/
    nodes.py
    edges.py
    clustering.py
    lineage.py
  storage/
    postgres.py
    vector_store.py
    document_store.py
  workflows/
    generate_evaluate_store.py
    expand_hypothesis.py
    literature_check.py
  api/
    server.py
    routes_hypotheses.py
    routes_search.py
    routes_graph.py
```

Frontend targets:

```text
frontend/
  components/
    HypothesisCard.tsx
    IdeaGraph.tsx
    CritiquePanel.tsx
    FrontierQueue.tsx
```

## First Database Tables

Minimum tables:

- `hypotheses`
- `claims`
- `concepts`
- `sources`
- `hypothesis_sources`
- `predictions`
- `experiments`
- `evaluations`
- `hypothesis_edges`
- `generation_runs`
- `model_outputs`

The idea graph should exist early. It is not a later visualization feature; it is the structure of the system.
