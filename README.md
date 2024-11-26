<img src="Banner.png">

# Project Description
In this project, we developed a machine learning model to predict student employability using mock interview data from the Technological Institute of the Philippines. The XGBClassifier achieved 85% accuracy by analyzing professional attributes, with Mental Alertness identified as the most critical factor. The research provides a scalable framework for educational institutions to enhance students' job readiness through data-driven insights.

## Highlights
* 86% Test Accuracy was achieved using XGBoost and Random Undersampling.
* Mental Alertness was the top global feature predicting employability of TIP students based on SHAP value.
* DiCE counterfactuals provide individualized insights and recommendations for students’ areas of improvement.
* 80% accuracy was achieved with a random sample of only 500 data points, indicating good deployment feasibility.

## Methodology
**Data Preparation:**
Student Name and Student Performance Score were dropped, the latter due to the fact that this information would only be available after an OJT experience. Feature engineering was considered but not implemented. This included calculating the total sum of all features, as well as their average. This did not improve accuracy and would also present difficulty in interpretation.

**Data Exploration:**
The project commenced with a thorough examination of the dataset, which revealed a slight imbalance in the target variable for binary classification. An analysis of the features indicated that all were ordinal, with a moderate level of correlation observed among them, yet no direct strong correlation to the target class was detected. The proportional chance criterion was calculated at 1.25 times chance, resulting in a threshold of 64%.

**Model and Resampling Method Selection:**
The core of the methodology involved comparing various machine learning models and resampling techniques to address class imbalance and optimize performance. The models tested included Gradient Boosting Machine, XGBoost, Random Forest, Decision Tree, Logistic Regression (L2), and K-Nearest Neighbors. Resampling methods evaluated were Random Oversampling, Random Undersampling, TomekLinks, and No Resampling, explicitly excluding methods like SMOTE due to the ordinal nature of the data. The training dataset underwent resampling to mitigate the impact of class imbalance.

**Hyperparameter Tuning and Model Evaluation:**
Hyperparameter optimization was conducted through GridSearchCV for each combination of model and resampling method to enhance training accuracy. Performance metrics such as test accuracy, precision, recall, and Area Under the ROC Curve (AUC) were meticulously recorded for evaluation and comparison purposes.

**Final Model Production:**
Upon determining the optimal combination of model, parameters, and resampling method, the final model was constructed and applied to the resampled training dataset to prepare for deployment and further interpretability analysis.

**Interpretability:**
The interpretability segment aimed to explain the model's decision-making process, divided into global and local interpretability. Global interpretability involved using SHAP to calculate the average impact of each feature. Local interpretability was demonstrated through case studies of two students, analyzing the specific features that influenced their employability predictions using SHAP, followed by utilizing DiCE for generating counterfactual scenarios to suggest paths for achieving the desired classification.

**Deployability:**
The concluding phase focused on the deployability of the model, specifying the data collection prerequisites for institutions aspiring to implement a similar predictive system based on mock interviews. This involved repeated sampling of the original dataset at different levels, and recording a model's accuracy. 

## Authors
* CoKehyeng, Ian Joseph C.
* Laylo, Rex Gregor M.
* Orenday, John Cris J.
* Singian, Miguel Lorenzo M.
* Uy, Gregory Patrick A.

## References
1. Commission on Higher Education: Revised Guidelines for Student Internship Program in the Philippines (SIPP) for All Programs (CMO No. 104, S. 2017). Retrieved March 10, 2024. https://ched.gov.ph/wp-content/uploads/2018/03/CMO-NO.-104-S.-2017.pdf
2. Huss, R., Jhileek, T., Butler, J.: Mock Interviews in the Workplace: Giving Interns the Skills They Need for Success. The University of West Georgia and Academy for Advanced Studies (2017)
3. Lipovetsky, S., Conklin, M.: Analysis of regression in game theory approach. Applied Stochastic Models in Business and Industry 17(4) (2001)
4. Mothlilal, R., Sharma, A., Tan, C.: Explaining machine learning classifiers through diverse counterfactual explanations. Conference on Fairness, Accountability, and Transparency, 607-617 (2020)
5. Casuat, C.D., Festijo, E.D., Alon, A.S.: Predicting Students' Employability using Support Vector Machine: A SMOTE-Optimized Machine Learning System. International Journal of Emerging Technologies in Engineering Research (IJETER) 10(2) (2020)
6. Vo, M.-T., Nguyen, T., Le, T.: OPT-BAG Model for Predicting Student Employability. Computers, Materials & Continua 76(2) (2023)
7. Kaggle - Students' Employability Dataset - Philippines. Retrieved February 23, 2024. https://www.kaggle.com/datasets/anashamoutni/students-employability-dataset