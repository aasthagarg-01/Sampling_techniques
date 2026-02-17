# Credit Card Fraud Detection — Sampling Techniques

## Overview

This project analyzes the impact of different sampling techniques on machine learning model performance when handling an imbalanced credit card fraud dataset.

Imbalanced datasets are common in real-world fraud detection problems, where fraudulent transactions are rare compared to legitimate ones. This assignment demonstrates how balancing techniques and sampling methods influence classification accuracy.

---

## Objective

The main objectives of this assignment are:

* Understand the importance of sampling techniques in imbalanced datasets
* Convert an imbalanced dataset into a balanced dataset
* Create five different samples using different sampling techniques
* Apply five machine learning models on each sampling technique
* Compare model performance using accuracy
* Identify the best sampling technique for each model and overall

---

## Dataset Information

Source: Credit Card Fraud Dataset

### Original Dataset Shape

| Rows | Columns |
| ---- | ------- |
| 772  | 31      |

---

### Balanced Dataset Shape

After applying oversampling to the minority class:

| Rows | Columns |
| ---- | ------- |
| 1526 | 31      |

---

### Class Distribution After Balancing

| Class         | Count |
| ------------- | ----- |
| 0 (Non-Fraud) | 763   |
| 1 (Fraud)     | 763   |

The dataset is now perfectly balanced.

---

## Sampling Techniques Used

Five sampling techniques were applied:

1. Sampling1 — Random Sampling
2. Sampling2 — Systematic Sampling
3. Sampling3 — Stratified Sampling
4. Sampling4 — Bootstrap Sampling
5. Sampling5 — Balanced Stratified Sampling

---

## Machine Learning Models Used

Five machine learning models were evaluated:

| Model ID | Model Name             |
| -------- | ---------------------- |
| M1       | Logistic Regression    |
| M2       | Decision Tree          |
| M3       | Random Forest          |
| M4       | K-Nearest Neighbors    |
| M5       | Support Vector Machine |

---

## Accuracy Results Table

| Model               | Sampling1 | Sampling2 | Sampling3 | Sampling4 | Sampling5 |
| ------------------- | --------- | --------- | --------- | --------- | --------- |
| Logistic Regression | 90.83%    | 90.83%    | 91.48%    | 93.01%    | 93.67%    |
| Decision Tree       | 100.00%   | 98.25%    | 98.91%    | 99.78%    | 99.13%    |
| Random Forest       | 100.00%   | 100.00%   | 100.00%   | 100.00%   | 100.00%   |
| KNN                 | 97.60%    | 93.45%    | 97.82%    | 97.38%    | 96.94%    |
| SVM                 | 97.60%    | 96.07%    | 97.82%    | 98.03%    | 98.25%    |

---

## Accuracy Comparison Graph (Conceptual Representation)

Higher bars indicate better performance.

```
Random Forest        █████████████████████████ 100%
Decision Tree        ████████████████████████  99–100%
SVM                  ██████████████████████    96–98%
KNN                  █████████████████████     93–97%
Logistic Regression  ███████████████████       90–93%
```

---

## Best Sampling Technique for Each Model

| Model               | Best Sampling Technique |
| ------------------- | ----------------------- |
| Logistic Regression | Sampling5               |
| Decision Tree       | Sampling1               |
| Random Forest       | Sampling1               |
| KNN                 | Sampling3               |
| SVM                 | Sampling5               |

---

## Average Accuracy of Each Sampling Technique

| Sampling Technique | Average Accuracy |
| ------------------ | ---------------- |
| Sampling1          | 97.206%          |
| Sampling2          | 95.720%          |
| Sampling3          | 97.206%          |
| Sampling4          | 97.640%          |
| Sampling5          | 97.598%          |

---

## Overall Best Sampling Technique

Sampling4 (Bootstrap Sampling) achieved the highest average accuracy.

Overall Best Sampling Technique: Sampling4

---

## Key Observations

1. Random Forest achieved 100% accuracy across all sampling techniques, showing excellent robustness.

2. Bootstrap Sampling provided the best overall performance across all models.

3. Logistic Regression showed the lowest accuracy, indicating it is less effective for this dataset compared to other models.

4. Systematic Sampling performed worst overall, indicating it may not preserve class characteristics effectively.

5. Stratified and Bootstrap sampling techniques provided consistently high accuracy.

---

## Why Balancing is Important

Before balancing:

* Majority class dominates
* Models become biased
* Fraud detection accuracy is poor

After balancing:

* Equal representation of both classes
* Improved model fairness
* Better fraud detection performance

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* Google Colab

---

## Conclusion

This project demonstrates that sampling techniques significantly affect machine learning model performance on imbalanced datasets.

Key conclusions:

* Bootstrap Sampling is the best overall sampling technique
* Random Forest is the best performing model
* Balanced datasets greatly improve classification performance
* Proper sampling improves model reliability

---
