# Heart Disease Classification

This project contains notebooks for dataset preparation, feature engineering, model comparison, evaluation, and a Streamlit demo using the Cleveland Heart Disease data.

## Data and setup

The repository does not include CSV data. Download the public `heart.csv` dataset from [Kaggle: Heart Disease UCI](https://www.kaggle.com/datasets/lourenswalters/uci-heart-disease-data-set) yourself and place it at `Data/heart.csv`. The notebooks read this local path; they do not fetch dataset files from a remote URL. Do not commit the CSV files.

The dataset is derived from the Cleveland subset of the UCI Heart Disease dataset (303 instances). Please retain the dataset's attribution and license terms when using it; see the [UCI dataset page](https://archive.ics.uci.edu/dataset/45/heart%2Bdisease) and [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

From a local Jupyter session or Google Colab:

1. Clone this repository.
2. Download `heart.csv` from the Kaggle page above and put it in the repository's `Data/` folder.
3. Run `Solution/[Solution]_Create_Datasets.ipynb` from the repository root or its `Solution/` folder. This creates the processed CSV splits in `Data/`.
4. Run a model notebook in `Solution/`.

The Streamlit notebook also reads `Data/heart.csv` locally. The notebooks use Python with pandas, NumPy, scikit-learn, and model-specific libraries; the Random Forest notebook also includes SHAP analysis.

## Results reported in the CV

The CV reports nine classifiers compared and **Logistic Regression** as the best model, with **87.10% accuracy** and **0.9706 ROC-AUC** on a 31-case test set. The supplied notebooks include several ensemble-model experiments and saved outputs, but those outputs do not reproduce that exact Logistic Regression result. Treat the CV figures as reported results until the matching experiment and split are confirmed.

