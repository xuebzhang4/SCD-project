# snRNA-seq Analysis of Hypothalamic and Hippocampal Transcriptomes

This repository contains the source code for the single-nucleus RNA-sequencing (snRNA-seq) analysis presented in the manuscript:  
**"Rest-phase light disrupts hippocampal clock function and impairs object recognition memory"** (Zhang et al., 2026).

---

## Overview

This project provides a complete bioinformatics pipeline for analyzing snRNA-seq data from mouse hypothalamus (HY) and hippocampus (HIP) tissues collected from the same animals under **Control (Ctrl)** or **Rest-Phase Light (RPL)** conditions.

Key analytical focuses include:
- Suprachiasmatic nucleus (SCN) clock organization and output signaling dynamics.
- Hippocampal differentially expressed genes (DEGs) and Gene Ontology (GO) terms across phases (Active vs. Rest phase) under the Ctrl condition.
- Phase-dependent synaptic gene expression alterations in Dentate Gyrus (DG), CA1, and CA3 neurons.

---

## Repository Structure

```text
.
├── HIP_snRNA-seq/                                # Hippocampus Analysis
│   ├── Data_analysis/
│   │   ├── Dot plot presenting number of nuclei expressing clock genes in seven HIP cell types
│   │   ├── Dot plot presenting expression of excitatory and inhibitory neuronal markers in DG, CA1, and CA3
│   │   ├── Dot plot presenting expression of HIP cell-type markers
│   │   ├── Dot plots presenting expression of HIP neuronal markers
│   │   ├── Proportions of seven cell types in HIP
│   │   ├── Ridge plots showing clock gene-expressing nuclei in DG, CA1, and CA3
│   │   ├── UMAP of seven HIP cell types
│   │   ├── UMAP of six HIP neuronal subclusters
│   │   ├── UMAPs identifying nuclei expressing clock genes in HIP
│   │   └── UMAPs visualizing nuclei expressing clock genes in HIP neuronal subclusters
│   └── Function_analysis/
│       ├── DEGs and GO term enrichment in DG, CA1, and CA3
│       ├── Heatmap of DEGs in excitatory neurons under Ctrl condition
│       ├── UMAP of subclusters in DG, CA1, and CA3
│       └── UMAPs identifying nuclei expressing selected DEGs
│
└── HY_snRNA-seq/                                 # Hypothalamus Analysis
    ├── Data_analysis/
    │   ├── Dot plot presenting number of nuclei expressing clock genes in six HY cell types
    │   ├── Dot plot presenting expression levels of HY cell-type markers
    │   ├── Dot plot presenting expression levels of HY neuronal markers
    │   ├── Proportions of six cell types in HY
    │   ├── Ridge plots visualizing clock gene expression distribution in HY neuronal subclusters
    │   ├── UMAP of five HY neuronal subclusters
    │   ├── UMAP of six HY cell types
    │   ├── UMAPs identifying nuclei expressing clock genes in six HY cell types
    │   └── UMAPs visualizing nuclei expressing clock genes in HY neuronal subclusters
    └── Function_analysis/
        └── Topology of signaling mediated by neuropeptide-receptors between HY neuronal subclusters

## Dependencies
The analysis was performed using R (version 4.3.1). Key required R packages include:

Seurat (v4.3.0.1) – snRNA-seq data processing

DoubletFinder (v2.0.3) – Doublet detection

clusterProfiler (v4.0) – GO enrichment analysis

org.Mm.eg.db – Mouse gene annotation

ggplot2, pheatmap, UpSetR – Data visualization

dplyr, tidyverse – Data manipulation
