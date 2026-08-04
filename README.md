[![Open in Hugging Face](https://img.shields.io/badge/Open%20in%20Hugging%20Face-Analysis--Notebook-black?style=flat&logo=huggingface&logoColor=FFD21E)](https://huggingface.co/datasets/QasimHussain/viral_cancer_tcga/blob/main/TCGA_Viral_Etiology_Analysis.Rmd) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

![Volcano Plot](https://huggingface.co/datasets/QasimHussain/viral_cancer_tcga/resolve/main/figures/Volcano_Plot_Viral_vs_NonViral.png)
# TCGA Viral Etiology in Hepatocellular Carcinoma
## Overview

Comprehensive transcriptomic analysis comparing **viral** (HBV/HCV) versus **non-viral** hepatocellular carcinoma (HCC) using The Cancer Genome Atlas (TCGA-LIHC) dataset.

## Analysis Pipeline

1. **Data Loading & QC** - Patient ID standardization, viral status classification
2. **Differential Expression** - DESeq2 negative binomial modeling
3. **Pathway Enrichment** - KEGG & GO gene set enrichment analysis
4. **Survival Analysis** - Cox proportional hazards, Kaplan-Meier curves
5. **Visualizations** - Publication-quality figures

## Installation & Usage

### Prerequisites
- R 4.5+
- See `install_packages.R` for dependencies

### Quick Start
```r
# Install packages
source("install_packages.R")

# Run analysis
rmarkdown::render("TCGA_Viral_Etiology_Analysis.Rmd")
```

## Repository Structure

```
├── TCGA_Viral_Etiology_Analysis.Rmd  # Main analysis
├── install_packages.R                         # Setup
├── data/                                      # Input files
├── results/                                   # CSV outputs
└── figures/                                   # Visualizations
```

## Key Results Visualizations

### 1. PCA of Gene Expression
![PCA Plot](https://huggingface.co/datasets/QasimHussain/viral_cancer_tcga/resolve/main/figures/PCA_Plot.png)

### 3. Top 50 Differentially Expressed Genes (Heatmap)
![Heatmap Top 50 DEGs](https://huggingface.co/datasets/QasimHussain/viral_cancer_tcga/resolve/main/figures/Heatmap_Top50_DEGs.png)

### 4. Top Genes Expression (Boxplots)
![Top Genes Boxplots](https://huggingface.co/datasets/QasimHussain/viral_cancer_tcga/resolve/main/figures/Top_Genes_Boxplots.png)

### 6. MA Plot
![MA Plot](https://huggingface.co/datasets/QasimHussain/viral_cancer_tcga/resolve/main/figures/MA_Plot.png)

**Data Source**: [TCGA-LIHC](https://portal.gdc.cancer.gov/)
