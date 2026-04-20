# Credit-Scoring-Project
This project focuses on building a high-performance credit scoring model to predict the probability of clients default. The core challenge involved processing large-scale binned and coded banking data and engineering behavioral features to capture credit discipline and debt burden.

**The core challenges** involved:
*   Managing memory efficiency using Dask for "lazy" computation.
*   Processing large-scale binned and coded banking data.
*   Engineering behavioral features to capture credit discipline and debt burden.

**Tech Stack:**
*   Data Processing: Dask (for handling datasets larger than RAM)
*   Machine Learning: CatBoost, Scikit-learn

**Key Features:**
*   Scalable Architecture: Used Dask for "lazy" computing to process data in chunks without memory overflows.
*   Feature Engineering:
    Delinquency Buckets: Categorized overdue periods (e.g., <5d, 5-30d, 90d+).
    Credit Dynamics: Age of oldest credit, limit utilization rates, and total debt burden.
    Clean Logic: Removed data contradictions (e.g., removing >90d delinquencies not yet flagged as defaults).
*   Hyperparameter Tuning: Performed RandomizedSearchCV with 5-fold cross-validation to optimize model stability and AUC.

**The Results**
The final CatBoost Classifier was chosen as the champion model:
*   Metric: ROC-AUC
*   Performance: add upon finalization
*   Best Parameters: Depth: 3, Learning Rate: 0.05, Iterations: 1000.
