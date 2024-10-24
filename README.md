# California-Earthquakes-Prediction-And-Analysis-Using-Advanced-Machine-Learning-Algorithms

## Project Overview
This project centers on predicting earthquake-prone cities and counties in California based on a dataset containing geographical and administrative details. California, being one of the most seismically active regions in the USA, provides an ideal case study for earthquake prediction. The primary goal is to identify which cities or counties are prone to earthquakes, leveraging historical data on earthquake occurrences within the state.

## Dataset Description
The dataset includes the following columns:
- **ID:** Unique identifier for each entry.
- **STATE_CODE:** Code representing the state (California in this case).
- **STATE_NAME:** Name of the state (California).
- **CITY:** Name of the city where the earthquake occurred.
- **COUNTY:** County of the occurrence.
- **LATITUDE & LONGITUDE:** Geographical coordinates of the location.

## Preprocessing
- Missing values were addressed by either filling or removing incomplete rows.
- Categorical columns, such as state name and county, were label encoded to prepare them for the modeling process.

## Feature Engineering
To create a binary target column, cities/counties were labeled as “prone” if they experienced more than 10 earthquakes according to the dataset. This helped generate a balanced target variable for effective model training.

## Modeling & Algorithms
Three classification algorithms were applied to predict earthquake-prone areas in California:

1. **Logistic Regression**
   - **Accuracy:** 92.15%
   - While achieving high overall accuracy, the model struggled to correctly predict earthquake-prone cities. It predicted most entries as non-prone, leading to low recall and F1-score for the prone class.

2. **Random Forest**
   - **Accuracy:** 92.59%
   - This model provided a slight improvement in predicting earthquake-prone areas, with higher precision for the prone class, though recall remained low. It correctly identified a few prone cities but still missed many.

3. **XGBoost**
   - **Accuracy:** 92.15%
   - XGBoost demonstrated moderate precision for the prone class but, like the other models, had a low recall and F1-score. With further tuning, XGBoost shows potential to improve its performance.

## Evaluation Metrics
The models were evaluated based on accuracy, confusion matrix, and classification reports (precision, recall, and F1-score). Despite high overall accuracy, all models faced challenges in correctly predicting earthquake-prone cities due to data imbalance and the complexity of earthquake prediction.

## Future Improvements
- **Handling Data Imbalance:** Implement techniques such as SMOTE (Synthetic Minority Over-sampling Technique) to address the class imbalance between prone and non-prone areas.
- **Enhanced Feature Engineering:** Incorporate additional seismic and geographical features, such as fault line proximity, depth of earthquakes, and magnitude history, which could enhance the models' predictive power.
- **Hyperparameter Tuning:** Further tuning of the models to improve recall and F1-scores for the earthquake-prone class is needed for more balanced performance.

## Conclusion
This project serves as a valuable starting point for predicting earthquake-prone regions within California. While current models demonstrate high accuracy, their ability to correctly identify prone cities remains a challenge. Focusing on improving recall and optimizing the models will lead to more reliable predictions, potentially aiding disaster preparedness and risk mitigation in California's earthquake-prone areas.
