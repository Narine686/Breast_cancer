# Breast Cancer Transcriptomic Analysis

This repository contains the RMarkdown code used to perform:

* Differential Expression Analysis (DEA)
* Functional Enrichment Analysis (FEA)
* Location Enrichment Analysis

using breast cancer samples and healthy breast tissue samples. The code filters for triple negative samples.

## Data

The analysis uses open-access data from the TCGA-BRCA project available through the Genomic Data Commons (GDC) Data Portal.

Data download requires the GDC Data Transfer Tool (`gdc-client`).

## Requirements

### Software

* R / RStudio
* GDC Data Transfer Tool (`gdc-client`)

### R packages

* TCGAbiolinks
* edgeR
* geneplotter
* limma
* sva
* dplyr
* ggplot2
* tidyr
* rlist
* openxlsx
* SummarizedExperiment
* AnnotationDbi
* org.Hs.eg.db
* GOstats

## Workflow

The analysis should be performed in the following order:

1. `breast_DEA.Rmd`

   * Downloads and preprocesses TCGA-BRCA data
   * Performs Differential Expression Analysis (DEA)

2. `Breast_FEA.Rmd`

   * Performs functional enrichment analysis using the differential expression results
   * Performs location enrichment analysis using the differential expression results

## Output

The workflow generates tables and visualizations describing differentially expressed genes, enriched biological functions and enriched locations associated with breast cancer samples.

## License

This project is licensed under the MIT License.
