# Airline Delay Cause Prediction 

A Deep Learning project aimed at analyzing and predicting flight delays caused by weather conditions. The model classifies whether a flight will have a significant weather delay based on operational data.

##  Project Overview
* **Objective:** Predict if a flight will have a "Weather Delay" greater than 100 minutes.
* **Target Variable:** A binary classification (`WDCase`), where:
    * `1`: Weather Delay > 100 mins.
    * `0`: Minor or no Weather Delay.

##  Data Processing
* **Cleaning:** Removed unnecessary columns (`carrier`, `carrier_name`, `airport`, `airport_name`) and handled missing values using `dropna`.
* **Feature Engineering:** Created a binary target class based on the `weather_delay` threshold.
* **Splitting:** Data split into Training (75%) and Testing (25%).

##  Model Architecture (Keras/TensorFlow)
* **Type:** Sequential Neural Network.
* **Layers:**
    * Input Layer.
    * Hidden Layer 1: 128 Neurons (Activation: `tanh`).
    * Hidden Layer 2: 64 Neurons (Activation: `tanh`).
    * Output Layer: 1 Neuron (Activation: `sigmoid` for binary classification).
* **Optimizer:** `AdamW` with custom learning rate and weight decay.
* **Callbacks:** Used `EarlyStopping` to prevent overfitting by monitoring validation accuracy.

##  Evaluation Results
The model performance was evaluated using:
* **Confusion Matrix:** To visualize True Positives and False Negatives.
* **Classification Report:** Precision, Recall, and F1-Score.
* **Learning Curves:** Plotted Accuracy and Loss over epochs.

##  Technologies Used
* **Python Libraries:** TensorFlow, Keras, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn.
* **Environment:** Google Colab.

---
**Developed by:** [Sherin Shaban]
