# Cycle Double Cover via Random Embeddings

This repository contains computational experiments related to the **Cycle Double Cover (CDC) Conjecture** using random graph embeddings and facial diagrams.

## Cycle Double Cover Conjecture

The CDC conjecture states:

> Every bridgeless graph has a family of cycles such that each edge is covered exactly twice.

For bridgeless cubic graphs, this is equivalent to finding an embedding with no singular edges.

---

## Singular and Regular Edges

Let \( G \) be a bridgeless cubic graph and let \( F \) be a facial walk in an embedding of \( G \).

- An edge \( e \) is **singular** if a facial walk traverses it twice.
- An edge \( e \) is **regular** if it appears in two different facial walks.

We further classify singular edges:

- **Good singular edge (-)**: the edge is traversed twice in the same direction.
- **Bad singular edge (+)**: the edge is traversed twice in opposite directions.

These definitions follow the facial diagram framework developed in our paper.

---

## Main Computational Experiment

For a random embedding of a bridgeless cubic graph \( G \) with \( m \) edges, our experiments suggest:

- Expected number of good singular edges ≈ \( m/3 \)
- Expected number of bad singular edges ≈ \( m/3 \)
- Expected number of regular edges ≈ \( m/3 \)

This experimental observation motivated Conjecture 1 in our paper.

---

## Repository Structure

```bash
.
├── README.md
└── notebooks/
    └── random_embedding_experiments.ipynb
```

---

## Example

```python
G = graphs.PetersenGraph()

sample_good_bad_regular(G, samples=10)
expected_good_bad_regular(G, samples=1000)
diagram_good_bad_regular(G, samples=1000)
```

Output format:

```python
[good singular (-), bad singular (+), regular]
```

---

## Paper

This work was published in:

**Proceedings of the 13th European Conference on Combinatorics, Graph Theory and Applications (EUROCOMB 2025)**

Pages 493–498

https://site.pheedloop.com/event/Eurocomb25/Abstracts

---

## Topics

- Graph Theory  
- Cycle Double Cover Conjecture  
- Random Graph Embeddings  
- Combinatorics  
- SageMath  
- Computational Mathematics
