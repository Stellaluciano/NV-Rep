# NV-Rep

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](#license)
[![Docs](https://img.shields.io/badge/Docs-In%20Progress-0A66C2.svg)](./docs/overview.md)
[![GitHub stars](https://img.shields.io/badge/Stars-Placeholder-blue.svg)](https://github.com/)
[![Research Status](https://img.shields.io/badge/Status-Active%20Research-6f42c1.svg)](#)

**NV-Rep** is a research framework for biologically grounded representation learning in single-cell transcriptomics. It integrates large language model (LLM)-derived gene embeddings, biologically informed cell representations, and supervised contrastive learning to resolve neuronal subtype heterogeneity and selective vulnerability from limited and imbalanced datasets.

## Key Features

- **LLM-derived gene semantics** from curated gene descriptions (e.g., NCBI Gene).
- **Expression-aware cell representations** built by aggregating embeddings from top expressed genes.
- **Dual biological views** via full transcriptome and housekeeping-filtered representations.
- **Supervised contrastive refinement** for label-aware embedding structuring.
- **Downstream-ready embeddings** for classification, label transfer, visualization, and robustness analysis.

## Method Overview

1. Retrieve textual gene descriptions.
2. Encode gene descriptions with pretrained LLMs into dense vectors.
3. Select top expressed genes per cell and aggregate gene vectors into an initial cell embedding.
4. Construct two biological views:
   - Full transcriptome-informed view
   - Housekeeping-filtered view
5. Refine embedding space with supervised contrastive learning.
6. Evaluate learned representations on subtype discrimination and vulnerability-oriented tasks.

## Architecture Diagram (Mermaid)

```mermaid
flowchart TD
    A[scRNA-seq expression matrix] --> B[Top expressed gene selection]
    B --> C[Gene description retrieval\n(e.g., NCBI Gene)]
    C --> D[LLM-based gene embedding]
    D --> E[Cell embedding aggregation]
    E --> F[Biological view construction]
    F --> F1[Full transcriptome view]
    F --> F2[Housekeeping-filtered view]
    F1 --> G[Supervised contrastive learning]
    F2 --> G
    G --> H[Refined cell embedding space]
    H --> I[Downstream tasks]
    I --> I1[Cell subtype classification]
    I --> I2[Label transfer]
    I --> I3[UMAP visualization]
    I --> I4[Robustness evaluation]
```

## Repository Structure

```text
NV-Rep/
├── README.md
├── LICENSE
├── CITATION.cff
├── CONTRIBUTING.md
├── SECURITY.md
├── CODE_OF_CONDUCT.md
├── assets/
│   ├── architecture_diagram.md
│   └── architecture_mermaid.md
├── configs/
│   └── default.yaml
├── docs/
│   ├── overview.md
│   ├── method.md
│   ├── data.md
│   └── experiments.md
└── notebooks/
    └── demo.ipynb
```

## Installation (Placeholder)

```bash
# TODO: provide package and environment setup instructions
```

## Quick Start (Placeholder)

```bash
# TODO: provide end-to-end demo commands for NV-Rep pipeline
```

## Datasets

NV-Rep is designed for single-cell RNA-seq datasets with emphasis on neuronal subtype heterogeneity and selective vulnerability analyses. Planned benchmark collections include curated GEO datasets spanning healthy and disease-relevant neuronal populations, with attention to class imbalance and cross-cohort transfer settings.

## Evaluation Metrics

- Classification Accuracy
- Macro/Weighted F1 Score
- Cohen's Kappa
- kNN Purity in embedding space
- Bootstrap-based confidence intervals for robustness

## Citation

If you use NV-Rep, please cite:

```bibtex
@software{nv_rep_2026,
  title   = {NV-Rep},
  author  = {Zhang, Luxuan and Jiang, Douglas and Wang, Jaiyi and Yu, Qiyi and Tian, Feng},
  year    = {2026},
  url     = {https://github.com/<org>/NV-Rep}
}
```

## Major Contributors

- Luxuan Zhang
- Douglas Jiang
- Jaiyi Wang
- Qiyi Yu
- Feng Tian

## License

This project is released under the MIT License. See [LICENSE](LICENSE).

## Contact

For collaboration and questions, please open an issue or contact the Feng Tian Lab.
