# Machine Learning Benchmark Results

Generated from automated training across 3 distinct datasets.

| Dataset | Task | Algorithm | Primary Metric | Full Metrics | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Mall Customers | Clustering | K-Means Clustering | Silhouette: 0.5547 | Silhouette: 0.5547 | Calinski-Harabasz: 248.6 | Davies-Bouldin: 0.5722 | Inertia: 65.6 | **BEST MODEL** |
| Mall Customers | Clustering | Agglomerative Clustering | Silhouette: 0.5538 | Silhouette: 0.5538 | Calinski-Harabasz: 244.4 | Davies-Bouldin: 0.5779 | Runner-up |
| Social Network Ads | Classification | Support Vector Machine (SVC) | Accuracy: 91.25% | Accuracy: 91.25% | F1: 0.8852 | Precision: 0.8438 | Recall: 0.9310 | ROC-AUC: 0.9554 | **BEST MODEL** |
| Social Network Ads | Classification | Random Forest Classifier | Accuracy: 90.00% | Accuracy: 90.00% | F1: 0.8667 | Precision: 0.8387 | Recall: 0.8966 | ROC-AUC: 0.9500 | Runner-up |
| Insurance Premium | Boosting (Regression) | XGBoost Regressor | R²: 0.8835 | R²: 0.8835 | RMSE: $4,252.36 | MAE: $2,400.06 | **BEST MODEL** |
| Insurance Premium | Boosting (Regression) | Gradient Boosting Regressor | R²: 0.8785 | R²: 0.8785 | RMSE: $4,342.91 | MAE: $2,424.53 | Runner-up |
