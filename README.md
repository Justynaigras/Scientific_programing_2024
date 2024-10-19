# Differential gene analysis pipeline using atopic dermatitis data

This repository contains R Markdown file for performing differential gene analysis (DGA) on RNA-seq data. It includes functions for preparing data, conducting statistical analysis, generating quality control plots, and performing pathway enrichment analysis. The code allows for comparing gene expression levels across different conditions, accounting for batch effects, and identifying significantly differentially expressed genes (the analysis is performed using data from a study of atopic dermatitis).

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [License](#license)
- [Contact](#contact)

## Introduction

This project implements a pipeline for differential gene analysis (DGA) on RNA-seq data. It provides a framework for comparing gene expression levels across different experimental conditions, including lesional vs. non-lesional samples, pre-treatment vs. post-treatment samples, and healthy controls vs. baseline samples (all using atopic dermatitis datasets that can be found in the following links [as per the the associated study the dat set were combined]:
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE121212
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE157194).

Pipeline summary:

Data preparation: The code prepares the data for each comparison group, checking missing values duplicates and inconsistencies, as well as correcting batch effect and performing normalization
 
Differential gene analysis: A custom function dga() is implemented using the edgeR package to perform differential gene analysis, considering both group and batch effects. Function dga_up() performs differential gene analysis with up-sampling to correct for imbalances between groups.

Quality control: Functions for generating quality control plots are provided, allowing visualization of genes based on log-fold change and false discovery rate their variability between repetitions.

Pathway enrichment analysis: Gene set pathway enrichment analysis using GO terms for every comparison.

Comparison between baseline AD and after treatment: Mean counts of each group (baseline, healthy, after treatment) of top 20 differentially expressed genes between healthy and AD baseline are visualized. PCA on all differentially expressed genes is also performed.

## Installation

First chunk of the script contains all the necessary packages, please install the ones you don't have. Besides that the script doesn't require any additional Installations. At the end of the script all the plots are saved in appropriate subfolders of Results folder.

## License

Distributed under the MIT License. See `LICENSE` for more information.

## Contact

Justyna Igras - justynkaxl@gmail.com

