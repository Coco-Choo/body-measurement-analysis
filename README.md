# 🏋️ Body Measurement Analysis for Health Research  
**Fall 2024 | Texas Tech University | ISQS-6350 (Multivariate Analysis)**  
**RAWLS College of Business - MS Data Science Program**

---

## 📄 Introduction
This case study explores a rich dataset of body measurements for 507 individuals, collected from Kaggle's [Body Measurements Dataset](https://www.kaggle.com/datasets/mexwell/body-measurements). The dataset includes anthropometric and demographic attributes such as diameters, girths, height, weight, sex, and age. This analysis is structured around multivariate statistical techniques to extract meaningful insights about body composition and its practical implications.

---

## 🚀 Motivation
Understanding how body measurements relate to each other can impact a variety of domains:
- **Health Profiling**: Inform BMI, fat distribution, and health risks.
- **Body Type Classification**: Cluster individuals into natural body-type groups.
- **Predictive Modeling**: Predict health metrics (e.g., weight or BMI) using other variables.
- **Gender-Based Analysis**: Identify anatomical distinctions across sexes.
- **Aging Trends**: Understand how body composition evolves with age.

---

## 💡 Data Preparation
- Renamed columns for clarity (e.g., `wri_d` to `wrist_d`).
- Outlier detection via Mahalanobis distance removed 7 extreme cases.
- Correlation matrices before and after outlier removal showed minimal difference due to large sample size.

---

## 🔎 Exploratory Analysis & Visualizations
- **Kernel Density Plots** showed multimodal distributions in height and weight, consistent with sex-based subgroups.
- **Bivariate Density Plots** further demonstrated sex differences in body shape (e.g., male vs female cluster zones).

---

## 🔄 Dimension Reduction (PCA)
- Performed Principal Component Analysis (PCA) to reduce 25 variables to 5 components explaining 85% of total variance.
- Each component captured distinct anatomical interpretations (e.g., overall size, leg girth, height vs girth proportions).

---

## 🤸 Cluster Analysis (K-Means)
- Optimal number of clusters: **3**, determined using a scree plot.
- **Cluster 1**: Large individuals  
  **Cluster 2**: Average-sized individuals  
  **Cluster 3**: Small individuals  
- Clusters validated using means of key body measurement variables.

---

## 🌐 Confirmatory Factor Analysis (CFA)
- Developed 2-factor model:
  - **Factor 1**: Upper-body metrics and general body size
  - **Factor 2**: Lower-body and girth measurements
- Initial model had poor fit (GFI = 0.48, AGFI = 0.38), prompting exclusion of general variables (age, sex, weight, height).
- Revised model showed marginal improvement, though still limited explanatory power.

---

## 📈 Findings
- Outlier removal had minimal statistical impact.
- PCA helped group highly correlated features into interpretable components.
- Clustering revealed meaningful body size groupings.
- CFA confirmed upper/lower body latent dimensions but needs model refinement.

---

## 🚀 Future Work
- **Machine Learning Models**: Predict BMI or body types using decision trees or neural nets.
- **Longitudinal Analysis**: Evaluate how body composition changes over time.
- **Gender-Specific Analytics**: Build sex-separated models for ergonomics or fitness.
- **Industry Applications**: Apply findings to apparel sizing, ergonomic product design, or health diagnostics.

---

## 📂 Dataset Source
- Kaggle: [Body Measurements Dataset](https://www.kaggle.com/datasets/mexwell/body-measurements)
- Observations: 507 (used 500 after outlier removal)
- Variables: 25 anthropometric and demographic features

---
