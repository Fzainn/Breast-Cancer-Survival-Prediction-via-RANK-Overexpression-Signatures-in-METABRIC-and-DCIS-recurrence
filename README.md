**Description**

This repository contains the code and analysis for evaluating the prognostic value of gene signatures derived from RANK overexpression in luminal epithelial cells in breast cancer survival. The analysis is performed using the METABRIC dataset, a comprehensive resource for breast cancer genomics and clinical data. The goal is to confirm whether RANK-associated gene signatures can predict patient survival outcomes and serve as potential biomarkers for breast cancer prognosis.

**Overview**

1- **Gene Signature Derivation:**  Identification of gene signatures associated with Differentially expressed genes between WT luminal and Rank +/tg luminal MECS.
2- **METABRIC Dataset:**  Integration of gene expression and clinical data from the METABRIC cohort for validation.
3-**Visualization:** Generation of survival plots, hazard ratios, and p-values for individual genes and the combined RANK signature score.
4- **Reproducible Workflow:** R scripts for data preprocessing, survival analysis, and visualization, ensuring reproducibility and transparency.

**Key Steps**

1- **Data Preprocessing:** 
* Load and clean RANK expression data (mmc2.xlsx).
* Filter for differentially expressed genes (DEGs) with adj.P.Val < 0.05 and |logFC| > 1.
* Classify genes as upregulated or downregulated based on logFC.

2- **METABRIC Data Integration:**
* Load METABRIC gene expression and clinical data.
* Remove duplicates and aggregate gene expression values.
* Merge gene expression data with clinical data for survival analysis.

3- **Survival Analysis:**
* Perform univariate Cox regression to identify significant predictors of survival.
* Apply Benjamini-Hochberg correction for multiple testing.
* Generate Kaplan-Meier curves for significant genes and the RANK signature score.

4- **Visualization:**
* Create Volcano plots and bar plots for DEGs.
* Generate Kaplan-Meier curves for survival analysis.
* Save all plots as individual PDFs and a combined PDF (Myplots.pdf).


**Dependencies**
The following R packages are required:
* biomaRt
* survival
* survminer
* readxl
* ggplot2
* dplyr
* tibble
* gridExtra

**Results**

* **Significant Genes:** A list of genes significantly associated with survival, along with their hazard ratios and p-values.
* Kaplan-Meier Curves: Visualizations of survival differences between high and low expression groups for significant genes and the RANK signature score.
* Volcano Plot: Visualization of differentially expressed genes.
* Bar Plot: Distribution of upregulated and downregulated genes.


