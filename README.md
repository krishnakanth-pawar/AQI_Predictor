
# Air Quality Index (AQI) Analysis and Prediction

## Overview

This project performs **exploratory data analysis, interactive visualization, and neural network–based prediction of Air Quality Index (AQI)** using historical city-wise air pollution data.
The workflow includes data preprocessing, visual analytics using Plotly, and AQI prediction using a TensorFlow-based Artificial Neural Network (ANN).

---

## Dataset


* **Description:** City-level daily air pollution and AQI measurements from open-source data from Kaggle.
* **Key Columns Used:**

  * `Date`, `City`, `AQI`
  * Pollutants: `PM2.5`, `PM10`, `NO`, `NO2`, `NOx`, `NH3`, `CO`, `SO2`, `O3`, `Benzene`, `Toluene`, `Xylene`

---

## Data Preprocessing

* Loaded dataset using **Pandas**
* Checked and removed missing values using row-wise deletion
* Converted `Date` column to `datetime` format
* Split dataset into features and target variable (`AQI`)
* Standardized feature values using **StandardScaler**

---

## Exploratory Data Analysis & Visualization

Interactive visualizations are created using **Plotly**:

1. **AQI Trend Over Time**

   * Line plot of AQI variation across dates for different cities

2. **AQI Distribution by City**

   * Box plot showing AQI spread and variability across cities

3. **Scatter Plot Matrix**

   * Visual relationship between major pollutants and AQI
   * Includes compatibility fallback for older Plotly versions

---

## Machine Learning Model

### Model Type

* **Artificial Neural Network (ANN)** using TensorFlow (Keras)

### Architecture

* Input Layer: 12 pollutant features
* Hidden Layers:

  * Dense (64 units, ReLU)
  * Dense (32 units, ReLU)
* Output Layer:

  * Dense (1 unit) for AQI prediction

### Training Configuration

* Optimizer: Adam
* Loss Function: Mean Squared Error (MSE)
* Epochs: 30
* Batch Size: 32
* Validation Split: 20%

---

## Model Evaluation

* Evaluated on a held-out test set (20% of data)
* Performance metric:

  * **Mean Squared Error (MSE)**
* Training and validation loss trends visualized using **Matplotlib**

---

## Technologies Used

* **Python**
* **Pandas**, **NumPy**
* **Plotly Express & Graph Objects**
* **Scikit-learn**
* **TensorFlow / Keras**
* **Matplotlib**

---

## How to Run

1. Install required dependencies:

   ```bash
   pip install pandas plotly scikit-learn tensorflow matplotlib
   ```

2. Ensure dataset is present in the project directory

3. Run the script or notebook sequentially to:

   * Preprocess data
   * Generate visualizations
   * Train the neural network
   * Evaluate model performance

---

## Output

* Interactive AQI visualizations
* Scatter matrix of pollutant relationships
* Training vs validation loss curve
* Test-set Mean Squared Error for AQI prediction

---

## Author

**Krishnakanth Pawar**

---
