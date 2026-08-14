# Titanic Survival Classifier

A compact, portfolio-ready machine-learning project that predicts passenger survival on the Titanic. The notebook is designed for **Google Colab**: it downloads the Kaggle competition data, trains a reproducible scikit-learn pipeline, evaluates it, and saves the model to Google Drive.

## What it demonstrates

- Kaggle API dataset download in Colab
- Feature engineering and preprocessing with `ColumnTransformer`
- Baseline logistic-regression classifier
- Holdout evaluation with accuracy, classification report, and confusion matrix
- Model persistence to Google Drive with `joblib`

## Run it

1. Open [`notebooks/titanic_colab_pipeline.ipynb`](notebooks/titanic_colab_pipeline.ipynb) in Google Colab.
2. Create a Kaggle API token at [Kaggle Settings](https://www.kaggle.com/settings), then upload `kaggle.json` when the notebook asks. Keep this token private.
3. Run the cells from top to bottom. The trained model is saved as `MyDrive/ml-portfolio/titanic_survival_pipeline.joblib`.

The notebook uses Kaggle's [Titanic competition dataset](https://www.kaggle.com/competitions/titanic/data). This project does not commit datasets, credentials, or trained-model binaries to GitHub.

## Next improvements

- Compare Logistic Regression with Random Forest and Gradient Boosting
- Add cross-validation and a simple experiment table
- Publish a Streamlit prediction demo

