# 📘 Feature Engineering Notes

## 🧠 What is Feature Engineering?
Feature engineering is the process of converting **raw data into meaningful features** that machine learning models can understand and learn from.

👉 Better features = better models
👉 Poor features = poor predictions 🗑️


![alt text](image-1.png) ![alt text](image-2.png)

---

## 1️⃣ Feature Transformation
Transform existing features to improve model performance.

---

### a️⃣ Missing Value Transformation 🕳️
Missing values are very common in real-world datasets.

#### Common techniques:
- **Mean / Median Imputation** ➗
  Suitable for numerical data
- **Mode Imputation** 📊
  Best for categorical data
- **Constant Value** (`0`, `"Unknown"`) 🏷️
- **Drop rows or columns** ❌
  Use only if missing values are very few
- **Advanced methods**: KNN, regression imputation 🤓

💡 **Tip**
Use **median** instead of mean when outliers exist.

---

### b️⃣ Handling Categorical Features 🏷️
Machine learning models do not understand text data.

#### Encoding techniques:
- **Label Encoding** 🔢
  Example: `Low → 0, Medium → 1, High → 2`
  ⚠️ Use only when order matters
- **One-Hot Encoding** 🎯
  Example: `Color_Red, Color_Blue, Color_Green`
- **Target Encoding** 📈
  Category replaced by mean target value
- **Frequency Encoding** 📊
  Category replaced by its frequency

💡 **Tip**
Tree-based models handle encodings better than linear models 🌳

---

### c️⃣ Outlier Detection 🚨
Outliers are extreme values that can negatively affect models.

#### Detection methods:
- **IQR (Interquartile Range)** 📦
- **Z-score method** 📏
- **Box plots** 📊
- **Data visualization** 👀

#### Handling techniques:
- Remove ❌
- Cap values (Winsorization) 🎩
- Log transformation 📉

⚠️ Not all outliers are bad. Some contain valuable information.

---

### d️⃣ Feature Scaling 📏
Scaling ensures features are on similar ranges.


![alt text](image-3.png) ![alt text](image-4.png)


#### Scaling methods:
- **Min-Max Scaling** 📐
  Scales data between `0 and 1`
- **Standardization (Z-score)** 📊
  Mean = 0, Standard Deviation = 1
- **Robust Scaling** 🛡️
  Uses median and IQR (outlier-resistant)

#### Required for:
- Linear Regression
- Logistic Regression
- KNN
- SVM

#### Not required for:
- Decision Trees
- Random Forest
- XGBoost

---

## 2️⃣ Feature Construction 🧩
Creating **new features** from existing ones.

#### Examples:
- `Total_Price = Price × Quantity` 💰
- `Age = Current_Year - Birth_Year` 🎂
- `BMI = Weight / Height²` 🧍

🎯 Benefits:
- Captures hidden patterns
- Injects domain knowledge
- Often improves accuracy more than model tuning

💡 **Rule of thumb**
Strong features can outperform complex models 😉

---

## 3️⃣ Feature Selection 🎯
Select only the most important features.

#### Why?
- Faster training ⚡
- Reduced overfitting 🧠
- Better interpretability 👓

#### Selection methods:
- **Filter methods** 🧹
  Correlation, Chi-square
- **Wrapper methods** 🎁
  Recursive Feature Elimination (RFE)
- **Embedded methods** 🌱
  Lasso, Ridge, Tree-based feature importance

💡 **Tip**
Fewer meaningful features > many noisy features 🏆

---

## 4️⃣ Feature Extraction 🧠✨
Reduce dimensionality by transforming data into a new feature space.

#### Common techniques:
- **PCA (Principal Component Analysis)** 🔄
- **LDA (Linear Discriminant Analysis)** 📊
- **Autoencoders** 🤖
- **Text features**: TF-IDF, Word Embeddings 📝

🎯 Use when:
- Dataset has too many features
- Features are highly correlated
- Visualization is needed

⚠️ Drawback
Reduced interpretability compared to original features.

---

## 🧠 Final Advice from Experience 🧓
- Spend **more time on features than models**
- Simple models with great features beat complex models
- Always visualize your data 👀
- Understand the business problem 🗣️

---

## 📌 TL;DR Stickers 😄
🧹 Clean your data
🧩 Build smart features
🎯 Select important ones
🧠 Extract when necessary
🚀 Then train models

---

