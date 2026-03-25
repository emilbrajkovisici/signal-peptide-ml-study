# Signal Peptide Prediction with Interpretable Machine Learning

<p align="center">
  <b>Lightweight, interpretable models can rival deep learning in biological sequence analysis</b>
</p>

<p align="center">
  <a href="#"><img src="https://img.shields.io/badge/python-3.10-blue"></a>
  <a href="#"><img src="https://img.shields.io/badge/license-MIT-green"></a>
  <a href="#"><img src="https://img.shields.io/badge/status-research-orange"></a>
  <a href="#"><img src="https://img.shields.io/badge/reproducibility-yes-brightgreen"></a>
</p>

---

##  Abstract

This repository provides a fully reproducible pipeline for signal peptide prediction using interpretable machine learning.
We demonstrate that biologically motivated feature engineering—combined with a simple logistic regression model—achieves strong performance without relying on deep neural architectures.

Our results suggest that, in certain bioinformatics tasks, carefully designed features may be as effective as complex models while offering improved interpretability.

---

##  Key Contributions

*  Interpretable feature design grounded in protein biology
*  Explicit modeling of N-terminal signal properties
*  Competitive performance without deep learning
*  Fully reproducible experimental pipeline
*  Detailed ablation study and feature importance analysis

---

##  Repository Structure

```id="repo_tree"
.
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── 01_data_preparation.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_model_training.ipynb
│   └── 04_evaluation.ipynb
├── src/
├── results/
│   └── figures/
├── requirements.txt
└── README.md
```

---

##  Method Overview

We model protein sequences as feature vectors:

* **Amino Acid Composition (AAC)**
* **Global physicochemical properties**
* **N-terminal signal peptide proxies**

A logistic regression classifier is trained on these features:

```math
P(y=1 \mid x) = \sigma(w^T x + b)
```

This enables:

* direct interpretability
* feature attribution
* biological insight

---

##  Quick Start

### 1. Clone repository

```bash id="clone_cmd"
git clone git@github.com:emilbrajkovisici/signal-peptide-ml-study.git
cd signal-peptide-ml-study
```

### 2. Install dependencies

```bash id="install_cmd"
pip install -r requirements.txt
```

### 3. Run pipeline

Execute notebooks in order:

```id="run_order"
01_data_preparation.ipynb
02_feature_engineering.ipynb
03_model_training.ipynb
04_evaluation.ipynb
```

---

##  Results

| Metric   | Value |
| -------- | ----- |
| Accuracy | ~0.91 |
| ROC-AUC  | ~0.95 |
| PR-AUC   | ~0.92 |

---

##  Generated Outputs

All results are automatically saved:

```id="outputs"
results/
├── metrics.json
├── test_predictions.csv
├── feature_coefficients.csv
└── figures/
```

### Figures include:

* ROC curve
* Confusion matrix
* Feature importance
* Distributional analysis

---

##  Reproducibility

This repository is designed for full reproducibility:

* Fixed random seeds
* Deterministic pipeline
* Transparent feature engineering
* No hidden preprocessing steps

---

##  Data

Supported formats:

* FASTA sequences (`data/raw/`)
* Precomputed CSV datasets (`data/processed/`)

---

##  Limitations

* No sequence identity filtering
* Dataset derived from annotation-based labels
* Linear model assumptions

---

##  Future Work

* Transformer-based sequence models
* Hybrid interpretable + deep approaches
* Cross-organism generalization
* Improved biological validation

---

##  Citation

If you use this work, please cite:

```bibtex
@article{batistabrajkovic2026signal,
  title={Interpretable Machine Learning for Signal Peptide Detection},
  author={Batista,Jadranko;Brajković, Emil},
  year={2026}
}
```

---

##  Author

Jadranko Batista
Emil Brajković

---

##  License

MIT License

---

##  Acknowledgments

* UniProt database
* BioPython library
* scikit-learn ecosystem

---
