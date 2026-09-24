# Datamites-Capstone-Project-Heart-disease-Prediction



# Heart Disease Prediction



## Project Overview



This project focuses on analyzing patient health data and developing a machine learning model to predict the presence of heart disease.



The project includes data analysis, data preprocessing, exploratory data analysis (EDA), multiple machine learning model development and comparison, hyperparameter tuning, and selection of the best-performing model for production.



The complete analysis and modeling workflow has been implemented in a single Jupyter Notebook as required by the project guidelines.



## Project Objectives



The main objectives of this project are:



\- Perform a complete analysis of the available patient data.

\- Explore relationships and patterns in the healthcare features.

\- Preprocess the data appropriately for machine learning.

\- Build and evaluate multiple machine learning classification models.

\- Compare the performance of the different models.

\- Perform hyperparameter tuning on the selected model.

\- Identify the best model for production based on its performance.

\- Provide useful suggestions to the hospital based on the model predictions.

\- Document the challenges encountered during the project and the techniques used to address them.



\## Dataset



The dataset contains patient-level information related to heart disease.



There are 14 columns in the dataset description, where `patient\_id` is a unique and random identifier. The remaining features describe demographic information, clinical measurements, electrocardiography results, and exercise-related characteristics.



### Dataset Features



| Feature | Type | Description |

|---|---|---|

| `patient\_id` | Identifier | Unique and random patient identifier |

| `slope\_of\_peak\_exercise\_st\_segment` | Integer | Slope of the peak exercise ST segment |

| `thal` | Categorical | Thallium stress test result: normal, fixed\_defect, reversible\_defect |

| `resting\_blood\_pressure` | Integer | Resting blood pressure |

| `chest\_pain\_type` | Integer | Chest pain type (4 values) |

| `num\_major\_vessels` | Integer | Number of major vessels (0–3) colored by fluoroscopy |

| `fasting\_blood\_sugar\_gt\_120\_mg\_per\_dl` | Binary | Fasting blood sugar greater than 120 mg/dl |

| `resting\_ekg\_results` | Integer | Resting electrocardiographic results (0, 1, 2) |

| `serum\_cholesterol\_mg\_per\_dl` | Integer | Serum cholesterol in mg/dl |

| `oldpeak\_eq\_st\_depression` | Float | ST depression induced by exercise relative to rest |

| `sex` | Binary | 0: Female, 1: Male |

| `age` | Integer | Age in years |

| `max\_heart\_rate\_achieved` | Integer | Maximum heart rate achieved in beats per minute |

| `exercise\_induced\_angina` | Binary | 0: False, 1: True |





## Data Analysis and Preprocessing



The project includes exploratory data analysis (EDA) to understand the dataset, identify patterns, and examine the characteristics of the target variable.



The following steps were performed during the data preparation and modeling workflow:



\- Loaded and inspected the patient data.

\- Checked the structure and data types of the dataset.

\- Separated the features and target variable.

\- Examined categorical and numerical variables.

\- Applied appropriate preprocessing techniques to prepare the data for machine learning.

\- Encoded the categorical `thal` feature using one-hot encoding.

\- Applied feature scaling where required using `StandardScaler`.

\- Split the dataset into training and testing sets using an 80:20 ratio.

\- Used stratification during the train-test split to maintain the target-class distribution.

\- Built preprocessing and modeling pipelines for the final model.



The notebook contains the detailed exploratory analysis, visualizations, preprocessing steps, and outputs.





## Machine Learning Models



Multiple classification models were developed and evaluated to predict the presence of heart disease.



The following models were considered:



1\. Logistic Regression

2\. K-Nearest Neighbors (KNN)

3\. Decision Tree Classifier

4\. Random Forest Classifier

5\. Gradient Boosting Classifier



The models were evaluated using classification performance metrics, including:



\- Accuracy

\- Precision

\- Recall

\- F1 Score

\- ROC-AUC



The project also includes hyperparameter tuning using `GridSearchCV` for the Gradient Boosting model. The grid search used 5-fold cross-validation and ROC-AUC as the scoring metric. :contentReference\[oaicite:0]{index=0}





## Model Comparison



The following classification models were evaluated on the test dataset:



| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |

|---|---:|---:|---:|---:|---:|

| Gradient Boosting | 0.9167 | 0.8421 | 1.0000 | 0.9143 | 0.9562 |

| K-Nearest Neighbors | 0.8889 | 0.8750 | 0.8750 | 0.8750 | 0.9141 |

| Random Forest | 0.8333 | 0.7778 | 0.8750 | 0.8235 | 0.9359 |

| Logistic Regression | 0.8056 | 0.7647 | 0.8125 | 0.7879 | 0.9406 |

| Decision Tree | 0.8056 | 0.8462 | 0.6875 | 0.7586 | 0.8000 |



The models were compared using Accuracy, Precision, Recall, F1 Score, and ROC-AUC. The results show that Gradient Boosting achieved the highest Accuracy, Recall, F1 Score and ROC-AUC, making it the best-performing model among the evaluated models.



## Final Model Selection



Based on the model comparison, the Gradient Boosting Classifier was selected as the final model for this project.



The original Gradient Boosting model achieved:



