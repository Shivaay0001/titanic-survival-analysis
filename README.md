# 🚢 Titanic Survival Analysis — EDA using Python

## 📌 Project Overview

Exploratory Data Analysis on the Titanic dataset to identify which factors most strongly influenced passenger survival. The dataset contains records of **891 passengers** with demographic, socioeconomic, and travel information.

---

## 🎯 Objective

To analyze passenger data and determine how gender, passenger class, age, fare, and family size affected survival probability — and to extract quantified, actionable insights from raw data.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical operations |
| Matplotlib | Static visualizations |
| Seaborn | Statistical plots and heatmaps |

---

## 📊 Dataset

The dataset contains information about 891 passengers including:

| Column | Description |
|--------|-------------|
| Survived | Target variable (0 = No, 1 = Yes) |
| Pclass | Passenger class (1st, 2nd, 3rd) |
| Sex | Gender |
| Age | Age in years (177 missing values handled) |
| Fare | Ticket price |
| SibSp / Parch | Family members aboard |
| Embarked | Port of embarkation |

---

## 🔍 Steps Performed

### 1. Data Cleaning
- Dropped `Cabin` column — over 77% missing values
- Filled missing `Age` values using median (28.0)
- Filled 2 missing `Embarked` values using mode (Southampton)

### 2. Feature Engineering
- Created `FamilySize` = SibSp + Parch + 1
- Created `IsAlone` flag for solo travelers
- Grouped `Age` into bins: Child (0–12), Teen (13–17), Adult (18–60), Senior (60+)
- Grouped `Fare` into quartile-based ranges (Low / Mid / High / Very High)

### 3. Exploratory Data Analysis
- Survival rate breakdown by gender, class, age group, fare range
- Family size vs survival analysis
- Correlation heatmap across all numeric features
- Distribution plots for age and fare

---

## 📈 Key Insights

- **Gender:** Female survival rate was **~74%** vs only **~19%** for males — the strongest single predictor
- **Class:** 1st class passengers survived at **63%**, compared to **47%** in 2nd class and **24%** in 3rd class
- **Fare:** Higher fare passengers (top quartile) had significantly better survival — likely correlated with class and deck location
- **Family Size:** Passengers traveling alone or with 1–2 family members survived better than large groups (5+)
- **Age:** Children (under 12) had a relatively higher survival rate, consistent with "women and children first" evacuation policy

---

## 📷 Visualizations

![Gender Survival](gender_survival.png)
*Survival rate by gender — females survived at nearly 4× the rate of males*

![Class Survival](class_survival.png)
*1st class passengers had 2.6× higher survival than 3rd class*

![Age Group Survival](Age_group_survival.png)
*Children had a notably higher survival rate compared to adults*

![Correlation Heatmap](heatmap.png)
*Heatmap showing feature correlations — Pclass and Fare show strongest correlation with survival*

---

## ✅ Conclusion

Gender, passenger class, and fare were the three most significant factors influencing survival on the Titanic. Female passengers in 1st class had survival rates exceeding 95%, while male passengers in 3rd class survived at under 15%. These findings reflect both the "women and children first" evacuation policy and the structural advantage of higher-deck cabin placement for 1st class passengers.

This project demonstrates proficiency in data cleaning, feature engineering, and extracting quantified business insights from raw data using Python.

---

## 📁 Files in This Repository

| File | Description |
|------|-------------|
| `Titanic_EDA_Project.ipynb` | Main analysis notebook |
| `*.png` | Visualization outputs |
