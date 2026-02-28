# Data

## Dataset Scope

NV-Rep targets single-cell RNA-seq datasets from GEO with emphasis on neuronal subtype heterogeneity and selective vulnerability.

## Planned GEO Data Characteristics

- Neuronal and glial populations from healthy and disease-relevant tissues.
- Studies with subtype-level labels or high-quality proxy annotations.
- Cohorts with realistic class imbalance and batch heterogeneity.
- Datasets suitable for cross-study label transfer evaluation.

## Data Processing Expectations

Typical preprocessing assumptions for NV-Rep experiments include:

- Quality control (cell and gene filtering)
- Normalization and log transformation
- Feature harmonization across datasets
- Label curation for subtype and vulnerability states

## Reproducibility Notes

Future releases will include explicit accession lists, preprocessing scripts, and configuration manifests to support reproducible benchmark preparation.
