# Method

## Pipeline Summary

NV-Rep combines semantic gene representations and contrastive representation learning:

1. **Gene Description Retrieval**
   - Retrieve textual annotations for genes (e.g., NCBI Gene descriptions).
2. **LLM-based Gene Encoding**
   - Encode each gene description with a pretrained language model to obtain dense gene vectors.
3. **Cell Embedding Aggregation**
   - For each cell, select top expressed genes and aggregate their vectors into an initial cell embedding.
4. **Biological View Construction**
   - Create two complementary views:
     - Full transcriptome-informed view
     - Housekeeping-filtered view
5. **Supervised Contrastive Refinement**
   - Optimize embeddings by pulling biologically related cells together and pushing distinct groups apart.
6. **Downstream Evaluation**
   - Use refined embeddings for classification, transfer, visualization, and robustness tests.

## Design Rationale

- **Semantic prior integration:** Gene descriptions provide biologically meaningful context beyond count values.
- **View consistency:** Dual-view learning encourages embeddings robust to ubiquitous housekeeping signals.
- **Label-aware geometry:** Supervised contrastive learning improves class separation under imbalance.

## Scope of This Repository Stage

This repository currently focuses on documentation and project scaffolding for the NV-Rep research framework. Algorithmic implementation details and training code will be released in subsequent versions.
