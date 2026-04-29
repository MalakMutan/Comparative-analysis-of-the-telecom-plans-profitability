# 🧠 Breast Cancer Data Analysis & Tumor Classification Study

## 📌 Project Overview

This project focuses on analyzing a breast cancer dataset to identify key features that distinguish between **benign (B)** and **malignant (M)** tumors. The analysis combines statistical methods and data visualization to uncover patterns that can support medical diagnosis and serve as a foundation for machine learning models.

---

## 🎯 Objectives

* Explore the distribution of tumor diagnoses (Benign vs Malignant)
* Identify the most important features influencing diagnosis
* Analyze relationships between tumor characteristics
* Perform statistical hypothesis testing to validate differences
* Provide insights for potential classification models

---

## 📊 Dataset Description

The dataset contains detailed measurements of tumor characteristics, including:

* Radius, texture, perimeter, and area
* Smoothness, compactness, concavity
* Symmetry and fractal dimension

Each observation is labeled as:

* **B (Benign)** → Non-cancerous
* **M (Malignant)** → Cancerous

Additionally, a binary variable was created:

* `0` → Benign
* `1` → Malignant

---

## 🧹 Data Preprocessing

* Converted categorical diagnosis into binary format
* Selected numerical features for analysis
* Checked for missing values and inconsistencies
* Ensured proper data types for computation

---

## 📈 Exploratory Data Analysis (EDA)

### 🔹 Diagnosis Distribution

* Benign cases: 357
* Malignant cases: 212
* The dataset is slightly imbalanced but still usable

---

### 🔹 Correlation Analysis

* Strong correlations observed between:

  * `radius_mean` and `perimeter_mean`
  * `area_mean` and `radius_mean`
* High correlation indicates redundancy among some features

---

### 🔹 Feature Distributions

* Malignant tumors tend to have:

  * Larger radius and area
  * Higher concavity and irregularity
* Visualizations (histograms & boxplots) show clear separation trends

---

### 🔹 Outlier Detection

* Boxplots reveal the presence of outliers in several features
* Outliers are more prominent in malignant tumor measurements

---

## 🔬 Statistical Analysis

### Hypothesis Testing

We tested whether there is a significant difference in tumor characteristics between malignant and benign cases.

#### Example Hypothesis:

* **H₀:** μₘ = μᵦ (no difference in mean radius)
* **H₁:** μₘ ≠ μᵦ (significant difference exists)

A two-sample t-test was applied to compare feature means.

### 📌 Result:

* The p-value was found to be **less than 0.05**
* Therefore, we **reject the null hypothesis**

👉 This confirms that key features (e.g., `radius_mean`) differ significantly between tumor types.

---

## 🔍 Key Insights

* Features such as:

  * `concave points_worst`
  * `perimeter_worst`
  * `radius_mean`
    are highly correlated with tumor diagnosis

* Tumors with **large area_mean values** are overwhelmingly malignant (~96%)

* Malignant tumors generally exhibit:

  * Larger size
  * Higher irregularity
  * More complex structure

---

## 🤖 Future Work

* Build classification models (e.g., Logistic Regression, Random Forest)
* Apply feature selection techniques
* Evaluate model performance using accuracy, precision, recall

---

## 🛠️ Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* SciPy

---

## 📁 Project Structure

```
├── data/
│   └── breast-cancer.csv
├── notebook/
│   └── analysis.ipynb
├── README.md
```

---

## 📌 Conclusion

This analysis demonstrates that tumor characteristics differ significantly between benign and malignant cases. Statistical testing confirmed these differences, and exploratory analysis highlighted the most influential features. These findings provide a strong basis for developing accurate predictive models for early breast cancer detection.

---

## ✨ Author

**Malak Mu'tan**
Mathematics Major | Data Science Enthusiast
