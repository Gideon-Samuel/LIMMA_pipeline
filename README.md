# LIMMA Differential Expression Pipeline

This repository contains an **R Markdown pipeline** for performing differential expression (DE) analysis on microarray or RNA-seq datasets using the **LIMMA** package. The pipeline retrieves data from **GEO** (Gene Expression Omnibus), preprocesses it, performs DE analysis, and visualizes results with PCA and heatmaps.

---

## Features

- Download and process GEO datasets using `GEOquery`.
- Subset samples by experimental groups (e.g., Control vs Treated).
- Filter low-variance genes.
- Build a design matrix for LIMMA linear modeling.
- Fit linear models and compute contrasts for DE analysis.
- Identify top upregulated and downregulated genes.
- Visualize sample clustering using PCA.
- Heatmap of top variable genes.

---

## File Structure

- `LIMMA_pipeline.Rmd` : The main R Markdown pipeline.
- `LIMMA_pipeline.html` : (Optional) Knit HTML version for viewing results.
- `README.md` : This file.

---

## Requirements

- **R** (>= 4.0)
- **R packages**:
  ```r
  install.packages(c("ggplot2", "pheatmap", "matrixStats"))
  if (!requireNamespace("BiocManager", quietly = TRUE))
      install.packages("BiocManager")
  BiocManager::install(c("GEOquery", "limma"))
