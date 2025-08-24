# Feature Selection for High-Dimensional Data
Code repository for performing feature selection in machine learning.

## Table of Contents

### 1. Basic Selection Methods
<details>
<summary>1.1 Removing Constant Features</summary>
Remove features that have the same value across all samples, as they carry no predictive information.
</details>

<details>
<summary>1.2 Removing Quasi-Constant Features</summary>
Remove features where a single value dominates (e.g., >99% same value), reducing redundancy.
</details>

<details>
<summary>1.3 Removing Duplicated Features</summary>
Remove features that are exact duplicates of other features to avoid multicollinearity.
</details>

### 2. Correlation Feature Selection
<details>
<summary>2.1 Removing Correlated Features</summary>
Remove one of a pair of highly correlated features to reduce redundancy and multicollinearity.
</details>

<details>
<summary>2.2 Smart Correlation</summary>
Select features based on correlation thresholds intelligently, e.g., prioritize features with higher predictive power.
</details>

### 3. Statistical Methods
<details>
<summary>3.1 Chi-square Distribution</summary>
Measure the dependence between categorical features and target variable for classification tasks.
</details>

<details>
<summary>3.2 ANOVA (Analysis of Variance)</summary>
Assess whether continuous features differ significantly across target classes.
</details>

<details>
<summary>3.3 Correlation</summary>
Use Pearson or Spearman correlation to quantify linear or monotonic relationships between features and target.
</details>

<details>
<summary>3.4 Mutual Information</summary>
Measures nonlinear dependency between feature and target variable, useful for both classification and regression.
</details>

### 4. Univariate Methods
<details>
<summary>4.1 Single Feature Classifiers / Regressors</summary>
Evaluate each feature individually using a simple model to estimate its predictive power.
</details>

<details>
<summary>4.2 Target Mean Encoding</summary>
Encode categorical features by replacing each category with the mean of the target variable for that category.
</details>

### 5. Wrapper Methods
<details>
<summary>5.1 Exhaustive Feature Selection</summary>
Try all possible combinations of features to find the best performing subset (computationally expensive).
</details>

<details>
<summary>5.2 Step Forward Feature Selection</summary>
Iteratively add features that improve model performance until no significant improvement occurs.
</details>

<details>
<summary>5.3 Step Backward Feature Selection</summary>
Start with all features and iteratively remove the least significant features until performance decreases.
</details>

### 6. Embedded Methods: Linear Model Coefficients
<details>
<summary>6.1 Lasso</summary>
L1-regularized linear regression that shrinks less important feature coefficients to zero.
</details>

<details>
<summary>6.2 Decision Tree Feature Importance</summary>
Use tree-based models to measure the importance of each feature based on split gains.
</details>

<details>
<summary>6.3 Recursive Feature Elimination (RFE)</summary>
Iteratively remove the least important features based on model performance or embedded importance.

- **RFE - embedded importance**: Use model coefficients or feature importance for elimination.  
- **RFE - model performance**: Remove features and evaluate performance iteratively.
</details>

### 7. Alternative Feature Selection Methods
<details>
<summary>7.1 Feature Shuffling</summary>
Shuffle feature values and observe the impact on model performance to assess feature importance.
</details>

<details>
<summary>7.2 Recursive Feature Addition</summary>
Start with no features and iteratively add the most impactful features.
</details>

<details>
<summary>7.3 Probe Features</summary>
Add synthetic or random features to compare and identify meaningful features.
</details>

<details>
<summary>7.4 MRMR (Minimum Redundancy Maximum Relevance)</summary>
Select features that have high relevance with the target and minimal redundancy among themselves.
</details>
