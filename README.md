
#  Comprehensive Morphological Analysis for Breast Cancer Diagnosis

## Overview

This project focuses on developing a predictive model to classify breast tumors as **malignant or benign** using morphological features derived from fine needle aspiration biopsy data. Utilizing machine learning and statistical tools (Logistic Regression, SVM, Random Forest), the project aims to enhance early detection and diagnostic precision of breast cancer.

* **Institution**: University of Pittsburgh, School of Health and Rehabilitation Sciences
* **Course**: Statistical Analysis in Health Informatics
* **Author**: Sree Gayatri Anusha Mylavarapu
* **Supervisor**: Dr. Leming Zhou, PhD, DSc

---

##  Objectives

* Develop a machine learning model to predict breast cancer malignancy.
* Explore morphological and clinical features to identify tumor characteristics.
* Improve diagnostic accuracy over traditional methods.
* Use both statistical tools (Stata) and visual machine learning environments (Orange).

---

##  Motivation

Current diagnostic tools like mammography and physical examination can lead to **false positives and false negatives**, affecting timely treatment. This study addresses:

* The need for **high sensitivity and specificity** in diagnosis.
* Integration of **machine learning** to enhance predictive capabilities.
* Use of **morphological data** to better detect malignancy patterns in tumors.

---

##  Dataset

* **Source**: UCI Breast Cancer Wisconsin Diagnostic Dataset
* **Samples**: 569
* **Features**: 30 (including radius, texture, smoothness, compactness, area, perimeter, etc.)
* **Target**: Diagnosis

  * `0 = malignant`
  * `1 = benign`

---

## Tools & Techniques

###  Statistical Tool: **Stata**

* Logistic regression performed for binary classification.
* Output:

  * **LR chi2** = 655.74
  * **Pseudo R²** = 0.8727
  * Highly statistically significant (p < 0.0001)
  * Indicates strong model fit and predictive power

### ML Platform: **Orange Workflow**

* Models used: Logistic Regression, Support Vector Machine (SVM), Random Forest
* Evaluation Metrics:

  * High **precision** (minimized false positives)
  * High **recall** (sensitive to true malignant cases)
  * Strong **F1 score** (balance of precision and recall)

###  Model Validation

* **K-Fold Cross-Validation** used to evaluate model stability.
* Future validation suggested using independent datasets.

---

## Results Summary

| Feature     | Mean (Malignant) | Std. Error (Malignant) |
| ----------- | ---------------- | ---------------------- |
| Radius      | 12–23            | 0.2–1                  |
| Texture     | 16–28            | 0.4–1.9                |
| Perimeter   | 77–144           | 1.4–8                  |
| Area        | 430–1400         | 13–150                 |
| Concavity   | 0.02–0.25        | 0.012–0.1              |
| Smoothness  | 0.08–0.1         | 0.002–0.01             |
| Compactness | 0.05–0.2         | 0.008–0.061            |

>  Notable Finding: Tumors with larger areas tend to exhibit **lower smoothness**, suggesting potential biological implications.

---

##  Key Insights

* **High Accuracy**: Models performed excellently in distinguishing malignant from benign tumors.
* **Most influential features**: Radius, Area, Concavity, and Texture.
* **Inverse relationships** (e.g., smoothness vs. area) open avenues for further biological exploration.

---

## Limitations

* Dataset size (n=569) may limit generalizability.
* Lacks **genetic or molecular** markers for deeper insights.
* No **temporal data**—static snapshot limits understanding of progression.
* Feature interaction analysis is pending and can uncover complex dependencies.

---

##  References

* [UCI Machine Learning Repository – Breast Cancer Dataset](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)
* Aleskandarany et al. (2018). Tumor heterogeneity and personalized medicine. Pathobiology.
* Bychkov et al. (2021). Deep learning and HER2 status prediction. Scientific Reports.

---

##  Conclusion

This study successfully implemented predictive models using machine learning and statistical tools to classify breast cancer cases. The models, especially those built with **logistic regression and SVM**, demonstrated high accuracy and precision. While findings are promising, **further research** involving larger datasets, genetic features, and longitudinal data is recommended to refine diagnostic performance and support **personalized treatment** strategies.
