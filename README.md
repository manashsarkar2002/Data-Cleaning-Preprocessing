# Data Preprocessing on the Titanic Dataset

This repository demonstrates essential **data preprocessing** techniques on the famous [Titanic dataset](https://www.kaggle.com/c/titanic), preparing it for machine learning tasks such as classification.

---

## 📌 Project Objective

The goal of this project is to:
- Understand the structure of the Titanic dataset
- Handle missing values
- Treat outliers
- Encode categorical variables
- Prepare a clean dataset suitable for ML models

---

## 📁 Dataset

The dataset used is the classic Titanic dataset, containing information about passengers such as:
- Passenger Class (Pclass)
- Name, Age, Sex
- Number of siblings/spouses aboard (SibSp)
- Number of parents/children aboard (Parch)
- Fare paid
- Port of Embarkation (Embarked)
- Survival status

---

## ⚙️ Preprocessing Steps

### 1. **Data Cleaning**
- Removed irrelevant columns: `Name`, `Ticket`, and `Cabin` (high cardinality or sparse data).
- Handled missing values in:
  - `Age` (filled with median after outlier treatment)
  - `Embarked` (filled with placeholder before encoding)

### 2. **Outlier Treatment**
- Applied **IQR method** to cap outliers in numerical columns:
  - `Age`, `Fare`, `SibSp`, `Parch`

### 3. **Encoding Categorical Variables**
- Encoded:
  - `Sex` using Label Encoding (`male` → 1, `female` → 0)
  - `Embarked` using Label Encoding after filling missing with placeholder

### 4. **Final Cleaned Dataset**
- Resulting dataset contains only numeric features
- Ready for model training or further analysis

---

## 🧪 Tools & Libraries Used

- Python 3.13.3
- Pandas
- NumPy
- scikit-learn (for Label Encoding)

---

## 📂 Output Files

- `Titanic-Dataset.csv`: Original File
- `Titanic-Dataset-Encoded-Clean.csv`: Dataset after outlier handling

---
