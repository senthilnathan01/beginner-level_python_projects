# MA 5755 Assignment 2: Geometry, Loss, and Structure in Real Data

## Overview

This assignment explores the California Housing dataset through three fundamental lenses:
1. **Geometry**: How do different learning methods see the same data?
2. **Loss**: What does it mean to predict well?
3. **Dimension**: What happens to local methods in high dimensions?

## Files Included

- `startedHW2.ipynb` - Complete Jupyter notebook with all tasks implemented
- `HW2_report_senthilnathan_t.pdf` - Completed report
- `HW2_taskfile.pdf` - Taskfile

## Setup Instructions

### Prerequisites

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

### Modifying Analysis

Key parameters you can adjust:

**Task 2 (Global vs Local Models):**
```python
knn_small = KNeighborsRegressor(n_neighbors=5)   # Try different k values
knn_large = KNeighborsRegressor(n_neighbors=50)
```

**Task 3 (Loss Functions):**
```python
subset = y[y > y.quantile(0.6)]  # Try different quantiles (0.5, 0.7, 0.8)
```

**Task 4 (Dimensionality):**
```python
dims = [1, 2, 3, 4, 5, 6, 7, 8]  # Add or remove dimensions
sample_size = 2000  # Adjust for speed vs accuracy
```

**Task 5 (Regularization):**
```python
Ridge(alpha=1.0)  # Try different alpha values
Lasso(alpha=0.01)
```

## Assignment Tasks Summary

### Task 1: Data Familiarization
- Explore the California Housing dataset
- Create 2-3 exploratory visualizations
- Understand response variable distribution and feature relationships

### Task 2: Two Ways to Draw a Shape Through Data
- Compare global model (Linear Regression) vs local model (kNN)
- Visualize predictions in 1D/2D
- Analyze how each method "sees" the data

### Task 3: What Does It Mean to Be Right?
- Explore skewed response distribution
- Compare mean vs median predictions
- Analyze squared loss vs absolute loss
- Plot risk curves

### Task 4: When Neighborhoods Stop Being Local
- Study curse of dimensionality
- Measure nearest neighbor distances across dimensions
- Compare kNN vs Linear Regression performance as dimension increases

### Task 5: High-Dimensionality (Optional)
- Explore structured models (Ridge, Lasso)
- Compare with ordinary least squares
- Analyze coefficient shrinkage
- Understand bias-variance tradeoff

## Expected Outputs

After running the notebook, you should have these files stored in figs_results folder:

**9 Figure Files:**
   - `a2_task1_fig1_senthilnathan_t.png` - House value distribution
   - `a2_task1_fig2_senthilnathan_t.png` - Income vs house value scatter
   - `a2_task1_fig3_senthilnathan_t.png` - Correlation matrix
   - `a2_task1_fig4_senthilnathan_t.png` - Scatter Plots
   - `a2_task2_fig1_senthilnathan_t.png` - Global vs local models
   - `a2_task3_fig1_senthilnathan_t.png` - Skewed distribution
   - `a2_task3_fig2_senthilnathan_t.png` - Risk curves
   - `a2_task4_fig1_senthilnathan_t.png` - Curse of dimensionality
   - `a2_task5_fig1_senthilnathan_t.png` - Regularization comparison

**Last Updated**: February 3, 2026
