# Disease Data Preparation

## Project Overview
This project focuses on data preparation and preprocessing using the Healthcare Stroke Prediction Dataset.

The notebook cleans the dataset, handles missing values, removes duplicate records, performs data visualization, encodes categorical variables, and scales numerical features.

## Dataset
**Dataset Name:** Healthcare Stroke Prediction Dataset

**Dataset File:** `healthcare-dataset-stroke-data.csv`

### Dataset Features
- `id` – Unique patient identifier.
- `gender` – Gender of the patient.
- `age` – Age of the patient.
- `hypertension` – Whether the patient has hypertension.
- `heart_disease` – Whether the patient has heart disease.
- `ever_married` – Marital status.
- `work_type` – Type of occupation.
- `Residence_type` – Type of residence.
- `avg_glucose_level` – Average glucose level.
- `bmi` – Body Mass Index.
- `smoking_status` – Smoking status.
- `stroke` – Stroke occurrence (target variable).

## Technologies Used
- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## Data Preparation Steps

1. **Load Dataset:** Read the healthcare stroke dataset using Pandas.
2. **Dataset Exploration:** Check the number of rows, columns, data types, and statistical information.
3. **Remove Unnecessary Column:** Remove the `id` column because it has no predictive meaning.
4. **Check Missing Values:** Identify missing values in the dataset.
5. **Handle Missing Values:** Replace missing BMI values with the median BMI.
6. **Remove Duplicates:** Remove duplicate records.
7. **Handle Gender Values:** Remove the single record with gender value `Other`.
8. **Data Visualization:** Create a histogram of glucose levels and a bar chart of stroke cases by smoking status.
9. **Categorical Encoding:** Convert `ever_married` into numerical values and apply one-hot encoding to other categorical columns.
10. **Feature Scaling:** Apply StandardScaler to age, average glucose level, and BMI.
11. **Save Cleaned Dataset:** Export the processed data into `cleaned_stroke_data.csv`.

## Data Visualization
The notebook includes:
- Histogram showing the distribution of glucose levels.
- Bar chart showing stroke cases by smoking status.

## Feature Encoding
- `ever_married`: Yes = 1, No = 0.
- One-hot encoding is applied to gender, work type, residence type, and smoking status.
- `drop_first=True` is used to avoid redundant dummy columns.

## Feature Scaling
StandardScaler is used to standardize:
- Age
- Average Glucose Level
- BMI

The standardized values have a mean of approximately 0 and a standard deviation of approximately 1.

## Installation

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## How to Run
1. Open Google Colab or Jupyter Notebook.
2. Upload `Disease_Data_preparation.ipynb`.
3. Upload `healthcare-dataset-stroke-data.csv`.
4. Run all cells sequentially.
5. The cleaned dataset will be saved as `cleaned_stroke_data.csv`.

## Output
**Generated File:** `cleaned_stroke_data.csv`

The output contains the cleaned, encoded, and scaled healthcare dataset.

## Objective
To understand and implement essential data preprocessing techniques using a real-world healthcare dataset and prepare the data for further machine learning analysis.

## Conclusion
The project demonstrates important data preparation techniques, including missing value handling, duplicate removal, data visualization, categorical encoding, and feature scaling. The resulting dataset is ready for further machine learning experimentation.
