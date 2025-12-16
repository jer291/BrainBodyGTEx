# Detailed Data Guide – Integrative Transcriptomic Analysis of Brain–Body Gene-Expression Aging Using GTEx RNA-Seq Data

**Author:** Jennifer Reed  
**Project:** Brain–Body Aging (GTEx RNA-Seq)

## Objective
This document explains how to download, filter, and prepare GTEx v10 RNA-seq data (53 donors, 3 tissues) for the brain–body aging analysis.

## Folder Structure
```
BrainBody_GTEx/
├── data/
│   ├── GTEx_Analysis_v10_Annotations_SubjectPhenotypesDS.txt
│   ├── GTEx_Analysis_v10_Annotations_SampleAttributesDS.txt
│   ├── GTEx_Analysis_v10_RNASeqCounts_GeneReads.csv
│   ├── metadata_GTEx_subset.csv
│   ├── counts_GTEx_subset.csv
│   └── sample_counts_mock.csv
├── scripts/
│   └── rna_seq_pipeline_brain_aging.py
└── results/
    ├── figures/
    └── tables/
```

## Key Steps
1. Download GTEx v10 open-access metadata and counts.  
2. Apply inclusion criteria: RIN > 5.7, Hardy 1–2, ischemic time < 900, autolysis ≤ 2.  
3. Retain three tissues: Frontal Cortex (BA9), Left Ventricle, Whole Blood.  
4. Export subset as `metadata_GTEx_subset.csv` and `counts_GTEx_subset.csv`.

## Mock Dataset
If data access fails, use `sample_counts_mock.csv`, generated automatically by the pipeline.

## Troubleshooting
| Issue | Cause | Fix |
|--------|--------|-----|
| File too large | GTEx counts exceed Excel limits | Use Python filtering |
| Memory error | Not enough RAM | Use top 10,000 genes |
| Missing donors | Filters incorrect | Recheck metadata filters |

## Final Checklist
- [x] GTEx files downloaded  
- [x] Filters applied and validated  
- [x] Donor count verified (53)  
- [x] Clean subset exported  
- [x] Mock dataset functional
