# 📘 **RNA, ATAC & CITE-seq Analysis for https://www.biorxiv.org/content/10.1101/2024.06.06.597775v2**

This repository contains Jupyter notebooks and reproducible scripts used to generate figures for our manuscript. 
The study incorporates single-cell RNA-seq, ATAC-seq, and CITE-seq data from **mouse** and **human bone marrow**, highlighting distinct chromatin and epigenetic states during hematopoietic aging which dictate multilineage potential.

---

## 🧬 Project Overview
We integrated and analyzed multiple datasets to profile hematopoietic stem cells (LT-HSCs) across modalities and species. This includes:

- Mouse multiome single-cell RNA- and ATAC-seq **(this study; GSE246464)**

- Mouse CITE-seq **(Solomon et al. JEM 2024; GSE243197)**

- Human bone marrow scRNA-seq from young and old donors **(Sommarin et al. Biorxiv 2021)**

---

## 🔧 **Data Processing Pipelines**

### 🐭🧪 **RNA-seq (Mouse)**

- **Dataset:** [GSE246464]
- **Input:** `filtered_feature_bc_matrix.h5` files from Cell Ranger
- **Pipeline:** Processed using [shunPykeR](https://github.com/kousaa/shunPykeR) with downstream analysis in Python

### 🐭🧬 **ATAC-seq (Mouse)**

- **Dataset:** [GSE246464]
- **Pipeline:** [ArchR](https://www.archrproject.com/)
- **Key steps:**
  - Generate Arrow files from fragments
  - Filter cells and peaks
  - Dimensionality reduction and clustering
  - Peak calling, gene scoring, and motif enrichment

### 🐭🎯 **CITE-seq (Mouse LSKs)**

- **Dataset:** [GSE243197](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE243197)
- **Pipeline:** Processed using `Scanpy` and/or `Seurat`

### 🧍‍♂🧍‍♀️🎯 **Human Bone Marrow (Young vs. Old)**

- **Dataset:** [OSF Archive](https://osf.io/vdf42/)

---

## 📁 **Repository Structure**

- **Notebooks for RNA analysis**: Notebook for RNA_Analysis.ipynb; Notebook for MAST and MiloR analysis.ipynb
- **Notebook for ATAC analysis**: ArchR_Notebook_Mouse_ATAC.ipynb; Anndata_Notebook_Mouse_ATAC.ipynb
- **Notebook for CITE-seq analysis**: Notebook_Human_CITEseq.ipynb; Notebook_Mouse_CITEseq.ipynb


---

## 📦 **Download Processed Data**

All processed RNA and ATAC datasets are available via Zenodo:

🔗 [**Download from Zenodo**] (https://zenodo.org/uploads/15521122)

---

## 📈 **Figure Reproducibility**

This repository includes all scripts and notebooks needed to recreate key figures:

- UMAPs for RNA, ATAC, and CITE-seq data
- Dot plots and heatmaps for gene and protein expression
- Motif enrichment and peak accessibility analyses
- Aging comparisons (mouse and human)

💡 **To reproduce figures**, use the included Jupyter notebooks. Compatible Python/R environments with all required packages are provided to ensure proper execution.

---
## 📜 **Citation**

Please cite the manuscript and Zenodo dataset if using this resource. Citation details will be added upon publication.


