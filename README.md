# Flood Prediction Dataset

This repository contains information and resources related to the Flood Prediction Dataset from the Kaggle competition [Playground Series - Season 4, Episode 5](https://www.kaggle.com/competitions/playground-series-s4e5/).

## Overview

Flooding is a critical environmental challenge that affects millions of people globally. This dataset provides a simulated environment to develop and test predictive models for flood occurrence based on various environmental, geographical, and socio-economic factors. The goal is to classify whether a flood event will occur based on the given features.

## Dataset Description

The dataset consists of both training and testing files with labeled and unlabeled examples, respectively. Below are the key features:

### Features

| Feature Name                     | Description                                           |
|----------------------------------|-------------------------------------------------------|
| `MonsoonIntensity`               | Intensity of monsoon rainfall                        |
| `TopographyDrainage`             | Topographical factors affecting water drainage       |
| `RiverManagement`                | Effectiveness of river management practices          |
| `Deforestation`                  | Impact of deforestation in the area                 |
| `Urbanization`                   | Degree of urban development                          |
| `ClimateChange`                  | Indicators of climate change impact                  |
| `DamsQuality`                    | Structural and operational quality of dams           |
| `Siltation`                      | Level of silt accumulation in water bodies           |
| `AgriculturalPractices`          | Influence of farming practices on water systems      |
| `Encroachments`                  | Presence of unauthorized land use                    |
| `IneffectiveDisasterPreparedness`| Quality of disaster management systems               |
| `DrainageSystems`                | Efficiency of urban and rural drainage systems       |
| `CoastalVulnerability`           | Susceptibility of coastal areas to flooding          |
| `Landslides`                     | Incidence of landslides contributing to floods       |
| `Watersheds`                     | Health and management of watershed areas             |
| `DeterioratingInfrastructure`    | Aging or inadequate infrastructure                   |
| `PopulationScore`                | Impact of population density                         |
| `WetlandLoss`                    | Loss of wetlands affecting natural water regulation  |
| `InadequatePlanning`             | Shortcomings in urban and regional planning          |
| `PoliticalFactors`                | Political influences on flood management policies    |
| `FloodProbability`               | Target variable (1=Flood, 0=No Flood) (train.csv)    |

### File Structure

- `train.csv`: Contains training data with features and the target variable.
- `test.csv`: Contains testing data without the target variable (for prediction).
- `sample_submission.csv`: Example of the required submission format.

## Machine Learning Models and Techniques

This project leverages multiple machine learning models and techniques for flood prediction:

### Models Used

- **LightGBM (LGBM):** A gradient boosting framework that is fast and efficient for tabular data.
- **H2O AutoML:** An automated machine learning platform to quickly build and optimize models.
- **Artificial Neural Networks (ANN):** Deep learning-based approach for capturing non-linear relationships.
- **XGBoost:** Extreme Gradient Boosting, known for its performance and accuracy in structured data tasks.

### Hyperparameter Optimization

- **Optuna:** Used for hyperparameter optimization across all models to achieve better performance by searching for optimal configurations.

### Evaluation Metric

Submissions are evaluated using the **F1-Score**, which balances precision and recall for binary classification tasks.

## Getting Started

### Prerequisites

To work with the dataset, you need:
- Python 3.8+
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `lightgbm`, `xgboost`, `h2o`, `optuna`

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/rassien/flood-prediction-dataset.git
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Usage

1. Load the dataset:
   ```python
   import pandas as pd
   train_data = pd.read_csv('data/train.csv')
   test_data = pd.read_csv('data/test.csv')
   ```

2. Explore the dataset:
   ```python
   print(train_data.head())
   print(train_data.info())
   ```

3. Train models and optimize hyperparameters using Optuna:
   ```python
   import optuna
   # Define objective function for model optimization
   ```

### Example Notebook

Refer to the `notebooks/analysis.ipynb` file for a detailed walkthrough of data exploration, modeling, and optimization.

## Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin feature-name`.
5. Submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

Special thanks to Kaggle for providing this dataset and competition platform. For more information, visit the [competition page](https://www.kaggle.com/competitions/playground-series-s4e5/).
