# BrainBodyGTEx

**Integrative Transcriptomic Analysis of Brain–Body Gene-Expression Aging Using GTEx RNA-Seq Data**  
*Author: Jennifer Reed (Harvard University, Bioinformatics Final Project)*  
*Date: December 2025*

---

## 🧬 Project Overview
This repository contains all code, documentation, and results for a computational analysis exploring how aging shapes gene-expression coordination between the human brain and peripheral tissues (heart and blood).  

The project implements two complementary RNA-seq analysis pipelines using open-access **GTEx v10** data:  
- **Pipeline A:** Differential expression analysis using DESeq2-style modeling.  
- **Pipeline B:** Co-expression network analysis using WGCNA-style clustering.  

Together, these frameworks reveal consistent molecular signatures of aging—decline in mitochondrial/synaptic function and upregulation of immune and structural pathways—demonstrating coordinated brain–body aging.

---

## 📂 Repository Structure
```
BrainBodyGTEx/
├── data/                       # Processed GTEx data subsets (open-access metadata only)
├── scripts/                    # Python analysis scripts
│   └── rna_seq_pipeline_brain_aging.py
├── notebooks/                  # Jupyter notebook for combined workflow
│   └── BrainBodyGTEx_Notebook.ipynb
├── results/
│   ├── figures/                # Figures 1–2 (PNG)
│   └── tables/                 # Table 1 summary (CSV)
├── documentation/
│   ├── BrainBodyGTEx_Data_Guide.md
│   ├── BrainBodyGTEx_Execution_Guide.docx
│   └── Bioinformatics_Final_Paper_JReed_v7.docx
└── presentation/
    └── BrainBodyGTEx_Presentation.pptx
```

---

## ⚙️ Workflow Summary
1. **Preprocessing:** FastQC → Trimmomatic → HISAT2 → featureCounts  
2. **Pipeline A:** Differential expression modeling in DESeq2 framework  
3. **Pipeline B:** WGCNA module detection using variance-stabilized counts  
4. **Integration:** Cross-validation of DESeq2 and WGCNA outputs → shared aging pathways  

For additional detail, see:  
- *BrainBodyGTEx_Data_Guide.md* – sample filtering and preprocessing  
- *BrainBodyGTEx_Execution_Guide.docx* – pipeline steps and commands  
- *Bioinformatics_Final_Paper_JReed_v7.docx* – full manuscript and figures  

---

## 🧠 Results Summary
- **Tissues analyzed:** Frontal cortex (BA9), Heart (left ventricle), Whole blood  
- **Sample size:** 53 donors, ages 20–79  
- **Key findings:**  
  - Downregulated mitochondrial/synaptic genes with age  
  - Upregulated immune/ECM pathways  
  - 65% overlap between DESeq2 and WGCNA age modules  

---

## 🧰 Tools and Dependencies
- Python ≥ 3.10  
- pandas, numpy, scipy, seaborn, matplotlib, networkx  
- Compatible with standard Linux or Harvard FAS Research Cluster environments  

---

## 🔗 Citation
If you reference this project or reuse its methodology, please cite:
> Reed, J. (2025). *Integrative Transcriptomic Analysis of Brain–Body Gene-Expression Aging Using GTEx RNA-Seq Data.* Harvard University, Bioinformatics Final Project.  
> GTEx Consortium. (2020). *The GTEx transcriptomic landscape of human tissues.* Science, 369(6509), 1318–1330.

---

## 🪪 License
Distributed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** License.  
You are free to share and adapt the material for any purpose, provided proper credit is given to the author.

---

## 💡 Author Notes
This project serves as both a capstone for Harvard’s Bioinformatics course and a foundation for future integrative molecular studies under **Pelorias/Resilora**.  
Feedback and collaborations are welcome—please cite appropriately and contact via GitHub or academic email.
