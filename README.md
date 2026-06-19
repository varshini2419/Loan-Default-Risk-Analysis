# 🎯 Credit Default Risk Analysis Suite

A comprehensive, Python-based Exploratory Data Analysis (EDA) project designed to systematically investigate customer financial profiles and identify the critical risk factors influencing loan defaults. 

This repository showcases an analytical workflow that handles data preprocessing, isolates behavioral quirks across multiple financial features, and translates technical visualizations into strategic business insights.

---

## 📊 Project Overview & Problem Statement
The primary objective of this analysis is to interrogate customer financial and personal information (such as income, credit scores, and loan amounts) to determine how they correlate with loan defaults (`Default: 0 = No default, 1 = Default`). By understanding these joint-variable interactions, the project establishes a solid analytical foundation required for building an eventual risk-scoring and classification framework.

---

## 💡 Key Data Insights

### 1. Perfectly Uniform Feature Distributions
Initial univariate exploration reveals that the core financial metrics—**Income**, **Credit Score**, and **Loan Amount**—exhibit entirely flat, uniform distributions. Every value range holds a highly identical frequency count (~4,000 observations per bin). Real-world banking data naturally clusters or skews (e.g., credit scores typically form a bell curve), which strongly indicates that this dataset is synthetically generated or simulated for testing purposes.

### 2. Income Divergence
Successful loan repayment strongly correlates with higher earnings. The average income of the "Safe" group sits at roughly **$83,899**, which is **$12,055 higher** than the "Risky" defaulting group's average of **$71,844**. However, a detailed look at the distribution shows that this risk-differentiation power flattens out entirely once an applicant clears a middle-class threshold of **$60,000**.

### 3. Loan Amount Scaling Risk
While "Safe" borrowers request small, medium, and large loans in relatively equal proportions, "Risky" borrowers scale upward smoothly alongside loan sizes. The probability of an applicant defaulting increases steadily as the requested capital rises, showing that larger loans carry a disproportionately higher default risk in this environment.

### 4. Credit Score Stability
Surprisingly, the absolute distribution of safe versus risky customers remains almost completely identical across the entire **300 to 850** spectrum. An applicant with a perfect credit score of 800 is statistically almost as likely to default as someone with a poor score of 400, indicating that credit score alone is an ineffective standalone predictor for this specific dataset.

### 5. The "Confetti" Interaction
Bivariate scatter plots mapping Income against Loan Amount reveal a perfectly uniform, rectangular distribution block. The groups cannot be cleanly split using simple linear rules or single-threshold filters (e.g., blocking loans based purely on standard credit caps), as the overlapping patterns heavily mix safe and risky borrowers together across all axes.

---

## 🛠️ Technical Stack & Libraries Used
* **Language:** Python
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`

---

## 📋 Core Analytical Workflow

1. **Data Preprocessing:** Cleaned column formatting by stripping whitespaces, handled missing values, explicitly coerced the target variable to numeric types, and ensured defensive, reproducible programming practices.
2. **Univariate Analysis:** Evaluated isolated feature distributions using individual histograms combined with Kernel Density Estimate (KDE) lines to detect initial dataset traits.
3. **Bivariate Analysis:** Deployed overlapping, color-coded frequency distributions to visually separate and compare the behavior of "Safe" vs. "Risky" consumer segments.
4. **Multivariate Exploration:** Interrogated the joint relationship between income levels and total funding requests to evaluate visual separability and look for joint-variable risk clusters.

---
