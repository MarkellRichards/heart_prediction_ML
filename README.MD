# Heart Disease Prediction Using Machine Learning

## Overview

Cardiovascular diseases (CVDs) claim approximately 17.9 million lives annually, highlighting a significant global health crisis. This project leverages a comprehensive dataset to develop machine learning models aimed at predicting the likelihood of heart disease in individuals. Early identification of risk factors facilitates preventive measures, potentially saving lives and reducing premature deaths. The insights provided by this project can guide patient care and inform public health strategies.

## Project Workflow

This project follows a systematic five-step approach:

1. Data Collection: Using a dataset sourced from Kaggle containing various health attributes relevant to CVD.
2. Exploratory Data Analysis: Understanding data distributions and relationships between features.
3. Feature Engineering: Cleaning and transforming data for optimal model training, including handling zero values in key features.
4. Model Selection & Training: Implementing K-Nearest Neighbors (KNN) and Logistic Regression, with feature engineering pipelines.
5. Model Evaluation: Assessing model performance using techniques like GridSearchCV for hyperparameter tuning and analyzing model accuracy.

## Dataset Description

The dataset includes the following features:

- `Age`: age of the patient [years]
- `Sex`: sex of the patient [M: Male, F: Female]
- `ChestPainType`: chest pain type [TA, ATA, NAP, ASY]
- `RestingBP`: resting blood pressure [mm Hg]
- `Cholesterol`: serum cholesterol [mg/dl]
- `FastingBS`: fasting blood sugar [binary]
- `RestingECG`: electrocardiogram results [Normal, ST, LVH]
- `MaxHR`: maximum heart rate achieved
- `ExerciseAngina`: exercise-induced angina [binary]
- `Oldpeak`: ST depression value
- `ST_Slope`: slope of peak exercise ST segment [Up, Flat, Down]
- `HeartDisease`: target class [1: disease, 0: Normal]

## Results

### K-Nearest Neighbors (KNN)

- Best Parameters: {'classifier**metric': 'minkowski', 'classifier**n_neighbors': 10, 'feature_selection\*\*k': 11}
- Best Cross-Validation Score: 0.87
- Test Set Accuracy: 0.88

### Logistic Regression

- Best Parameters: {'classifier**C': 1, 'classifier**penalty': 'l2', 'feature_selection\*\*k': 10}
- Best Cross-Validation Score: 0.86
- Test Set Accuracy: 0.86

## Future Work

To improve model performance, we plan to explore advanced algorithms such as Random Forest and Gradient Boosting. Enhancing the feature engineering process through interaction terms and polynomial features, as well as balancing the dataset with synthetic data generation techniques, will be considered. Additionally, gathering more data from diverse sources could provide further insights and enhance model generalizability.

## Getting Started

To reproduce the results or build upon this project, follow these steps:

## Clone the repository:

1. git clone https://github.com/MarkellRichards/heart_prediction_ML.git

2. Install docker desktop

3. Run jupyter docker stack of choice in a container using the following command (modify as necessary):
   ```bash
   # Example
   docker run -it --rm -p 10000:8888 -v "${PWD}":/home/jovyan/work quay.io/jupyter/datascience-notebook:2024-10-07
   ```
   Jupyter Docker Stacks documentation: https://jupyter-docker-stacks.readthedocs.io/en/latest/

Alternatively, can create a requirements.txt and use a python virtual environment or conda.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request with your changes.

## License

This project is licensed under the MIT License.
