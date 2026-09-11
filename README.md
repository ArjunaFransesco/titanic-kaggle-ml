# 🚢 Titanic Survival Classifier — ML Pipeline & Prediction

A compact, reproducible, and portfolio-ready end-to-end Machine Learning pipeline built to predict passenger survival on the Titanic dataset.

Designed specifically for **Google Colab**, this project automates data ingestion via the Kaggle API, applies modular feature preprocessing using Scikit-Learn pipelines, evaluates baseline performance, and persists artifacts to Google Drive.

---

## 📌 Key Highlights

* **Automated Data Ingestion:** Download competition data securely using the Kaggle API directly within Colab.
* **Leakage-Free Preprocessing:** Data imputation, standard scaling, and categorical encoding encapsulated cleanly in Scikit-Learn `Pipeline` and `ColumnTransformer`.
* **Feature Engineering:** Extraction of passenger title groups, family size calculation, and lone traveler indicators.
* **Diagnostics & Metrics:** Holdout evaluation via Accuracy, ROC-AUC, Precision, Recall, F1-Score, and a Confusion Matrix heatmap.
* **Model Serialization:** Pipeline exported directly to `.joblib` in Google Drive for future deployment.
* **Clean Repo Standards:** Strictly configured `.gitignore` preventing raw data, API keys, and binary models from being pushed to Git.

---

## 🏗️ Pipeline Architecture

```text
Raw Data (Kaggle) ➡️ Feature Extraction & Imputation ➡️ Encoding & Scaling ➡️ Estimator (Logistic Regression) ➡️ Evaluator ➡️ Google Drive (.joblib)


ComponentTarget ColumnsTransformation MethodNumericalAge, Fare, SibSp, ParchSimpleImputer(strategy='median') + StandardScaler()CategoricalSex, Embarked, TitleSimpleImputer(strategy='most_frequent') + OneHotEncoder(handle_unknown='ignore')ModelAll Transformed FeaturesLogisticRegression(max_iter=1000, random_state=42)📁 Repository StructurePlaintexttitanic-kaggle-ml/
├── notebooks/
│   └── titanic_colab_pipeline.ipynb   # Main execution pipeline
├── src/                               # Optional Python modules
│   ├── preprocessing.py
│   └── train.py
├── .gitignore                         # Ignores credentials, datasets, and cache
└── README.md
🚀 How to RunOpen notebooks/titanic_colab_pipeline.ipynb in Google Colab.Download your API token (kaggle.json) from Kaggle Account Settings.Run all cells in order and upload kaggle.json when requested.Authenticate your Google Drive when prompted to export the serialized model to /MyDrive/ml-portfolio/titanic_survival_pipeline.joblib.📊 Evaluation & MetricsValidation Strategy: 80/20 Stratified Train-Test SplitMetrics Tracked: Accuracy, ROC-AUC, Precision, Recall, F1-ScoreVisualizations: Confusion Matrix Heatmap & Feature Importance Coefficients🗺️ Roadmap & Next Steps[ ] Benchmark Random Forest, XGBoost, and LightGBM models.[ ] Implement $k$-Fold Cross-Validation and hyperparameter tuning with Optuna.[ ] Deploy an interactive prediction interface using Streamlit.[ ] Add GitHub Actions for automated code linting and testing.📜 Dataset ReferenceDataset sourced from the Kaggle Titanic: Machine Learning from Disaster competition.

<!-- Last Maintenance Audit: 2026-09-11 -->
