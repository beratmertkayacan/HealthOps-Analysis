# 🏥 HealthOps: AI-Driven Patient Segmentation & Efficiency Analyzer
**An end-to-end data intelligence engine designed to transform raw hospital operational data into strategic clinical insights.**

---

## 📂 Data Acquisition & Ingestion
The primary dataset was sourced from **Kaggle** as a raw CSV file. To simulate real-world healthcare data management and ensure cross-platform compatibility, the ingestion pipeline follows an **Excel-based workflow**:

* **Source:** Kaggle Open Healthcare Datasets.
* **Processing:** Raw data is transitioned from CSV to **XLSX format** to leverage structured data validation.
* **Ingestion:** The pipeline utilizes `pd.read_excel()` for robust data loading, followed by immediate integrity checks.

---
## 🔍 Exploratory Data Analysis (EDA)
*Uncovering hidden patterns and correlations within the healthcare environment through rigorous statistical mapping:*

### 📈 1. Correlation & Distribution Analysis
* **Pearson Correlation:** Calculated coefficients to quantify the strength of the relationship between **Length of Stay (LOS)** and **Total Revenue**. 
* **Key Finding:** Identified how patient discharge patterns directly influence the hospital's cash flow consistency.

### 💳 2. Segmented Payer Performance
* **Multi-variate Mapping:** Analyzed the impact of the **Payer Mix** (Insurance types) on revenue flows.
* **Visualization:** Used hue-encoded scatter plots to distinguish between high-margin and low-margin insurance providers.

### ⚡ 3. Efficiency Mapping (The "Value" Metric)
* **Custom Metric Development:** Engineered the **Daily Revenue (Revenue / LOS)** ratio.
* **Strategic Comparison:** Benchmarked different medical **Specialties** to identify which departments utilize hospital beds most profitably.

### 🚨 4. Residual-Based Anomaly Detection
* **Baseline Modeling:** Utilized a **Linear Regression** model to define "Expected Revenue" per case based on stay duration.
* **Outlier Discovery:** Calculated the **Residuals** (Actual - Expected) to flag the **Top 10 Critical Anomalies**.
* **Operational Impact:** These cases were prioritized for administrative audit to detect potential billing errors or clinical inefficiencies.

---

## 🚀 Technical Excellence & AI Optimizations
This project focuses on bridging the gap between clinical complexity and financial sustainability through several key AI implementations:

### 1. Advanced Unsupervised Learning
Implemented **K-Means Clustering** with optimized centroid initialization (`k-means++`) to categorize multidimensional patient data (Revenue, LOS, CMI).

### 2. Hyperparameter Optimization
Utilized the **Elbow Method (WCSS)** to mathematically determine the optimal number of clusters, ensuring statistical significance in patient segmentation.

### 3. Predictive Anomaly Detection
Developed a **Residual Analysis** framework using **Linear Regression** to detect "Outlier Cases"—identifying high-deviation billing or operational inconsistencies.

### 4. Robust Feature Engineering
Integrated a specialized preprocessing pipeline featuring:
* **StandardScaler:** For high-performance feature normalization.
* **One-Hot Encoding:** For handling categorical variables like *Specialty* and *Payer Mix*.

---

## 🛠️ Tech Stack

| Category | Tools & Libraries |
| :--- | :--- |
| **Language** | Python |
| **Machine Learning** | Scikit-Learn (Clustering, Preprocessing, Linear Models) |
| **Data Science** | Pandas, NumPy |
| **Visualization** | Matplotlib (3D Engine), Seaborn |

---

## 📊 Strategic Value & Business Insights
The system categorizes the hospital portfolio into three actionable segments, providing a roadmap for hospital management:

* 🚀 **Operational Champions:** High-efficiency cases with optimal difficulty-to-revenue ratios.
* ⚠️ **Resource Intensive (At-Risk):** High-revenue cases with disproportionately long stay durations.
* 🔄 **Standard Flow:** Routine high-turnover cases ensuring consistent operational cash flow.

---

