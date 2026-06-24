# 🏥 Patient Health Data Cleanser

## 📋 Overview

This project processes a **patient health dataset** containing demographic and clinical features to improve data quality before downstream analysis or machine learning tasks.

<details>
<summary>📂 <b>Dataset Features — Click to Expand</b></summary>

<br/>

|    🏷️ Feature    |     📌 Type     |            📖 Description            |
| :----------------: | :--------------: | :-----------------------------------: |
|   `patient_id`   |      🔑 ID      |       Unique patient identifier       |
|      `age`      |   🔢 Numerical   |              Patient age              |
|     `gender`     | 🏷️ Categorical |            Patient gender            |
|     `region`     |  🌍 Categorical  |           Geographic region           |
|      `bmi`      |  ⚖️ Numerical  |            Body Mass Index            |
| `blood_pressure` |   💉 Numerical   |        Blood pressure reading        |
|  `cholesterol`  |   🩸 Numerical   |           Cholesterol level           |
|    `glucose`    |   🍬 Numerical   |          Blood glucose level          |
|  `disease_risk`  |    🎯 Target    | `0` = Low Risk · `1` = High Risk |

</details>

---

## 🎯 Objectives

```
🔍  Identify and handle missing values using multiple imputation strategies
📉  Detect and treat outliers using robust statistical methods
⚖️  Compare different preprocessing approaches side-by-side
🤖  Prepare a clean dataset ready for machine learning
```

---

## 🗂️ Project Structure

```
🔍  Identify and handle missing values using multiple imputation strategies
📉  Detect and treat outliers using robust statistical methods
⚖️  Compare different preprocessing approaches side-by-side
🤖  Prepare a clean dataset ready for machine learning
```

---

## 🔧 Preprocessing Techniques

### 💊 Missing Value Imputation

|                   🧪 Method                   | 📖 Description                                                                    |
| :-------------------------------------------: | :-------------------------------------------------------------------------------- |
|          🟦**Simple Imputer**          | Fills numerical NaNs with mean/median; categorical with mode                      |
|     🟩**Most Frequent Imputation**     | Replaces missing values with the most common value (mode)                         |
| 🟨**Missing Indicator + Random Sample** | Creates a missingness flag, then fills by randomly sampling existing values       |
|            🟧**KNN Imputer**            | Uses K-Nearest Neighbors similarity to estimate missing values                    |
|          🟥**MICE Algorithm**          | Multiple Imputation by Chained Equations — iterative regression-based imputation |

<br/>

### 🚨 Outlier Detection & Treatment

|           🔬 Method           | 📖 Description                                                                       |
| :---------------------------: | :----------------------------------------------------------------------------------- |
|      📐**Z-Score**      | Flags values beyond ±3 standard deviations; best for normal distributions           |
|    📦**IQR Method**    | Detects values outside`Q1 − 1.5×IQR` / `Q3 + 1.5×IQR`; robust for skewed data |
| 📏**Percentile Method** | Caps/removes values below 1st and above 99th percentile                              |
|   🪄**Winsorization**   | Replaces extremes with boundary thresholds — no data is lost                        |

---

## 📊 Key Visualizations

### 📈 1. BMI Distribution

> 💡 Right-skewed histogram with KDE overlay — most patients in the **20–35 BMI range** with extreme outliers reaching up to **~75**.

![BMI Distribution](./image/bmi.png)

---

### 📦 2. BMI Outliers — Boxplot

> 💡 Multiple outliers visible on both the **lower end (<10)** and **upper end (>50)** before any treatment.

![BMI Outliers Boxplot](./image/bmiOutlier.png)

---

### ❌ 3. Before Outlier Treatment

> 💡 Raw BMI data showing the **full spread** of values including extreme outliers on both sides of the distribution.

![Before Outlier Treatment](./image/beforeOutlier.png)

---

### ✅ 4. After Outlier Treatment (IQR Method)

> 💡 Outliers significantly reduced after IQR capping — distribution **tightened to 15–38**, a clinically meaningful range.

![After Outlier Treatment](./image/afterOutlier.png)

---

### 🔵 5. Cholesterol vs. Glucose Scatter Plot

> 💡 Reveals distinct anomalous clusters — **glucose 400–560** and **cholesterol >450** indicating data entry errors or clinical extremes.

![Cholesterol vs Glucose](./image/zscore.png)

---

## 🚀 Getting Started

### ⚙️ Prerequisites

```
🔍  Identify and handle missing values using multiple imputation strategies
📉  Detect and treat outliers using robust statistical methods
⚖️  Compare different preprocessing approaches side-by-side
🤖  Prepare a clean dataset ready for machine learning
```

### ▶️ Run the Notebook

```
🔍  Identify and handle missing values using multiple imputation strategies
📉  Detect and treat outliers using robust statistical methods
⚖️  Compare different preprocessing approaches side-by-side
🤖  Prepare a clean dataset ready for machine learning
```

---

## 🛠️ Tech Stack

<div align="center">

|         🔧 Tool         |                   💡 Purpose                   |
| :----------------------: | :---------------------------------------------: |
|  🐍**Python 3.x**  |            Core programming language            |
|    🐼**Pandas**    |          Data manipulation & cleaning          |
|    🔢**NumPy**    |              Numerical operations              |
| 🤖**Scikit-learn** | SimpleImputer · KNNImputer · IterativeImputer |
|  📊**Matplotlib**  |              Static visualizations              |
|   🎨**Seaborn**   |         Statistical data visualization         |

</div>

---

## 👩‍💻 Author

<div align="center">

### ✨ Aesha Makrubiya
