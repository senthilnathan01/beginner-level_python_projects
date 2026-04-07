# HW7: Bayesian and Nonparametric Regression with Gaussian Processes

This repository contains the completed notebook implementation, exported figures, and LaTeX report source for HW7 in MA 5755.

## Higher-Level Goal

We study how different regression assumptions shape predictions on the Airfoil Self-Noise dataset. The progression is intentional:

1. Linear regression tests a single global relationship.
2. Polynomial regression increases flexibility and exposes overfitting.
3. Ridge regression shows how regularization stabilizes high-degree fits.
4. Cross-validation is used to choose complexity based on generalization.
5. Kernel ridge regression shifts from global basis functions to local similarity.
6. Gaussian Process regression adds both local modeling and predictive uncertainty.

The broader aim is to understand not just which model performs best, but why different inductive biases lead to different fitted functions, stability, and interpretability.

## What Was Done

The notebook:

- uses all five input features from the Airfoil Self-Noise dataset,
- takes `frequency` as the primary visualization variable,
- fixes the remaining features at their training-set mean values for plotting,
- standardizes both `X` and `y` during fitting,
- converts predictions back to original `pressure` units for plots and MSE reporting,
- uses a `70/30` train-validation split with `random_state=42`,
- uses `5`-fold cross-validation for Task 4 model selection.

## Main Results

| Model | Selected setting | Validation MSE | Validation R^2 | Interpretation |
| --- | --- | ---: | ---: | --- |
| Linear regression | all original features | 23.688 | 0.498 | Underfits and captures only a global trend |
| Polynomial regression | degree 4 | 8.565 | 0.819 | Best unregularized polynomial balance |
| Ridge regression | degree 4, alpha = 0.01 | 8.449 | 0.821 | Slightly improves generalization over plain degree-4 polynomial |
| Kernel ridge regression | alpha = 0.01, gamma = 1.0 | 4.860 | 0.897 | Strong local fit without the instability of high-degree polynomials |
| Gaussian Process regression | optimized RBF + white noise kernel | 4.456 | 0.906 | Best holdout model and the only one with uncertainty bands |

## Theoretical Takeaways

- Linear models are too rigid for this dataset because the relationship between `frequency` and `pressure` is not globally linear.
- Increasing polynomial degree improves fit up to a point, then sharply increases variance.
- Ridge regularization reduces the instability of degree-6 polynomials by shrinking extreme coefficients.
- Cross-validation correctly rejects overly complex models that look good only on training data.
- Kernel methods work well because they respond to nearby observations rather than forcing one global functional form.
- Gaussian Processes go one step further by producing both a mean prediction and an uncertainty estimate, which is useful when the slice moves through regions with different local data support.

## Overall Result

The final conclusion is that the optimized Gaussian Process is the best model for this dataset among the methods tested. It gives the lowest validation MSE, the highest validation `R^2`, and adds uncertainty quantification that the deterministic alternatives do not provide. The main tradeoff is computational cost and lower interpretability compared with linear or polynomial models, but for this dataset the improvement in predictive quality is strong enough to justify that complexity.
