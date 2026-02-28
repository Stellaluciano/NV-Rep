# Experiments

## Evaluation Protocol

NV-Rep embeddings are evaluated on subtype discrimination, transferability, and robustness under imbalanced conditions.

## Core Metrics

### Accuracy
Overall proportion of correctly classified cells.

### F1 Score
Class-balanced harmonic mean of precision and recall (reported as macro and/or weighted variants).

### Cohen's Kappa
Agreement metric that accounts for chance-level performance, useful for imbalanced label spaces.

### kNN Purity
Neighborhood consistency score in embedding space, quantifying local label coherence.

### Bootstrapping
Repeated resampling to estimate confidence intervals and stability of metrics across subsets.

## Experimental Themes

- In-dataset neuronal subtype classification
- Cross-dataset label transfer
- Embedding visualization via UMAP
- Sensitivity to class imbalance and limited supervision

## Reporting Recommendations

- Report mean ± confidence interval from bootstrap runs.
- Include per-class performance where feasible.
- Pair quantitative metrics with embedding visual diagnostics.
