# 🚀 Machine Learning Benchmark & Analytics Studio

An end-to-end Machine Learning evaluation suite and interactive frontend dashboard benchmarking **Clustering**, **Classification**, and **Boosting Regression** algorithms across three distinct datasets.

Designed with a sleek, responsive frontend ready for **1-click deployment on [Vercel](https://vercel.com/)**.

---

## 📊 Benchmark Summary Table

| Dataset | ML Problem Domain | Evaluated Algorithm | Primary Metric | Full Metrics Breakdown | Outcome |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Mall Customers** (`Mall_Customers.csv`) | **Clustering** (Unsupervised) | **K-Means Clustering** | **Silhouette: 0.5547** | Calinski-Harabasz: 248.65 \| Davies-Bouldin: 0.5722 \| Inertia: 65.57 | 🏆 **WINNER** |
| **Mall Customers** (`Mall_Customers.csv`) | **Clustering** (Unsupervised) | **Agglomerative Clustering** | Silhouette: 0.5538 | Calinski-Harabasz: 244.41 \| Davies-Bouldin: 0.5779 | Runner-up |
| **Social Network Ads** (`Social_Network_Ads.csv`) | **Classification** (Supervised) | **Support Vector Machine (SVC)** | **Accuracy: 91.25%** | F1: 0.8852 \| Precision: 0.8438 \| Recall: 0.9310 \| ROC-AUC: 0.9554 | 🏆 **WINNER** |
| **Social Network Ads** (`Social_Network_Ads.csv`) | **Classification** (Supervised) | **Random Forest Classifier** | Accuracy: 90.00% | F1: 0.8667 \| Precision: 0.8387 \| Recall: 0.8966 \| ROC-AUC: 0.9500 | Runner-up |
| **Insurance Premium** (`insurance_pre.csv`) | **Boosting (Regression)** | **XGBoost Regressor** | **R²: 0.8835** | RMSE: \$4,252.36 \| MAE: \$2,400.06 | 🏆 **WINNER** |
| **Insurance Premium** (`insurance_pre.csv`) | **Boosting (Regression)** | **Gradient Boosting Regressor** | R²: 0.8785 | RMSE: \$4,342.91 \| MAE: \$2,424.53 | Runner-up |

---

## 🧠 Dataset Details & Algorithms Evaluated

### 1. Mall Customers (`Mall_Customers.csv`) — Clustering
* **Goal**: Discover latent customer spending behavior patterns for targeted segmentation.
* **Features**: Annual Income (k$), Spending Score (1-100), Age.
* **Algorithms**:
  * **K-Means Clustering** (5 clusters, k-means++ initialization) — *Top Performer*
  * **Agglomerative Hierarchical Clustering** (5 clusters, Ward linkage)
* **Outcome**: K-Means achieved superior silhouette separation (0.5547) and lower Davies-Bouldin index (0.5722), identifying 5 distinct customer personas: Target VIPs, Careful Savers, Careless Spenders, Sensible Middle, and Frugal.

### 2. Social Network Ads (`Social_Network_Ads.csv`) — Classification
* **Goal**: Predict whether a user will purchase a product after viewing a social media ad.
* **Features**: Gender (encoded), Age, Estimated Salary.
* **Split**: Stratified 80/20 train/test split.
* **Algorithms**:
  * **Support Vector Machine (SVC - RBF Kernel)** — *Top Performer*
  * **Random Forest Classifier** (100 estimators, max depth 5)
* **Outcome**: SVC attained **91.25% test accuracy** and a **0.8852 F1-score**, excelling at classifying non-linear boundaries in age/salary purchasing thresholds.

### 3. Insurance Premium Prediction (`insurance_pre.csv`) — Boosting Regression
* **Goal**: Predict healthcare expenditure (`charges`) based on biometric and demographic variables.
* **Features**: Age, Sex, BMI, Children, Smoker status.
* **Split**: 80/20 train/test split.
* **Algorithms**:
  * **XGBoost Regressor** (100 estimators, learning rate 0.1, max depth 3) — *Top Performer*
  * **Gradient Boosting Regressor** (Scikit-Learn baseline)
* **Outcome**: XGBoost led with an **R² of 0.8835** and lowest Root Mean Squared Error (**$4,252.36**), demonstrating that **Smoking status (78.4%)** and **BMI (13.1%)** are the primary actuarial cost drivers.

---

## 🌐 Interactive Frontend Features

The project includes a modern, zero-dependency static web application:

* **Interactive Tap-to-Inspect**: Tap/click any row, card, or metric to trigger a deep diagnostic modal with:
  * Full scorecard metrics (Silhouette, Accuracy, F1, ROC-AUC, R², RMSE, MAE).
  * Interactive visualizations powered by **Chart.js**:
    * 2D Customer Segmentation Scatter Plot (Clustering)
    * ROC Curve & Interactive Confusion Matrix (Classification)
    * Feature Importance Bar Chart & Actual vs Predicted plots (Boosting)
  * Exact tuned hyperparameters and dataset specs.
  * Analytical insights and production deployment recommendations.
* **Head-to-Head Comparison**: Side-by-side comparison modal between competing algorithms.
* **Search & Filters**: Real-time search by model name, task type, or metric value.
* **Theme Support**: Seamless Dark/Light mode toggle with persistent state.
* **CSV Export**: Instant 1-click export of the benchmark table.

---

## 🚀 Instant Deployment on Vercel

This repository is **100% frontend static**:
* `index.html` sits at the repository root.
* No Node.js build step or backend server required.
* Includes `vercel.json` with security headers and clean URL configuration.

### How to Deploy:
1. Log in to [Vercel](https://vercel.com/).
2. Click **"Add New Project"** -> **"Import Git Repository"**.
3. Select this repository: `AnuragMishra1234/ml-trained`.
4. Leave all build settings at their defaults (Vercel automatically detects static HTML/JS).
5. Click **Deploy**! 🚀

---

## 💻 Local Usage

### 1. View the Website Locally
Simply double-click `index.html` or open it with any local browser or Live Server.

### 2. Re-train Models
```bash
python train_models.py
```
This updates:
* `results.json`
* `results_table.csv`
* `results_summary.md`
* `trained_models/*.joblib`
