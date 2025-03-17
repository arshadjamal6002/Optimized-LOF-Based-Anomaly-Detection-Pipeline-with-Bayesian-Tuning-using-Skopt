# **Anomaly Detection in Time-Series Data**

## **📌 Project Overview**
This project focuses on detecting anomalies in a time-series dataset with **350K rows and 6 features** using **unsupervised machine learning techniques**. The goal is to identify unusual patterns that may indicate system failures, fraud, or rare events.

---

## **🔍 Workflow Summary**
1. **Preprocessing & Scaling**  
   - Loaded dataset (`data.xlsx`).
   - Converted `time` column to datetime format.
   - Selected 6 numerical features.
   - Standardized the dataset using `StandardScaler`.

2. **Anomaly Detection Approaches**  
   - **Isolation Forest** (for efficient anomaly detection in large datasets).
   - **Local Outlier Factor (LOF)** (for density-based anomaly detection).
   - **HDBSCAN** (hierarchical clustering-based outlier detection).

3. **Dimensionality Reduction for Visualization**  
   - **UMAP** (used for 2D anomaly visualization instead of t-SNE for better scalability).

4. **Hyperparameter Optimization**  
   - Used **Bayesian Optimization** (`skopt.gp_minimize`) to fine-tune Isolation Forest parameters.
   - Optimized using **Silhouette Score** (since no labeled anomalies were available).

5. **Final Model Training & Anomaly Labeling**  
   - Trained Isolation Forest with optimal parameters.
   - Predicted anomaly scores & assigned anomaly labels (1=Anomaly, 0=Normal).

6. **Visualization & Insights**  
   - Plotted **anomaly scores over time**.
   - Used **UMAP scatter plots** to analyze normal vs. anomalous points.

---

## **🚀 Technologies Used**
- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, UMAP, HDBSCAN)
- **Machine Learning Models:**
  - **Isolation Forest**
  - **Local Outlier Factor (LOF)**
  - **HDBSCAN**
- **Dimensionality Reduction:**
  - **UMAP** (for anomaly visualization)
- **Hyperparameter Tuning:**
  - **Bayesian Optimization (`skopt.gp_minimize`)**

---

## **📊 Results & Observations**
✅ Optimized Isolation Forest detected **meaningful anomalies**.  
✅ **UMAP visualization** showed clear **separation between normal & anomalous data**.  
✅ **Bayesian Optimization** improved anomaly detection **without labeled data**.  
✅ Anomalies appear **at specific time intervals**, suggesting periodic system failures.  

---

## **💡 Next Steps**
🔹 Compare results with **LOF & HDBSCAN** for validation.  
🔹 Perform **Root Cause Analysis** on detected anomalies.  
🔹 Implement **real-time anomaly detection pipeline** using streaming data.  

---


