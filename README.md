# Asteroid Diameter Prediction

A machine learning regression project that investigates whether astronomical and orbital characteristics can be used to predict asteroid diameter.

## Project Overview

This project applies supervised machine learning techniques to an asteroid dataset to predict asteroid diameter from available numerical and categorical characteristics.

The workflow covers data preparation, feature selection, exploratory analysis, model development, and regression performance evaluation.

The project was implemented in Python using a Jupyter Notebook.

---

## Objectives

The main objectives of this project were to:

* Prepare and clean an asteroid dataset for machine learning.
* Remove non-predictive identification fields.
* Handle missing values and duplicate observations.
* Encode categorical variables for machine learning.
* Identify important predictive features using a Random Forest model.
* Develop a Decision Tree regression model.
* Evaluate prediction performance using standard regression metrics.
* Visualise feature importance and the final Decision Tree structure.

---

## Dataset

The project uses an asteroid dataset containing astronomical and orbital characteristics, with **diameter** as the prediction target.

During preprocessing, non-predictive identification fields were removed, including:

* `id`
* `name`
* `full_name`
* `pdes`
* `prefix`

The notebook handles missing values, removes duplicate records, and converts categorical variables into numerical representations.

> **Dataset note:** The original dataset is not included in this repository unless redistribution rights permit it. The notebook can be configured to use a locally downloaded copy of the dataset.

---

## Methodology

The project follows the workflow below:

```text
Raw Asteroid Dataset
        │
        ▼
Data Cleaning
        │
        ├── Remove non-predictive fields
        ├── Handle missing values
        └── Remove duplicates
        │
        ▼
Categorical Encoding
        │
        ▼
Feature Selection
        │
        └── Random Forest Feature Importance
        │
        ▼
Top 10 Selected Features
        │
        ▼
Train/Test Split
        │
        ▼
Feature Scaling
        │
        ▼
Decision Tree Regression
        │
        ▼
Model Evaluation
```

---

## Feature Selection

A `RandomForestRegressor` was used to estimate feature importance and identify the ten features selected for the final modelling stage.

The selected features were:

```text
H
albedo
spkid
tp_cal
e
n
per
om
a
tp
```

This step reduced the modelling feature set and provided an interpretable view of which variables contributed most strongly to the prediction task.

---

## Machine Learning Model

### Decision Tree Regression

A `DecisionTreeRegressor` was trained using the selected features.

The model was evaluated using:

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² Score

---

## Results

The final model produced the following results on the evaluation data:

| Metric |    Result |
| ------ | --------: |
| MAE    | 1.3846 km |
| MSE    |   13.2205 |
| RMSE   | 3.6360 km |
| R²     |    0.8427 |

The R² value of **0.8427** indicates that the model captured a substantial proportion of the variation in asteroid diameter within the evaluation data.

The MAE of **1.3846 km** provides an estimate of the average absolute prediction error in kilometres.

---

## Visualisations

The notebook includes visual analysis of:

* Feature importance
* Selected features
* Model performance
* Decision Tree structure

These visualisations provide additional insight into the modelling process and the relationship between the selected features and predicted asteroid diameter.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Project Structure

```text
asteroid-diameter-prediction/
│
├── asteroid_diameter_prediction.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/asteroid-diameter-prediction.git
cd asteroid-diameter-prediction
```

Install the required Python packages:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
asteroid_diameter_prediction.ipynb
```

---

## Reproducibility

To reproduce the analysis:

1. Obtain the asteroid dataset used by the notebook.
2. Place the dataset in the expected project location.
3. Update the dataset path in the notebook if necessary.
4. Install the required dependencies.
5. Run the notebook cells sequentially.

---

## Key Skills Demonstrated

This project demonstrates practical experience with:

* Data cleaning
* Exploratory data analysis
* Feature engineering
* Feature selection
* Random Forest modelling
* Decision Tree regression
* Regression evaluation
* Data visualisation
* Python-based machine learning workflows
* Jupyter Notebook development

---

## Author

**Nonhle Mnqayi**

ICT Graduate | Cybersecurity Honours Student

GitHub: `YOUR-GITHUB-USERNAME`

LinkedIn: `https://www.linkedin.com/in/nonhle-okuhle-973581274/`
