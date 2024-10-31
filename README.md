# Microsoft-Classifying-Cybersecurity-Incidents-with-Machine-Learning

## Project Overview
This project aims to enhance Security Operation Centers (SOCs) by developing a machine learning model to accurately classify cybersecurity incidents. The model predicts the triage grade of incidents—True Positive (TP), Benign Positive (BP), and False Positive (FP)—based on historical evidence and customer responses, ultimately providing SOC analysts with actionable, context-rich recommendations.


---

## Skills Gained
- **Data Preprocessing and Feature Engineering**
- **Machine Learning Classification Techniques**
- **Model Evaluation Metrics (Macro-F1 Score, Precision, Recall)**
- **Cybersecurity Concepts and Frameworks (MITRE ATT&CK)**
- **Handling Imbalanced Datasets**
- **Model Benchmarking and Optimization**

## Business Use Cases
The classification model developed can be applied to various business scenarios:
1. **Security Operation Centers (SOCs)**: Automating triage for incident classification, enabling efficient prioritization for SOC analysts.
2. **Incident Response Automation**: Guiding response systems with automated, tailored actions for specific incident types.
3. **Threat Intelligence**: Enhancing threat detection by integrating historical evidence and customer feedback.
4. **Enterprise Security Management**: Reducing false positives and ensuring prompt attention to actual threats.

---

## Approach

### 1. Data Exploration and Understanding
   - **Initial Inspection**: Load the train dataset, examining the structure, feature types, and target variable distribution.
   - **Exploratory Data Analysis (EDA)**: Use visualizations and statistics to identify patterns, correlations, and anomalies.

### 2. Data Preprocessing
   - **Handling Missing Data**: Identify and handle missing values through strategies such as imputation or removing affected rows.
   - **Feature Engineering**: Create new features or modify existing ones to boost model performance.
   - **Encoding Categorical Variables**: Convert categorical features into numeric representations.

### 3. Data Splitting
   - **Train-Validation Split**: Split the data (e.g., 70-30 or 80-20) to ensure robust model evaluation.
   - **Stratification**: Use stratified sampling to maintain consistent class distributions across splits.

### 4. Model Selection and Training
   - **Baseline Model**: Begin with a simple model, such as Logistic Regression, to set a performance benchmark.
   - **Advanced Models**: Experiment with models like Random Forest, XGBoost, and Neural Networks, optimizing each with grid/random search.
   - **Cross-Validation**: Use k-fold cross-validation for reliable performance estimates and to prevent overfitting.

### 5. Model Evaluation and Tuning
   - **Metrics**: Focus on macro-F1 score, precision, and recall.
   - **Handling Class Imbalance**: Implement strategies like SMOTE, class weights adjustment, or ensemble methods.
   - **Hyperparameter Tuning**: Optimize model performance by fine-tuning key hyperparameters.

### 6. Model Interpretation
   - **Feature Importance**: Identify the most influential features using SHAP values or permutation importance.
   - **Error Analysis**: Analyze common misclassifications to refine the model or add relevant features.

### 7. Final Evaluation
   - **Testing on Unseen Data**: Evaluate model performance on `test.csv` using macro-F1 score, precision, and recall.
   - **Baseline Comparison**: Assess improvements over the baseline model.

---

## Dataset Overview
The GUIDE dataset comprises:
1. **Evidence Level**: Contains individual items (e.g., IP addresses, user details) with metadata.
2. **Alert Level**: Aggregates evidence items to represent potential threats.
3. **Incident Level**: Represents cohesive narratives of security incidents, with labeled triage grades (TP, BP, FP).

The dataset includes 1 million triage-annotated incidents with 45 features, split into training (70%) and test (30%) sets. The data is stratified by Triage Grade, OrgId, and DetectorId to ensure the consistency of incidents.

---


---

## Evaluation Metrics
1. **Macro-F1 Score**: Balanced metric accounting for all classes equally.
2. **Precision**: Accuracy of positive predictions to reduce false positives.
3. **Recall**: Ability to capture all relevant incidents, essential to avoid missing threats.

---
