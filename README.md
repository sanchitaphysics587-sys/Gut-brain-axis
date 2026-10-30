# Gut-brain-axis-
This production-grade machine learning pipeline is designed for the high-dimensional analysis of gut microbiome data. Implemented in Python, the pipeline automates the ingestion, transformation, feature selection, and classification of taxonomic relative abundance profiles to predict neurological states and biological phenotypes.

Key Features & Architectural Workflow:

• Tidy-to-Tabular Data Transformation: Implements robust pipelines utilizing pandas to reshape, melt, and pivot raw long-format OTU tables and public repository data (such as American Gut Project cohorts) into optimized wide-format feature matrices.

• L1-Regularized Feature Selection: Integrates a built-in Lasso penalization layer using SelectFromModel and LogisticRegression to aggressively reduce dimensions, filter statistical noise, and isolate the most predictive microbial biomarkers.

• Ensemble Classification Modeling: Employs a finely-tuned GradientBoostingClassifier optimized with custom learning rates and subsampling to accurately capture complex, non-linear multi-species interactions.

• Stratified Cross-Validation: Evaluates pipeline generalizability and prevents data leakage across patient cohorts using stratified K-fold cross-validation. It assesses model performance via precise metrics including LogLoss, receiver operating characteristic (ROC) curves, and area under the curve (AUROC).

• Explainable AI (XAI) Attribution: Integrates SHAP (SHapley Additive exPlanations) through TreeExplainer to calculate mathematical variable importance. It automatically exports publication-grade diagnostic beeswarm plots mapping exactly how specific neuroprotective or neurotoxic bacterial species drive the global model predictions.
