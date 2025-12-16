# BrainBodyGTEx

**Integrative Transcriptomic Analysis of Brain–Body Gene-Expression Aging Using GTEx RNA-Seq Data**  
*Author: Jennifer Reed (Harvard University, Bioinformatics Final Project)*  
*Date: December 2025*  

---

## 🧠 Project Overview

This repository contains all code, figures, and documentation for a computational study examining how **aging influences coordinated brain–body gene-expression networks**.  

Using open-access **GTEx v10** RNA-seq data, the project integrates **transcriptomic signatures** across the brain (frontal cortex), heart (left ventricle), and blood to explore systemic molecular pathways that shape **neural resilience vs. neurodegenerative decline**.  

Two complementary bioinformatics frameworks were applied:
- **Differential expression analysis** (DESeq2-style) to quantify gene-level changes with age.  
- **Network-based co-expression analysis** (WGCNA-style) to identify age-related gene modules and cross-tissue connectivity.  

Together, these analyses reveal shared molecular pathways — including **mitochondrial function**, **immune activation**, and **extracellular remodeling** — that link peripheral aging processes to the molecular architecture of the aging brain.  

---

## ⚙️ Workflow Summary

1. **Data Acquisition & Preprocessing**  
   - Open-access RNA-seq and phenotype data obtained from GTEx v10 (non-protected datasets).  
   - Quality control: FastQC → Trimmomatic.  
   - Alignment: HISAT2.  
   - Gene quantification: featureCounts.  

2. **Pipeline A – Differential Expression Framework**  
   - Differential modeling using DESeq2-style statistical analysis.  
   - Age-associated genes identified per tissue.  
   - Cross-tissue correlations and pathway enrichment analyses performed.  

3. **Pipeline B – Co-Expression Network Framework**  
   - Variance-stabilized expression data used for WGCNA-style network analysis.  
   - Detection of age-correlated modules across brain, heart, and blood.  
   - Biological interpretation of modules using enrichment results from Pipeline A.  

4. **Integration (A + B)**  
   - Cross-comparison of DESeq2 and WGCNA outputs revealed strong convergence of biological themes.  
   - Shared pathways include mitochondrial dysfunction, inflammatory signaling, and vascular remodeling — providing an integrated view of **systemic and neural aging**.  

---

## 📁 Repository Structure

```plaintext
BrainBodyGTEx/
├── Design/                          
│   └── [Figure design assets and layout files]
│
├── Old/                             
│   └── [Archived drafts and previous versions]
│
├── Project notes/                   
│   └── [Research notes, planning documents, and annotations]
│
├── Submitted/                       
│   └── [Final project submission files for course or review]
│
├── VideoFigures/                    
│   ├── figure1b_heatmap.png
│   ├── figure2a_dendrogram.png
│   └── figure2b_overlap_heatmap.png
│
├── BrainBodyGTEx_DataGuide.md        # Data preparation, filtering, and metadata overview
├── BrainBodyGTEx_ExecutionGuide      # Step-by-step pipeline execution instructions
├── BrainBodyGTEx_Figure1             # Master file for Figure 1 (conceptual + correlation plots)
├── BrainBodyGTEx_Figure2             # Master file for Figure 2 (network integration analysis)
├── BrainBodyGTEx_Notebook.ipynb      # Jupyter notebook for integrated analysis
├── BrainBodyGTEx_Paper_v8            # Final bioinformatics paper (v8)
├── BrainBodyGTEx_PresentationPDF     # Final presentation PDF (used for recording/submission)
├── BrainBodyGTEx_Proposal            # Original or refined proposal document
├── BrainBodyGTEx_Table1              # Summary table of WGCNA modules and overlap results
├── README.md                         # Repository overview and metadata
├── rna_seq_pipeline_brain_aging      # Python script implementing main transcriptomic analysis
└── ScientificReview_Coordinated_Gene_Expression_Aging_Across_Brain_and_Peripheral_Tissues_GTEx
                                      # Anchor research paper providing theoretical background
```

---

## 🖼️ Key Figures
- **Figure 1:** Conceptual overview of transcriptomic × aging pipelines, cross-tissue age correlation, and shared pathway enrichment.  
- **Figure 2:** Integration of gene-level (DESeq2) and network-level (WGCNA) analyses, demonstrating convergence on shared biological networks linking peripheral and neural aging.  

All figures used in the presentation and paper are stored under `/VideoFigures/`.

---

## 🧾 Presentation

🎥 **Live Interactive Presentation:**  
[https://brain-body-atlas.lovable.app/](https://brain-body-atlas.lovable.app/)  

📘 **Presentation PDF:**  
`BrainBodyGTEx_PresentationPDF` – full static version of slides used in the recording.  

---

## 🧪 Tools and Dependencies
- Python ≥ 3.10  
- pandas, numpy, scipy, seaborn, matplotlib, networkx  
- Compatible with Linux or Harvard FAS Research Cluster environments  

---

## 🔗 References

- GTEx Consortium. (2020). *The GTEx transcriptomic landscape of human tissues.* *Science, 369*(6509), 1318–1330.  
- Izgi, H., Sanchez, K., & van Heerden, A. (2022). *Pan-tissue transcriptome analysis reveals sex-dimorphic human aging.* *eLife, 11*, e102449.  
- Yang, J., Huang, T., & Zhou, L. (2015). *Synchronized age-related gene-expression changes across multiple tissues in humans.* *Scientific Reports, 5*, 13389.  
- Briller, D., Chen, M., & Li, Y. (2025). *A computational framework for detecting inter-tissue gene-expression coordination changes with aging.* *Scientific Reports.*  
- Oh, J., Choi, E., & Lee, S. (2023). *Organ-specific plasma proteome aging signatures and systemic predictors of cognitive decline.* *Nature, 619*, 312–326.  
- Tan, L., Gao, Y., & Zhou, J. (2023). *Peripheral inflammation and brain aging: mechanisms and biomarkers.* *Frontiers in Aging Neuroscience, 15*, 1134.  

---

## 🪪 License
This project is distributed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** License.  
You are free to share and adapt the material for any purpose, provided proper credit is given to the author.  
See: [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)  

---

## 💡 Author Notes
This repository represents the final deliverable for the Harvard Bioinformatics Final Project and serves as a foundation for future integrative transcriptomic and brain–body resilience research under **Pelorias / Resilora**.  

Feedback and collaborations are welcome — please cite appropriately or contact via GitHub.  
