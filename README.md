# Personalized Colorectal Cancer Risk Assessment through Explainable AI and Gut Microbiome Profiling
[![DOI](https://zenodo.org/badge/1029577614.svg)](https://doi.org/10.5281/zenodo.16778479)

![Graphical Abstract](graphical_abstract.png)

## 📄 Paper Information

**Title:** Personalized colorectal cancer risk assessment through explainable AI and Gut microbiome profiling  
**Authors:** Pierfrancesco Novielli, Simone Baldi, Donato Romano, Michele Magarelli, Domenico Diacono, Pierpaolo Di Bitonto, Giulia Nannini, Leandro Di Gloria, Roberto Bellotti, Amedeo Amedei & Sabina Tangaro  
**Journal:** *Gut Microbes*, Volume 17, 2025  
**DOI:** [10.1080/19490976.2025.2543124](https://doi.org/10.1080/19490976.2025.2543124)  
**Published:** August 4, 2025  
**Supplementary Data:**  
- [Training Datasets - Zenodo](https://zenodo.org/...)  
- [Independent Validation Set - GEO (GSE163366)](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE163366)

<p align="center">
<img src="gut_microbes_cover.png" alt="Gut Microbes Cover" width="300"/>
</p>

---

## 🧠 Project Overview

This repository contains the source code and environment specifications used for the analysis presented in the manuscript.  
The goal of the study was to identify explainable microbiome-derived biomarkers for colorectal cancer risk prediction using 16S rRNA data and XAI (SHAP-based) analysis.

The analysis includes:
- Preprocessing of microbiome and metadata
- ML model training (XGBoost, Random Forest, CatBoost)
- Global and local explanation using SHAP
- Embedding and clustering of adenoma patients
- SHAP interaction network analysis

---


## ⚙️ Environment Setup

The analysis was conducted in Python on the following system:

- **Operating System:** macOS 15.6  
- **Python Version:** 3.11.12

To reproduce the computational environment used in the study, we provide a Conda environment file.

### 🛠️ Installation

Make sure you have [Anaconda](https://www.anaconda.com/download) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html) installed. Then:

```bash
# Clone the repository
git clone https://github.com/pierfrancesco2021/Personalized-Colorectal-Cancer-Risk-Assessment.git
cd CRC_microbiome_XAI

# Create environment from YAML
conda env create -f environment.yml

# Activate the environment
conda activate microbiome-crc
```
---

### 📊 SHAP Interaction Network Visualization

The notebook `notebooks/shapInteraction_risk.ipynb` computes and saves:
- **Node matrix** (`nodes.csv`)
- **Link matrix** (`edges.csv`)

These files represent the SHAP-based interaction network and can be directly imported into [Gephi](https://gephi.org/) for interactive visualization and exploration.

