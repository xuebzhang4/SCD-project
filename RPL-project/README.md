snRNA-seq Analysis of Hypothalamic and Hippocampal Transcriptomes
This repository contains the source code for the snRNA-seq analysis presented in the manuscript: "Rest-phase light disrupts hippocampal clock function and impairs object recognition memory" (Zhang et al., 2026).
Overview
This project provides a complete bioinformatics pipeline for analyzing single-nucleus RNA-sequencing data from mouse hypothalamus (HY) and hippocampus (HIP), focusing on:

SCN clock organization and output signaling

Hippocampal DEGs and GO term (Active vs. Rest phase) under Ctrl condition

Phase-dependent synaptic gene expression in DG, CA1, and CA3 neurons

HY and HIP tissues were collected from the same animals under control (Ctrl) or rest-phase light (RPL) conditions.

Repository Structure

HIP_snRNA-seq/                                    # Hippocampus analysis
├── Data_analysis/
│   ├── Dot plot presenting number of nuclei expressing clock gene in the seven HIP cell types
│   ├── Dot plot presenting the expression of excitatory and inhibitory neuronal marker in DG, CA1, and CA3
│   ├── Dot plot presenting the expression of HIP cell-type markers
│   ├── Dot plots presenting the expression of HIP neuronal markers
│   └── Proportions of seven cell types in the HIP
│   ├── Ridge plots showing clock gene-expressing nuclei in the DG, CA1, and CA3
│   ├── UMAP of seven HIP cell types
│   └── UMAP of six HIP neuronal subclusters
│   ├── UMAPs identifying nuclei expressing clock genes in the HIP
│   └── UMAPs visualizing nuclei expressing clock genes in HIP neuronal subclusters
└── Function_analysis/
    ├── DEGs and GO term in DG, CA1, and CA3
    ├── Heatmap of DEGs in excitatory neurons under Ctrl condition
    └── UMAP of the subclusters in DG, CA1, and CA3
    └── UMAPs identifying nuclei expressing the selected DEGs

HY_snRNA-seq/                                     # Hypothalamus analysis
├── Data_analysis/
│   ├── Dot plot presenting number of nuclei expressing clock gene in the six HY cell types
│   ├── Dot plot presenting the expression levels of HY cell-type markers
│   ├── Dot plot presenting the expression levels of HY neuronal markers
│   ├── Proportions of six cell types in the HY
│   └── Rigge plots visualizing the distribution of clock gene expression in HY neuronal subclusters
    ├── UMAP of five HY neuronal subclusters
│   ├── UMAP of six HY cell types
│   ├── UMAPs identifying nuclei expressing clock genes in the six HY cell types
│   └── UMAPs visualizing nuclei expressing clock genes in HY neuronal subclusters
└── Function_analysis/
    ├── The topology of signaling mediated by neuropeptide-receptor between HY neuronal subclusters

Dependencies

The analysis was performed using R (version 4.3.1) . Key R packages required:

Seurat (version 4.3.0.1) - snRNA-seq data processing

DoubletFinder (version 2.0.3) - Doublet detection

clusterProfiler (version 4.0) - GO enrichment analysis

org.Mm.eg.db - Mouse gene annotation

ggplot2, pheatmap, UpSetR - Visualization

dplyr, tidyverse - Data manipulation

Usage
To reproduce the analysis, clone this repository and run the scripts in numerical order. Ensure that the raw data (or count matrix) and metadata are placed in the correct working directory as specified in the scripts.

Contact
For any questions regarding the code, please open an issue.