# RecA-TB Clean Senior-Review Workflow

This folder contains the cleaned workflow requested by the senior reviewer.

## Main correction
The final workflow now excludes exploratory/failed/probing scripts such as 4a, 4b, 4c, etc. The modeling section only uses:
1. final RFE-selected features,
2. hyperparameter optimization,
3. final trained model,
4. evaluation,
5. SHAP/ADMET interpretation.

## Notebook order
1. `01_RecA_ChEMBL_EC50_Curation_CLEAN.ipynb`
2. `02_RecA_PaDEL_Fingerprint_Matrix_CLEAN.ipynb`
3. `03_RecA_Final_Feature_Selection_RFE_CLEAN.ipynb`
4. `04_RecA_Final_Model_Hyperparameter_Optimization_CLEAN.ipynb`
5. `06_RecA_SHAP_ADMET_Interpretability_CLEAN.ipynb`

## Important methodological fixes
- The final model now uses the final RFE feature subset, not only F-score features.
- Hyperparameters are selected using cross-validated RandomizedSearchCV.
- Extra feature engineering after feature selection is removed from the main workflow.
- Exploratory model probing is excluded from the clean final pipeline.
- The SHAP/ADMET notebook interprets only the final trained model.
