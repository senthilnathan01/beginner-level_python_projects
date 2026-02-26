# HW3: Distance Geometry and K-means Clustering

**Student**: Senthilnathan T  
**Date**: February 2026

## Changes Summary

### Files Created/Modified

```
HW3_code_senthilnathan_t.ipynb     # Complete notebook implementation
HW3_report_senthilnathan_t.pdf    # Final report
figs_results/                         # All generated figures (10 total)
```

### Generated Figures

All figures saved to `figs_results/` with naming convention: `a3_task{#}_fig{#}_senthilnathan_t.png`

**Task 1** (3 figures):
- `a3_task1_fig1` - Pairwise scatter plot matrix (all 13 features)
- `a3_task1_fig2` - Correlation matrix heatmap
- `a3_task1_fig3` - Box plots by class

**Task 2** (2 figures):
- `a3_task2_fig1` - K-means vs K-medoids comparison (K=2,3,5)
- `a3_task2_fig2` - Initialization effects (3 seeds)

**Task 3** (3 figures):
- `a3_task3_fig1` - kNN decision boundaries (k=3,5)
- `a3_task3_fig2` - Prototype decision boundaries (1,2,3 per class)
- `a3_task3_fig3` - Local vs Global comparison

**Task 4** (2 figures):
- `a3_task4_fig1` - Distance behavior vs dimensionality
- `a3_task4_fig2` - Classification performance vs dimensionality

## Task-by-Task Changes

### Task 1: Data Familiarization
Explored wine dataset structure, correlations, and distributions.

### Task 2: Geometry Through Clustering
Discovered **diagonal separation pattern** in alcohol×color_intensity space using K-means and K-medoids with K=2,3,5.

### Task 3: Prototype Methods for Classification
Compared kNN (local, adaptive boundaries) vs prototypes (global, 6 fixed representatives) along the diagonal.

### Task 4: Curse of Dimensionality
Demonstrated distance concentration (150×→5× ratio) from 2D to 13D while maintaining ~98% accuracy with informative features.
