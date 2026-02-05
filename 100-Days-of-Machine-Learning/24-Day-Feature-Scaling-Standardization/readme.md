What is feature scaling

What we do in feature scaling

Type of feature scaling
a. Standarization
b. Normilaization

Standarization also z-scroe normilization

x  y
1  24
2  25
3  1

xi' = (xi - mean)/ std

when to apply

algo reasion for apply eature scaling

1. k-means
2. knn
3. principle component analysis(pca)
4. ann
5. Gradent decendant


# 📘 Feature Scaling – Machine Learning Notes

## 🌟 What is Feature Scaling?

Feature scaling is a **data preprocessing technique** used to bring all numerical features to a **similar scale** so that machine learning algorithms work correctly and efficiently.

👉 Simple idea:
If one feature has small values and another has very large values, the model may give **unfair importance** to the larger one.

---

## 🛠️ What We Do in Feature Scaling

- Rescale numeric features ⚖️
- Prevent dominance of large-scale features
- Improve model performance 🚀
- Speed up training and convergence 📉

---

## ❌ Why Feature Scaling is Needed

Example:

| Feature | Range |
|-------|-------|
| Age | 18 – 60 |
| Income | 20,000 – 1,000,000 |

Without scaling ❌
➡️ Income dominates the model

With scaling ✅
➡️ Both features contribute fairly

---

## 🧠 Types of Feature Scaling

---

## 1️⃣ Standardization (Z-Score Normalization)

**Formula:**


**Properties:**
- Mean = 0
- Standard deviation = 1
- Values range from -∞ to +∞
- Works best when data is normally distributed

---

### 🔢 Example

Given data:

| x | y |
|---|---|
| 1 | 24 |
| 2 | 25 |
| 3 | 1 |

For `x`:
- Mean = 2
- Standard Deviation ≈ 0.82


Now values are centered and comparable 🧠

---

## 2️⃣ Normalization (Min-Max Scaling)

**Formula:**

