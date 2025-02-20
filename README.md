# CS506-Project
Spring 2025 CS 506 Project Yijun Kim 

**Description of the project**
  - This project aims to employ machine learning techniques to predict mental health treatment outcomes, analyze key factors influencing success of treatments, and cluster patients based on therapy effectiveness. By applying predictive modeling, feature importance analysis, and clustering techniques, we can gain insights into which treatment plans work best for different patient groups. The findings can improve patient adherence by providing evidence-based recommendations for treatment plans and reduce ineffective treatments, leading to better resource allocation in mental healthcare.

- This proposal includes three goals, but only one or two goals will be the focus of the project, according to the comments that will be given to this proposal.

- The data for the project will be collected through the kaggle dataset which contains 500 rows representing real-world mental health diagnoses, treatment plans, and outcomes. It includes patient demographics, symptom severity, medication, therapy types, and progress tracking. However, it should be noted that this dataset is synthetic and created for research and analysis purposes.

**Goal 1: Predictive Model**

The first possible goal of this project is to successfully predict whether a patient’s mental health will improve based on their demographics, symptoms, and treatment adherence. To build a predictive model, the following key features will be used:

1. Diagnosis mental health condition: Categorical; Generalized Anxiety, Major Depressive Disorder, Panic Disorder, Bipolar Disorder
2. Symptom Severity: Numerical; 1-10
3. Medication	Type of medication prescribed: Categorical; SSRIs, Antidepressants, Benzodiazepines, Mood Stabilizers, Antipsychotics
4. Therapy Type: Categorical; CBT, DBT, etc.
5. Sleep Quality: Numertical; 1-10
6. Physical Activity: Numerical; Number of hours spent on physical activity weekly
7. Adherence to Treatment: Numerical; Percentage of adherence to treatment plan
8. Outcome: Categorical; Improved, Deteriorated, No change

**Modeling the Data**
  1.	Data processing

    	The modeling process of the data will include data processing which include the following:
        - Convert categorical features (Diagnosis, Medication, Therapy Type) into numerical values.
        - Normalize numerical features (Symptom Severity, Sleep Quality, Adherence to Treatment).
  3. Model selection
	   - Logistic Regression or random forest will be selected for the predictive modeling.

**Visualization of the Data**
  - The project plans to visualize the data using scatter plot of each of patient features x vs. outcome feature or feature importance graphs that Identifies which factors contribute most to treatment success. 

**Test Plan**
  - The project will train models using an 80/20 train-test split and hyperparameter tuning. It will also use use k-fold cross validation. Evaluation of modeling be conducted using accuracy, precision and recall. F1-score, or ROC-AUC score.


**Goal 2: Feature Importance**

The second possible goal of this project is to identify the most influential factors in treatment success, such as medication type, therapy type, adherence, and lifestyle factors. To determine which factors are most influential in treatment success, we focus on the following key features:

1. Treatment Duration: Numertical; Number of weeks the patient received treatment.
2. Mood Score: Numertical; 1-10
3. Stress Level: Numertical; 1-10
4. Adherence to Treatment: Numertical;	Percentage of adherence to the treatment plan.
5. Outcome: Categorical; Improved, Deteriorated, No change.

**Modeling the Data**
1. Data Processing
   - Convert categorical features (Diagnosis, Medication, Therapy Type) into numerical values.
   - Normalize numerical features (Symptom Severity, Sleep Quality, Adherence to Treatment).
2. Model selection
   - LASSO Regression (L1 Regularization) or Random Forest Feature Importance will be selected. 

**Visualization of the Data**
- The project plans to demonstrate the data through bar Chart of Feature Importance which Highlights the top contributors to positive outcomes or correlation Heatmap that reveals relationships between features, such as high adherence correlating with better outcomes.

**Test Plan**
- The project plans to train models using 80/20 split and validate using K-Fold Cross-Validation.

**Goal 3: Clustering for Therapy Effectiveness**

The last possible goal of the project is to group patients based on therapy effectiveness to determine which therapy types work best for specific patient groups. To effectively cluster patients based on therapy effectiveness, we will use the following key features:

1. Therapy Type: Categorical; CBT, DBT, etc.
2. Treatment Duration: Numertical; Number of weeks the patient received treatment.
3. Outcome: Categorical; Improved, Deteriorated, No change
4. Treatment Progress: Numerical; 1-10
   
**Modeling the Data**
1. Data Processing
   - Convert categorical features (Diagnosis, Medication, Therapy Type) into numerical values.
   - Normalize numerical features (Symptom Severity, Sleep Quality, Adherence to Treatment).
2. Model selection
   - K-Means Clustering with Elbow Method to find optimal K or Agglomerative Clustering (Hierarchical Clustering) will be the choice for the modeling.

**Visualization of Data**
- The project plans to visualize the data through scatter Plots of Therapy Types vs. Treatment Progress which can show which therapy types are associated with higher improvement. Other methods to discuss are heatmaps to display the relationship between therapy type, duration, and effectiveness or t-SNE for Dimensionality Reduction.


**Test Plan**
- The project aims to train models using 80/20 split and validate using K-Fold Cross-Validation and use Silhouette Score to measure clustering quality.
