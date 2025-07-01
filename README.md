
# fma-dimension-reduction
## Course: CS6140 – Machine Learning (Fall 2024)

### Author: *Reena Sajad Hyder*  

---

## 📌 Objective

This project builds upon Part 1 (fma-feature-explorer) by applying **dimensionality reduction techniques** to the Free Music Archive (FMA) dataset. The goal is to reduce the complexity of high-dimensional audio features while preserving meaningful patterns, enabling better visualization and clustering in later analysis.

---

## 🧠 Background

Dimensionality reduction helps simplify high-dimensional data by transforming it into a lower-dimensional space. This preserves important structures in the data and reduces noise and redundancy. It is essential for improving computational efficiency and visualization.

Techniques used in this project:
- **Principal Component Analysis (PCA)**
- **Uniform Manifold Approximation and Projection (UMAP)**
- **t-SNE (optional)**
- **Locally Linear Embedding (LLE)**
- **ISOMAP**

---

## 🔧 Tasks Performed

### 1. Data Preparation
- Selected domains: `chroma`, `mfcc`, `spectral`, `tonnetz`
- Cleaned and preprocessed feature data
- Standardized features using techniques like `StandardScaler`

### 2. Dimensionality Reduction Techniques
Each technique was applied independently to each domain to reduce to:
- **2D and 3D projections** (except PCA, which also analyzed variance)

Techniques were implemented using `scikit-learn` and `umap-learn`.

### 3. Visualization
- 2D and 3D scatter plots were generated for each method
- Data points were color-coded by `genre_top` to observe clustering patterns

### 4. Correlation Analysis
- Calculated pairwise correlations between reduced dimensions
- Identified high correlations or redundancies in projected dimensions

### 5. Comparative Analysis
Each method was evaluated based on:
- Visual separation of genres
- Preservation of global and local structure
- Dimensional correlation patterns
- Interpretability of projections

---

## 📊 Techniques Summary Table

| Method | Strengths | Limitations |
|--------|-----------|-------------|
| PCA | Fast, preserves global variance | Linear only, less effective for nonlinear structures |
| UMAP | Preserves local & global structure, fast | Stochastic, can vary between runs |
| t-SNE | Excellent local cluster separation | Poor global structure, slow |
| LLE | Captures local geometry | Sensitive to noise |
| ISOMAP | Preserves global structure | Slower, struggles with disconnected manifolds |

---

## 🛠 Files Included

- `fma-dimension-reduction.ipynb` – Main notebook for dimension reduction, visualization, and analysis.
- `HW Assignment 4 Unsupervised Learning Part 2.docx` – Assignment instructions.

---

## ✅ Summary

This project demonstrates how various dimensionality reduction techniques uncover latent structures in the FMA dataset. The analysis provides a foundation for clustering, anomaly detection, or genre prediction tasks in future work.
