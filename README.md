# Flood Prediction Dataset

This repository contains information and resources related to the Flood Prediction Dataset from the Kaggle competition [Playground Series - Season 4, Episode 5](https://www.kaggle.com/competitions/playground-series-s4e5/).

## Overview

Flooding is a critical environmental challenge that affects millions of people globally. This dataset provides a simulated environment to develop and test predictive models for flood occurrence based on historical weather and geographical data. The goal is to classify whether a flood event will occur based on the given features.

## Dataset Description

The dataset consists of both training and testing files with labeled and unlabeled examples, respectively. Below are the key features:

- **Features:** Various meteorological, geographical, and temporal variables, such as:
  - `precipitation` (mm)
  - `temperature` (°C)
  - `soil_moisture` (% of saturation)
  - `river_discharge` (cubic meters per second)
  - `elevation` (meters above sea level)
  - Temporal indicators (e.g., `month`, `day_of_week`)

- **Target Variable:**
  - `flood`: Binary label where `1` indicates a flood occurrence and `0` indicates no flood.

### File Structure

- `train.csv`: Contains training data with features and the target variable.
- `test.csv`: Contains testing data without the target variable (for prediction).
- `sample_submission.csv`: Example of the required submission format.

### Data Fields

| Column Name       | Description                                              |
|-------------------|----------------------------------------------------------|
| `id`              | Unique identifier for each record                       |
| `precipitation`   | Total precipitation in millimeters                      |
| `temperature`     | Average temperature in Celsius                          |
| `soil_moisture`   | Percentage of soil moisture saturation                  |
| `river_discharge` | River discharge rate (cubic meters per second)          |
| `elevation`       | Elevation above sea level in meters                     |
| `month`           | Month of the year (1-12)                                |
| `day_of_week`     | Day of the week (1=Monday, 7=Sunday)                    |
| `flood`           | Binary target variable (1=Flood, 0=No Flood) (train.csv)|

## Getting Started

### Prerequisites

To work with the dataset, you need:
- Python 3.8+
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/flood-prediction-dataset.git
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

3. Build your predictive model using machine learning frameworks like `scikit-learn` or `XGBoost`.

### Example Notebook

Refer to the `notebooks/analysis.ipynb` file for a detailed walkthrough of data exploration and modeling.

## Evaluation Metric

Submissions are evaluated using the **F1-Score**, which balances precision and recall for binary classification tasks.

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
