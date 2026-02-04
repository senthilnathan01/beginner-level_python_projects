# HW1: Statistical Learning Perspective & Exploratory Data Analysis

## Overview

This assignment performs a comprehensive exploratory data analysis (EDA) on the Iris dataset using Python. The analysis covers statistical inspection, univariate and bivariate visualizations to understand data distributions and relationships.

## Tasks Completed

1. **Data Loading and Inspection**: Loaded the Iris dataset from sklearn and converted it to a pandas DataFrame. The dataset contains 150 samples with 4 features (sepal length/width, petal length/width) and 3 species classes.

2. **Summary Statistics**: Computed descriptive statistics (mean, median, std dev) to identify feature variability. Found that petal length exhibits the largest variability, and the feature scales are not directly comparable, suggesting normalization may be beneficial for ML models.

3. **Univariate Visualization**: Created histograms and box plots for each feature to analyze distributions. Key findings: petal length and petal width show strong bimodal distributions, while sepal features are approximately symmetric with signs of multiple underlying groups.

4. **Bivariate Analysis**: Generated scatter plots for multiple feature pairs to investigate clustering and separation patterns between variables, revealing relationships useful for species classification.

5. **Labeled Visualization**: Colored scatter plots with species labels to confirm that Setosa is easily separable from other species, while Versicolor and Virginica show significant overlap.

6. **Reflection**: Discussed the importance of EDA before modeling, consequences of skipping visualization, and identified petal features as the most useful for classification.

## Results

All figures have been saved to the `figs_results/` folder:
- `a1_task3_fig1_senthilnathan_t.png` - Histograms of all features
- `a1_task3_fig2_senthilnathan_t.png` - Box plots for outlier detection
- `a1_task4_fig1_senthilnathan_t.png` - Bivariate scatter plots (sepal and petal pairs)
- `a1_task4_fig2_senthilnathan_t.png` - Additional bivariate analysis

## Files

- `Assignment_1_EDA.ipynb` - Main notebook with code and analysis
- `Answers_Senthilnathan_T.pdf` - Solution PDF with visualizations and inferences (graded submission)
- `README.md` - This file
- `figs_results/` - Output figures and visualizations
