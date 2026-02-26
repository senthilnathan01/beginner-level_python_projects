# HW4: Probabilistic Clustering and Gaussian Mixture Models
**MA 5755 — Data Analysis & Visualization in R/Python/SQL**

**Author:** Senthilnathan T, ED21B057

**Date:** 23 February 2026

---

## Task 1 — k-Means vs Spherical GMM vs Full-Covariance GMM

**Figures added:**
- `a4_task1_fig1_senthilnathan_t.png` — True species labels scatter plot (Versicolor vs Virginica)
- `a4_task1_fig2_senthilnathan_t.png` — Three-subplot cluster assignments (k-Means | Spherical GMM | Full-Cov GMM) with shaded decision regions, dashed decision boundary, and red-star centroids/means

---

## Task 2 — Soft vs Hard Assignments and Uncertainty Quantification

**Figures added:**
- `a4_task2_fig1_senthilnathan_t.png` — Three-panel uncertainty figure:
  - *Left:* Continuous certainty gradient per point ($\max_k \gamma_{ik}$), red → blue
  - *Centre:* Uncertain points (max posterior < 0.8) flagged as yellow diamonds (5 points)
  - *Right:* k-Means vs Full-Cov GMM assignment agreement — green (98 agree) vs red diamonds (2 disagree)
