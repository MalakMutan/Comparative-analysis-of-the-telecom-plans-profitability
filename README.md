# 📊 Telecom Plan Profit Analysis

## 📌 Project Overview

This project analyzes customer behavior for the **Megaline telecom company** to determine which prepaid plan—**Surf** or **Ultimate**—is more profitable. The analysis combines data preprocessing, feature engineering, and statistical testing to evaluate revenue patterns and user activity.

---

## 🎯 Objectives

* Compare the profitability of Surf and Ultimate plans
* Analyze customer usage behavior (calls, messages, internet)
* Build a monthly profit calculation model
* Perform statistical hypothesis testing to validate differences

---

## 📊 Dataset Description

The dataset includes the following components:

* **Users:** demographic and subscription information
* **Calls:** call durations (rounded according to company policy)
* **Messages:** number of SMS sent
* **Internet:** data usage (aggregated monthly and rounded to GB)
* **Plans:** pricing structure, limits, and overage costs

---

## 🧹 Data Preprocessing

* Converted date columns to proper datetime format
* Handled missing values (e.g., inactive users labeled as *in use*)
* Applied company billing rules:

  * Calls rounded up to the nearest minute
  * Monthly internet usage rounded up to GB
* Aggregated user activity on a monthly basis

---

## 🧠 Methodology

### 🔹 Feature Engineering

* Calculated:

  * Monthly call minutes
  * Number of messages per user
  * Monthly internet usage (GB)

### 🔹 Profit Model

Monthly profit per user is computed as:

> Monthly Fee + Extra Charges (calls + messages + data)

Where extra charges are applied only when users exceed plan limits.

### 🔹 Statistical Analysis

* Conducted **two-sample t-tests** to compare:

  * Profit between Surf and Ultimate plans
  * Profit between NY-NJ region and other regions

---

## 📈 Key Findings

* The **Surf plan** is significantly more profitable
* Users on Surf frequently exceed plan limits, generating additional revenue
* The **Ultimate plan** includes excessive allowances, resulting in lower profitability
* Profitability increases over time for Surf but declines for Ultimate

---

## 🔬 Hypothesis Testing

### 1. Plan Comparison

* **H₀:** No difference in average profit between Surf and Ultimate
* **H₁:** A significant difference exists

✔ Result: The null hypothesis was rejected → **plans differ significantly in profitability**

---

### 2. Regional Comparison

* **H₀:** No difference in average profit between NY-NJ and other regions
* **H₁:** A significant difference exists

✔ Result: Statistical testing was used to evaluate regional differences

---

## 📊 Tools & Technologies

* Python
* Pandas
* NumPy
* SciPy
* Matplotlib

---

## 📁 Project Structure

```text
├── data/
│   └── telecom_data.csv
├── notebook/
│   └── analysis.ipynb
├── README.md
```

---

## 📌 Conclusion

The analysis demonstrates that the Surf plan generates higher revenue due to frequent overuse by customers. In contrast, the Ultimate plan offers overly generous limits, reducing additional charges. These insights suggest that optimizing plan structures could significantly improve company profitability.

---

## ✨ Author

**Malak Mu'tan**
Mathematics Major | Data Science Enthusiast
