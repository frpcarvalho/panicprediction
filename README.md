Panic Prediction

Description

This repository contains the code and resources for a machine learning project focused on predicting panic disorder using NHANES data from 1999-2004. The project implements data processing, merging datasets across cycles, feature engineering, model training with Gradient Boosting Classifier, handling class imbalance via SMOTE, and interpretability analysis using SHAP values.

Key objectives:

Merge and preprocess NHANES datasets.

Create a target variable for panic prediction based on CIQPANIC data.

Train and evaluate a predictive model.

Analyze feature importance and generate visualizations.

Repository Structure

code_panic.ipynb: The main Jupyter notebook containing all code for data processing, model training, evaluation, SHAP analysis, and visualizations.

combined_datasets/: (Generated) Directory for merged CSV files from NHANES cycles.

shap_importance_gb.csv: Feature importance from SHAP analysis.

shap_values.csv: Raw SHAP values.

shap_summary_plot.png: SHAP summary plot visualization.

shap_feature_importance.png: SHAP feature importance bar plot.

shap_analysis_report.md: Detailed report on SHAP analysis insights.

Prerequisites

Python 3.x

Required libraries:

pandas

numpy

scikit-learn

imbalanced-learn (for SMOTE)

shap

matplotlib

seaborn

scipy

plotly (for interactive plots, if used)

Install dependencies:

pip install pandas numpy scikit-learn imbalanced-learn shap matplotlib seaborn scipy plotly

How to Use

Clone the repository:

git clone https://github.com/frpcarvalho/panicprediction.git
cd panicprediction

Download NHANES data: Place the raw NHANES datasets (1999-2000, 2001-2002, 2003-2004) in the appropriate directories as specified in the notebook (e.g., /Users/filipecarvalho/Documents/data_science_projects/PANICPRED/NHANES_YYYY_YYYY).

Run the notebook:

Open code_panic.ipynb in Jupyter Notebook or JupyterLab.

Execute cells sequentially to process data, train the model, and generate outputs.

Key Outputs:

Merged datasets in combined_datasets/.

Trained model evaluation metrics (classification report, confusion matrix).

SHAP visualizations and report.

Model Details

Algorithm: Gradient Boosting Classifier with hyperparameters: n_estimators=200, max_depth=5, learning_rate=0.1.

Preprocessing: Median imputation for numerics, label encoding for categoricals, StandardScaler, SMOTE for imbalance.

Evaluation: Stratified train-test split (70/30), cross-validation, ROC AUC, confusion matrix.

Interpretability: SHAP for feature importance and impact analysis.

Contributing

Fork the repository.

Create a branch: git checkout -b feature/new-feature.

Commit changes: git commit -m 'Add new feature'.

Push: git push origin feature/new-feature.

Open a Pull Request.

License

This project is licensed under the MIT License - see the LICENSE file for details.

Contact

[frpcarvalho] - For questions or collaborations.
