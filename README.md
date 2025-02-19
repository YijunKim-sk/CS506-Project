# CS506-Project
Spring 2025 CS 506 Project Yijun Kim 

**Description of the project**
  - This project aims to employ machine learning techniques to predict mental health treatment outcomes, analyze key factors influencing success of treatments, and cluster patients based on therapy effectiveness. By applying predictive modeling, feature importance analysis, and clustering techniques, we can gain insights into which treatment plans work best for different patient groups. The findings can improve patient adherence by providing evidence-based recommendations for treatment plans and reduce ineffective treatments, leading to better resource allocation in mental healthcare.

- This proposal includes three goals, but only one or two goals will be the focus of the project, according to the comments that will be given to this proposal.

- The data for the project will be collected through the kaggle dataset which contains 500 rows representing real-world mental health diagnoses, treatment plans, and outcomes. It includes patient demographics, symptom severity, medication, therapy types, and progress tracking. However, it should be noted that this dataset is synthetic and created for research and analysis purposes.

**Goal 1: Predictive Model**
- Successfully predict whether a patient’s mental health will improve based on their demographics, symptoms, and treatment adherence.
  1. What data needs to be collected and how you will collect it
      - To build a predictive model, the following key features will be used:
        1. Diagnosis mental health condition: Categorical; Generalized Anxiety, Major Depressive Disorder, Panic Disorder, Bipolar Disorder
        2. Symptom Severity: Numerical; 1-10
        3. Medication	Type of medication prescribed: Categorical; SSRIs, Antidepressants, Benzodiazepines, Mood Stabilizers, Antipsychotics
        4. Therapy Type: Categorical; CBT, DBT, etc.
        5. Sleep Quality: Numertical; 1-10
        6. Physical Activity: Numerical; Number of hours spent on physical activity weekly
        7. Adherence to Treatment: Numerical; Percentage of adherence to treatment plan
        8. Outcome: Categorical; Improved, Deteriorated, No change
  2. How you plan on modeling the data (e.g. clustering, fitting a linear model, decision trees, XGBoost, some sort of deep learning method, etc.)
     1. Data Processing
        - Convert categorical features (Diagnosis, Medication, Therapy Type) into numerical values.
        - Normalize numerical features (Symptom Severity, Sleep Quality, Adherence to Treatment).
     2. Model selection
        - Logistic Regression
        - Random Forest
  3. How do you plan on visualizing the data? (e.g. interactive t-SNE plot, scatter plot of feature x vs. feature y).
     1. Scatter plot of each of patient features x vs. outcome feature
     2. Feature Importance Graphs: Identifies which factors contribute most to treatment success
  4. What is your test plan? (e.g. withhold 20% of data for testing, train on data collected in October and test on data collected in November, etc.).
     - Train models using an 80/20 train-test split.
     - Hyperparameter Tuning
     - Use k-fold cross validation 
     - Evaluation will be conducted using accuracy, precision and recall. F1-score, or ROC-AUC score

**Goal 2: Feature Importance**
- Identify the most influential factors in treatment success, such as medication type, therapy type, adherence, and lifestyle factors
  1. What data needs to be collected and how you will collect it
     - To determine which factors are most influential in treatment success, we focus on the following key features:
       1. Treatment Duration: Numertical; Number of weeks the patient received treatment.
       2. Mood Score: Numertical; 1-10
       3. Stress Level: Numertical; 1-10
       4. Adherence to Treatment: Numertical;	Percentage of adherence to the treatment plan.
       5. Outcome: Categorical; Improved, Deteriorated, No change
  2. How you plan on modeling the data (e.g. clustering, fitting a linear model, decision trees, XGBoost, some sort of deep learning method, etc.)
     1. Data Processing
        - Convert categorical features (Diagnosis, Medication, Therapy Type) into numerical values.
        - Normalize numerical features (Symptom Severity, Sleep Quality, Adherence to Treatment).
     2. Model selection
        - LASSO Regression (L1 Regularization)
        - Random Forest Feature Importance
  3. How do you plan on visualizing the data? (e.g. interactive t-SNE plot, scatter plot of feature x vs. feature y).
     - Bar Chart of Feature Importance: Highlights the top contributors to positive outcomes.
     - Correlation Heatmap: Reveals relationships between features (e.g., high adherence correlating with better outcomes).
  4. What is your test plan? (e.g. withhold 20% of data for testing, train on data collected in October and test on data collected in November, etc.).
     - Train models using 80/20 split and validate using K-Fold Cross-Validation.

**Goal 3: Clustering for Therapy Effectiveness**
- Group patients based on therapy effectiveness to determine which therapy types work best for specific patient groups.
  1. What data needs to be collected and how you will collect it
     - To effectively cluster patients based on therapy effectiveness, we will use the following key features:
       1. Therapy Type: Categorical; CBT, DBT, etc.
       2. Treatment Duration: Numertical; Number of weeks the patient received treatment.
       3. Outcome: Categorical; Improved, Deteriorated, No change
       4. Treatment Progress: Numerical; 1-10
  2. How you plan on modeling the data (e.g. clustering, fitting a linear model, decision trees, XGBoost, some sort of deep learning method, etc.)
     1. Data Processing
        - Convert categorical features (Diagnosis, Medication, Therapy Type) into numerical values.
        - Normalize numerical features (Symptom Severity, Sleep Quality, Adherence to Treatment).
     2. Model selection
        1. K-Means Clustering (with Elbow Method to find optimal K)
           - K-Means partitions the data into K groups based on similarity.
           - The Elbow Method is used to find the optimal number of clusters by plotting the Within-Cluster Sum of Squares (WCSS) and identifying the point where adding more clusters does not significantly reduce the WCSS.
        2. Agglomerative Clustering (Hierarchical Clustering)
           - This method builds a hierarchy of clusters by merging smaller clusters step by step.
  3. How do you plan on visualizing the data? (e.g. interactive t-SNE plot, scatter plot of feature x vs. feature y).
     - Scatter Plots of Therapy Types vs. Treatment Progress: Shows which therapy types are associated with higher improvement.
     - Heatmaps: Displays the relationship between therapy type, duration, and effectiveness.
     - Cluster Visualizations (t-SNE for Dimensionality Reduction)
  4. What is your test plan? (e.g. withhold 20% of data for testing, train on data collected in October and test on data collected in November, etc.).
     - Train models using 80/20 split and validate using K-Fold Cross-Validation.
     - Use Silhouette Score to measure clustering quality: Measures how similar each patient is to their own cluster vs. other clusters. 
