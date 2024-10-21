# Diamond Price Prediction - Machine Learning Pipeline

This project is aimed at building a machine learning pipeline to predict the price of diamonds based on various features like carat, cut, color, clarity, and more. The solution involves data preprocessing, exploratory data analysis (EDA), model selection, and pipeline automation to ensure efficient training and testing.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset Information](#dataset-information)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Modeling Approach](#modeling-approach)
- [Results](#results)
- [References](#references)
- [Contributors](#contributors)

## Project Overview
The goal of this project is to predict the price of diamonds based on several attributes such as carat weight, diamond cut quality, color, and clarity. We implement a machine learning pipeline to handle data ingestion, transformation, and model training using several regression algorithms, ultimately selecting the best performing model.

This project is developed as part of my journey to explore data science, machine learning pipelines, and model deployment in real-world settings.

## Dataset Information
- **Source**: [Kaggle - Playground Series](https://www.kaggle.com/competitions/playground-series-s3e8/data?select=train.csv)
- The dataset contains 10 independent variables describing diamond attributes and 1 target variable (`price`) which represents the price of the diamond.

### Features:
- `carat`: Weight of the diamond.
- `cut`: Quality of the diamond cut (Fair, Good, Very Good, Premium, Ideal).
- `color`: Diamond color, with D (best) to J (worst).
- `clarity`: Diamond clarity grading (I1, SI1, SI2, VS1, VS2, VVS1, VVS2, IF).
- `depth`: Depth of the diamond (total height).
- `table`: Width of the top of the diamond.
- `x`: Length of the diamond (in mm).
- `y`: Width of the diamond (in mm).
- `z`: Depth of the diamond (in mm).
- **Target Variable**: `price`: Price of the diamond (USD).

## Project Structure

```
.
├── artifacts
│   ├── model.pkl                 # Trained model
│   ├── preprocessor.pkl           # Preprocessing object
│   ├── raw.csv                    # Raw data
│   ├── train.csv                  # Training data
│   └── test.csv                   # Test data
├── notebooks
│   ├── data
│   │   └── gemstone.csv           # Original dataset
│   ├── EDA.ipynb                  # Exploratory Data Analysis
│   └── Model Training.ipynb       # Model training process
├── src
│   ├── components
│   │   ├── data_ingestion.py      # Data ingestion component
│   │   ├── data_transformation.py # Data transformation component
│   │   └── model_trainer.py       # Model trainer component
│   ├── pipelines
│   │   ├── prediction_pipeline.py # Pipeline for prediction
│   │   └── training_pipeline.py   # Pipeline for training
│   ├── exception.py               # Custom exception handling
│   ├── logger.py                  # Logging configuration
│   └── utils.py                   # Utility functions
├── templates
│   ├── form.html                  # HTML form for user input
│   └── index.html                 # Home page HTML
├── application.py                 # Flask application entry point
├── requirements.txt               # Required Python packages
├── setup.py                       # Package setup
└── .gitignore                     # Git ignore file
```

## Installation

### 1. Clone the repository
```bash
git clone https://github.com/sarthakkalia/Machine-Learning-Pipeline.git
```

### 2. Navigate to the project directory
```bash
cd Machine-Learning-Pipeline
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the application
```bash
python application.py
```

## Usage
This project uses a Flask web application to serve predictions. You can use the app to:
- Upload diamond attributes through the form.
- Get price predictions based on the trained model.

The application is structured to handle both batch and real-time predictions. Data ingestion, transformation, and model prediction are handled in a seamless end-to-end pipeline.

## Modeling Approach
### Models used:
- `LinearRegression`
- `Lasso`
- `Ridge`
- `ElasticNet`
- `DecisionTreeRegressor`

We trained multiple models and evaluated their performance based on regression metrics such as Mean Squared Error (MSE) and R² score. The best model was selected based on accuracy and generalization performance.

For more details on the pipeline and model selection, check out the repository [here](https://github.com/sarthakkalia/Machine-Learning-Pipeline).

## Results
- **Best Performing Model**: `DecisionTreeRegressor`
- The final model achieved a high R² score on the test set, making it suitable for predicting diamond prices with high accuracy.

## References
- Kaggle Competition Dataset: [Playground Series](https://www.kaggle.com/competitions/playground-series-s3e8/data?select=train.csv)
- [Machine Learning Pipeline](https://github.com/sarthakkalia/Machine-Learning-Pipeline)

## Contributors
- **Sarthak Kumar Kalia** - [LinkedIn](https://www.linkedin.com/in/sarthakkalia/)
