# Overview

## Biological Motivation

Neurodegenerative and neuropsychiatric disorders often exhibit selective neuronal vulnerability: specific neuronal subtypes are disproportionately affected while neighboring populations remain relatively resilient. Disentangling this heterogeneity is a core challenge in single-cell transcriptomics, especially when datasets are sparse, imbalanced, and collected across heterogeneous cohorts.

NV-Rep is motivated by the hypothesis that gene-level biological semantics encoded in natural language descriptions can complement expression measurements and improve cell-level representation quality. By integrating textual biological context with quantitative expression signals, NV-Rep aims to produce embeddings that preserve subtle subtype boundaries and vulnerability-associated states.

## Selective Neuronal Vulnerability Context

Selective vulnerability can reflect coordinated molecular programs, stress responses, metabolism, and connectivity signatures. Conventional pipelines based purely on expression similarity may underperform when vulnerability markers are weak, dispersed, or under-sampled.

NV-Rep addresses this by:

- Leveraging language-model-derived gene embeddings to inject prior biological semantics.
- Building cell embeddings from the most informative expressed genes.
- Refining embeddings under supervised contrastive objectives to separate vulnerable and resilient populations.

This design targets robust subtype discrimination and better transferability across studies with limited annotations.
