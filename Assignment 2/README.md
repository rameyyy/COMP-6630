# Assignment 2: Binary Logistic Regression with One-vs-Rest

**Course:** COMP 6630 - Machine Learning

## Overview

This assignment implements and evaluates binary logistic regression classifiers using the One-vs-Rest (OvR) approach on the Iris dataset. The assignment covers:

- Implementation of logistic regression from scratch using gradient descent
- Training three binary classifiers: Class 0 vs Rest, Class 1 vs Rest, and Class 2 vs Rest
- Feature importance extraction and comparison
- L1 regularization for model sparsity
- Analysis of interpretability, performance, and feature selection

## Assignment Structure

### Part 1: Dataset and Preprocessing (10 points)
- Load the Iris dataset from sklearn
- Split data into 80% training and 20% testing (stratified, random_state=15)
- Standardize features using StandardScaler
- Create binary classification problems for each class

**Deliverables:**
- Code for loading and preprocessing
- Shape of X and distribution of target classes

### Part 2: Logistic Regression with Gradient Descent (30 points)
Implement logistic regression from scratch (cannot use scikit-learn for this part):
- Implement sigmoid function: σ(z) = 1/(1+e^(-z))
- Implement log-likelihood loss and gradient
- Gradient ascent with learning rate η = 0.0001, 5000-10000 iterations
- Evaluate training loss and accuracy for each OvR model

**Deliverables:**
- Code for gradient descent implementation
- Training loss curves
- Accuracy for each OvR classifier

### Part 3: Logistic Regression with Scikit-learn - No Regularization (15 points)
Use `LogisticRegression(penalty=None)` to replicate manual implementation:
- Fit model for each class (yc = 1 vs rest)
- Extract and rank feature weights by absolute value
- Report top 3 features with highest influence

**Deliverables:**
- Table of weights and top 3 features for each class
- Training accuracy
- Confusion matrix on test set

### Part 4: Feature Importance with L1 Regularization (25 points)
Train logistic regression with L1 regularization:
- Use `LogisticRegression(penalty='l1', solver='liblinear', C=0.1)`
- Extract feature weights and identify which are zeroed out
- Compare top 3 features with and without L1 regularization
- Evaluate model performance

**Deliverables:**
- For each class, provide comparison table:
  - Feature name
  - Weight (No Reg)
  - |Weight|
  - Weight (L1)
  - Zeroed? (Yes/No)

### Part 5: Evaluation and Comparison (10 points)
Compare all models:
- Training and test accuracy (no regularization vs L1)
- Number of features eliminated by L1 for each class
- Impact of feature sparsity on performance

**Deliverables:**
- Table of performance metrics
- Number of features retained
- Summary of top features across all classes

### Part 6: Analysis and Reflection (10 points)
Answer these questions briefly:
1. Were the most important features consistent across all three class-vs-rest classifiers?
2. Did any features appear important for one class but not others?
3. How does L1 regularization affect interpretability?
4. If you had to select 5 total features for all classes, which would you pick and why?

## Submission Requirements

### What to Submit
- **Code:** `.ipynb` notebook file
- **Feature weight tables** for each class
- **Training and evaluation results**
- **Plots:** loss curves
- **Written reflection:** answers to Part 6 questions

All content can be included in a single comprehensive notebook.

### Important Notes
1. **Code must run on Google Colab** - if it doesn't run, no credit for that segment
2. **Python only** - IPython notebook format required
3. **GenAI Declaration Required** - declare any AI assistance used (no penalty for declaration)
4. No syntax errors, indentation issues, or unnamed/unknown libraries

## Grading Rubric (Total: 100 points)

| Section | Points |
|---------|--------|
| Data Preparation | 10 |
| Manual Logistic Regression | 30 |
| scikit-learn OvR Models | 15 |
| Feature Importance with L1 | 25 |
| Evaluation and Comparison | 10 |
| Reflection | 10 |
| **Total** | **100** |

## Bonus (Extra Credit)
Implement L1-regularized logistic regression from scratch:
- Add -λ∥w∥₁ to the loss function
- Use subgradient method for optimization
- Compare results with scikit-learn

**(Extra 5-10 points)**

## Technical Specifications

- **Dataset:** Iris (sklearn.datasets.load_iris)
- **Train/Test Split:** 80/20, stratify=y, random_state=15
- **Learning Rate:** η = 0.0001
- **Iterations:** 5000-10000
- **L1 Parameter:** C=0.1
- **Solver for L1:** liblinear

## Files in This Directory

- `assignment2.ipynb` - Main assignment notebook with all code and analysis
- `HW_ML_2.pdf` - Original assignment document
- `assignment.txt` - Text version of assignment
- `todo.txt` - Assignment requirements and style guidelines
- `README.md` - This file
