# Practical Machine Learning - Project 2

## Overview
This repository contains the implementation of Project 2 for the Practical Machine Learning class. The project involves clustering movie plot data using two unsupervised learning methods: **OPTICS** and **BIRCH**. The goal is to explore patterns and group movies based on plot similarities, analyze the results, and compare them to known genres.

## Dataset
The dataset used in this project is the [Wikipedia Movie Plots](https://www.kaggle.com/datasets/jrobischon/wikipedia-movie-plots) dataset. This dataset contains information about movies such as:
- **Release Year**
- **Title**
- **Origin/Ethnicity**
- **Director**
- **Cast**
- **Genre** (used as labels for interpretability)
- **Plot** (used for clustering)

### Dataset Requirements Met:
- The dataset contains more than 1000 samples.
- The dataset is not considered a popular benchmark dataset (e.g., MNIST, CIFAR).
- The dataset includes labels (`Genre`) for comparison with supervised methods.

## Objectives
1. Cluster movies based on plot similarities using:
   - **OPTICS**
   - **BIRCH**
2. Use two different feature representations:
   - Text-based feature representation derived from the `Plot` column.
   - Numeric/tabular feature representation derived from `Release Year`, `Origin/Ethnicity`, `Director`, etc.
3. Compare the clustering results with:
   - Random chance baselines.
   - A supervised baseline model.
4. Interpret the results to understand cluster characteristics and align them with movie genres.

## Project Structure
```
.
|-- data/
|   |-- movie_plots.csv      # Dataset file (downloaded from Kaggle)
|-- notebooks/
|   |-- clustering_optics.ipynb  # Notebook for OPTICS implementation
|   |-- clustering_birch.ipynb   # Notebook for BIRCH implementation
|-- src/
|   |-- feature_engineering.py   # Feature extraction and preprocessing
|   |-- clustering.py            # Clustering methods
|   |-- evaluation.py            # Evaluation metrics and comparisons
|-- results/
|   |-- plots/                   # Visualizations of clusters and performance metrics
|   |-- reports/
|       |-- final_report.pdf     # Final report for the project
|-- README.md
```

## Methods
### Clustering Algorithms
1. **OPTICS**
   - Parameters tuned: `min_samples`, `xi`, `eps`, and distance metric.
   - Suitable for identifying clusters of varying density.
2. **BIRCH**
   - Parameters tuned: `threshold`, `branching_factor`.
   - Efficient for large datasets with hierarchical clustering capabilities.

### Feature Representations
1. **Text-based features**
   - Derived from the `Plot` column using TF-IDF.
2. **Numeric/tabular features**
   - Includes `Release Year`, `Origin/Ethnicity` (one-hot encoded), `Director`, and `Cast`.

### Evaluation
- **Metrics:** Silhouette score, Adjusted Rand Index (ARI), Normalized Mutual Information (NMI).
- **Baselines:**
  - Random chance baseline.
  - Supervised model (e.g., Logistic Regression) to predict `Genre`.

## Results
- **Cluster Insights:**
  - Analysis of how clusters align with known genres.
  - Patterns in plot similarities (e.g., clusters dominated by specific genres or themes).
- **Performance Metrics:**
  - Comparison of clustering performance with and without parameter tuning.
- **Visualization:**
  - 2D or 3D representations of clusters using PCA or t-SNE.

**Contact:** For any questions, reach out to [your email/username].

