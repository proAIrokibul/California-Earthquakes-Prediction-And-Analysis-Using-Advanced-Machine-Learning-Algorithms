# Earthquakes-Prediction-And-Analysis-Using-Advanced-Machine-Learning-Algorithms

# Earthquake Prediction Project

## Project Overview
This project focuses on predicting earthquake-prone cities or counties in the USA based on a dataset containing geographical and administrative details. The dataset includes latitude, longitude, state name, city, county, and more. The primary goal is to identify whether a city is prone to earthquakes based on the historical data of occurrences.

## Dataset Description
The dataset includes the following columns:
- **ID:** Unique identifier for each entry.
- **STATE_CODE:** Code representing the state.
- **STATE_NAME:** Name of the state.
- **CITY:** Name of the city where the earthquake occurred.
- **COUNTY:** County of the occurrence.
- **LATITUDE & LONGITUDE:** Geographical coordinates of the location.

## Preprocessing
- Missing values were handled by filling or dropping incomplete rows.
- Categorical columns were encoded using label encoding to prepare them for modeling.

## Feature Engineering
A binary target column was created to label cities/counties as “prone” if they had more than 10 earthquakes in the dataset. This created a balanced target column to train our models effectively.

## Modeling & Algorithms
Three classification algorithms were applied to predict earthquake-prone areas:

1. **Logistic Regression**
   - **Accuracy:** 92.15%
   - The model achieved high accuracy but failed to identify prone cities correctly. It predicted all entries as non-prone, resulting in poor recall and F1-score for the prone class.

2. **Random Forest**
   - **Accuracy:** 92.59%
   - The model slightly improved on the prone class with a few correct predictions. The precision of the prone class increased, but the recall remained low, indicating further improvements are needed.

3. **XGBoost**
   - **Accuracy:** 92.15%
   - XGBoost achieved moderate precision for the prone class but still had low recall and F1-score. It shows potential with more parameter tuning or feature engineering.

## Evaluation Metrics
The models were evaluated using accuracy, confusion matrix, and classification reports, including precision, recall, and F1-score. Despite high accuracy, all models struggled with correctly identifying the prone class due to data imbalance and the nature of the features.

## Future Improvements
- **Addressing Data Imbalance:** Implement techniques like SMOTE to handle class imbalance.
- **Feature Engineering:** Explore additional geographical and seismic features that could improve predictions.
- **Hyperparameter Tuning:** Optimize the models to improve recall and F1-scores for the prone class.

## Conclusion
The project lays a foundation for predicting earthquake-prone regions, but further work is needed to achieve balanced performance across all classes. Improving recall for the prone cities will make these predictions more reliable. 

