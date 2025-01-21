# Steel_Energy_consumption

## Overview
The aim of this project is to analyze and predict the energy consumption in kilowatt-hours (kWh) within the steel manufacturing process. The insights gained from this study can help industries enhance productivity while minimizing energy waste and environmental impact.

## Data Description
### SOURCE :
Dataset can be downloaded from the link:https://archive.ics.uci.edu/dataset/851/steel+industry+energy+consumption

### Features :
* date: Timestamp in string format.
* Usage_kWh (float64) – The total energy consumed in kilowatt-hours (kWh). (Target Variable)
* Lagging_Current_Reactive.Power_kVarh (float64) – The reactive power consumption when the current lags behind the voltage (measured in kilovar-hours, kVarh).
* Leading_Current_Reactive_Power_kVarh (float64) – The reactive power consumption when the current leads the voltage (measured in kVarh).
* CO2(tCO2) (float64) – Carbon dioxide emissions associated with energy consumption, measured in metric tons of CO2.
* Lagging_Current_Power_Factor (float64) – The power factor when the current lags the voltage (percentage).
* Leading_Current_Power_Factor (float64) – The power factor when the current leads the voltage (percentage).
* NSM (int64) – "Number of Seconds from Midnight" – a time-based feature representing the time of the day in seconds.
* WeekStatus (object) – Indicates whether the recorded data is from a "Weekday" or "Weekend".
* Day_of_week (object) – The specific day of the week (e.g., Monday, Tuesday, etc.).
*Load_Type (object) – The category of power usage, classified as "Light_Load", "Medium_Load", or "Maximum_Load".

## Usage

1.Data Preprocessing:
Run data_preprocessing.py to clean and preprocess the dataset.

2.Feature Selection:
Execute feature_selection.py to select relevant features for modeling.

3.Model Training:
Use model_training.ipynb to train various models and perform hyperparameter tuning.

4.Model Evaluation:
Evaluate the model's performance using metrics like MAE,	MSE, RMSE,	R² Score.

5.Predicting Unseen Data:
Load the saved model and use it to make predictions on new unseen data.

## Conclusion

In this project, we developed and evaluated multiple machine learning models to predict steel industry energy consumption based on various input features. The dataset underwent extensive preprocessing, including feature scaling, before being used to train different regression models.

Among the tested models, Gradient Boosting emerged as the best-performing model, achieving an R² score of 0.9917 after hyperparameter tuning. This indicates that the model can explain 99.17% of the variance in energy consumption, demonstrating a high level of accuracy.

To ensure model generalization, predictions were made on unseen data using the saved Gradient Boosting model. The predicted values varied across different input conditions, reflecting the model's ability to adapt to various energy consumption patterns.

While the model performed exceptionally well on the test set, further validation on real-world unseen data is recommended to assess its robustness. Potential areas for improvement include experimenting with additional feature selection techniques, fine-tuning hyperparameters further, and incorporating more diverse training data.

Overall, this project successfully developed a highly accurate predictive model for steel industry energy consumption, which can be valuable for optimizing energy efficiency and reducing operational costs in industrial settings.