\- \*\*Accuracy:\*\* 91.67%

\- \*\*Precision:\*\* 84.21%

\- \*\*Recall:\*\* 100.00%

\- \*\*F1 Score:\*\* 91.43%

\- \*\*ROC-AUC:\*\* 95.62%



The model achieved a recall of 100%, meaning it correctly identified all positive heart disease cases in the test set.



### Hyperparameter Tuning



Hyperparameter tuning was performed for the Gradient Boosting model using `GridSearchCV` with 5-fold cross-validation.



However, the tuned Gradient Boosting model did not improve the performance on the held-out test dataset. Its ROC-AUC decreased from 0.9562 to 0.9281.



Therefore, the original Gradient Boosting model was retained as the final model.



The trained final model has been saved as:



`Models/heart\_disease\_gradient\_boosting.pkl`







## Challenges Faced and Techniques Used



During the project, several challenges were encountered while preparing the data and developing the machine learning models.



| Challenge | Technique Used | Reason |

|---|---|---|

| The dataset contained a categorical `thal` feature. | One-Hot Encoding | One-hot encoding was used to convert the categorical values into a numerical representation suitable for machine learning models. |

| Numerical features had different scales. | StandardScaler | Feature scaling was used so that numerical variables with different ranges could be processed appropriately by the models. |

| Multiple machine learning algorithms had to be evaluated. | Model Comparison | Several classification models were trained and evaluated using Accuracy, Precision, Recall, F1 Score, and ROC-AUC to identify the most suitable model. |

| The selected Gradient Boosting model required performance optimization. | GridSearchCV with 5-fold cross-validation | Hyperparameter tuning was performed to search for better model parameters while using cross-validation. |

| Hyperparameter tuning did not improve the final test-set performance. | Comparison of tuned and original models | The tuned model was compared with the original Gradient Boosting model on the held-out test set. Since tuning reduced performance, the original model was retained. |



The detailed challenges, preprocessing steps, model evaluation, and experimentation are documented in the project Jupyter Notebook.



## Technologies Used



\- Python

\- Jupyter Notebook

\- Pandas

\- NumPy

\- Matplotlib

\- Seaborn

\- Scikit-learn

\- Joblib

\- Git \& GitHub





## Installation / Requirements



### 1. Clone the Repository



```bash

git clone <your-github-repository-url>

cd Heart-Disease-Prediction



pip install pandas numpy matplotlib seaborn scikit-learn joblib jupyter



jupyter notebook



Open the `heart\_disease\_prediction` notebook and run the cells sequentially.





### How to Run the Project



1\. Clone the repository to your local system.

2\. Install the required Python libraries.

3\. Open Jupyter Notebook.

4\. Open the `heart\_disease\_prediction` notebook.

5\. Make sure `labels.csv` and `values.csv` are available in the project folder.

6\. Run the notebook cells sequentially from beginning to end.

7\. Review the model predictions and evaluation results.



## Limitations



\- The model is trained on a limited dataset and may not represent all patient populations.

\- The prediction depends on the quality and accuracy of the input data.

\- The model provides a prediction based on historical data and should not be considered a medical diagnosis.

\- The system does not replace consultation with a qualified healthcare professional.

\- Further validation on larger and more diverse datasets is required before real-world clinical use.





## Future Enhancements



\- Integrate a hospital suggestion feature based on the patient's location and predicted risk level.

\- Deploy the machine learning model as a web application for easier access.

\- Improve model performance using larger and more diverse datasets.

\- Add real-time prediction capabilities.

\- Explore advanced machine learning and ensemble techniques.

\- Implement model monitoring and regular retraining with updated data.




## Disclaimer



This project is developed for educational and research purposes only. The heart disease prediction model provides an estimated prediction based on the input data and should not be considered a medical diagnosis. Users should consult a qualified healthcare professional for medical advice, diagnosis, or treatment decisions.





## Team Members



\- Supriya Warghude

\- Sinchana M C

\- Roshni Kumari

\- Srikanth Vunnam



## My Contribution

This was a collaborative team project developed by four members. The project work was divided among team members and integrated into a common repository.

My primary contribution was Exploratory Data Analysis (EDA), which included:

\- Understanding the structure and characteristics of the dataset.
\- Analyzing the distribution of the target variable.
\- Identifying patterns and relationships between features.
\- Performing univariate and bivariate analysis.
\- Creating visualizations to understand feature distributions and correlations.
\- Identifying relevant insights from the data to support further preprocessing and model development.


## Additional Contribution – Power BI Dashboard

In addition to the project requirements, I independently developed a **Power BI dashboard** to further explore and visualize the heart disease dataset.

The dashboard was created as an additional visualization component to present the data in an interactive and easy-to-understand format.

### My Contribution

* Independently developed the complete Power BI dashboard
* Prepared and transformed the data using **Power Query**
* Created required calculations and measures using **DAX**
* Designed interactive visualizations, KPIs, and filters
* Presented key patterns in the dataset through an interactive dashboard

### Tools Used

* **Power BI**
* **Power Query**
* **DAX**

### Dashboard Preview

![Heart Disease Analysis Dashboard](Power%20BI/Heart%20Disease%20Analysis%20Dashboard.png)


