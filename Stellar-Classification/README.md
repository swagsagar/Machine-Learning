# Stellar Classification: Deep Learning & Algorithmic Benchmarking (SDSS-17)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.0%2B-orange.svg)](https://scikit-learn.org/)
[![ML Framework](https://img.shields.io/badge/Focus-Experimental%20Design-green.svg)](#)


## Interactive Documentation: This project is structured as a self-documenting workflow. The .ipynb notebook follows a logical narrative—integrating data theory, code execution, and visual insights—making it easy for reviewers to follow the end-to-end technical decision-making process.


## Executive Summary
This project implements a robust machine learning pipeline to classify celestial objects—**Stars, Galaxies, and Quasars**—using a dataset of **100,000** observations from the **Sloan Digital Sky Survey (SDSS) Data Release 17**.

The core objective was to conduct a comparative analysis across 8 distinct experimental configurations, specifically evaluating the mathematical impact of **feature scaling** on distance-based algorithms versus tree-based models.

---

## Dataset & Feature Engineering
The dataset comprises 100,000 samples with 17 feature columns. To optimize for high-dimensional efficiency, the following preprocessing steps were executed:

* **Dimensionality Reduction:** Pruned 9 non-predictive metadata features (`obj_ID`, `run_ID`, `plate`, `MJD`, etc.) to reduce noise and prevent overfitting.
* **Astrometric & Photometric Analysis:** Utilized RA/Dec (`alpha`, `delta`) and magnitude filters (`u`, `g`, `r`, `i`, `z`) to identify spectral patterns.
* **Standardization Suite:** Implemented `StandardScaler` to normalize feature variance, ensuring distance-based metrics (kNN) were not biased by feature magnitude.
* **Data Integrity:** Validated class distributions and performed an 80/20 train-test split for rigorous model evaluation.

---

## Experimental Framework
I executed 8 specific experiments to benchmark performance across different mathematical approaches:

###  1. k-Nearest Neighbors (kNN) Suite
* **Baseline:** Unweighted kNN (k=3) on raw data.
* **Distance-Weighted:** Weighted kNN to give more influence to closer neighbors.
* **Normalized Trials:** Re-testing both configurations on scaled data to verify the **Normalization Hypothesis**.

### 2. Decision Trees & Ensemble Methods
* **Decision Tree Classifier:** Evaluated for baseline interpretability.
* **Random Forest Classifier:** Leveraged ensemble bagging to maximize classification accuracy (achieved **>97%**).

---

## Key Technical Insights (FAANG-Style Analysis)
* **The Scaling Effect:** As hypothesized, kNN performance saw significant gains when features were normalized, as it balanced the Euclidean distance contribution of variables like `redshift` against celestial coordinates.
* **Model Invariance:** Empirically demonstrated that tree-based models remained invariant to feature scaling, making them the most robust candidates for production deployment in this domain.
* **Error Analysis:** Confusion matrix analysis revealed that while Star classification is near-perfect, certain Quasars are misclassified as Galaxies due to overlapping redshift profiles—identifying a clear path for future feature engineering.

---

## Tech Stack
* **Language:** Python
* **Libraries:** Scikit-Learn, Pandas, NumPy, Matplotlib, Seaborn
* **Environment:** Jupyter Notebook

---

## Project Structure
```bash
├── Stellar_Classification_SDSS DR-17.ipynb    # Full ML Pipeline (EDA, Preprocessing, Experiments)
├── README.md                   # Project Documentation
