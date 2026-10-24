# Network Intrusion Detection System (NIDS)

A simple machine learning project to classify network traffic as normal or an attack using the NSL-KDD dataset and TensorFlow/Keras.

## Project Overview
The goal of this project is to build a basic Multi-Layer Perceptron (MLP) neural network to detect network intrusions. I used the NSL-KDD dataset, which is a standard benchmark dataset for network security research.

## Steps Implemented
1. **Data Preprocessing:** 
   - Handled categorical features (protocol type, service, flag) using Label Encoding.
   - Scaled numerical features using `StandardScaler`.
   - Converted the target variable into binary classes (0 for Normal, 1 for Attack).
2. **Model Architecture:**
   - Built a Sequential neural network model using TensorFlow/Keras.
   - Added Dense layers with ReLU activation, Dropout layers for regularization, and an EarlyStopping callback to prevent overfitting.
3. **Evaluation:**
   - Evaluated the model on the test set using accuracy, precision, recall, and a confusion matrix.

## Results
- **Test Accuracy:** ~77%
- **Observation:** The model performs well in identifying normal traffic and specific attacks, but the NSL-KDD test set includes novel attack types not seen during training, which creates a realistic challenge for generalization.

## Requirements
To run this project, you will need Python and the following libraries:
- `pandas`
- `numpy`
- `tensorflow`
- `scikit-learn`
- `matplotlib`
- `seaborn`

## How to Run
1. Download the NSL-KDD dataset files (`KDDTrain.csv` and `KDDTest.csv`) and place them in the project directory.
2. Run the Python script:
   ```bash
   python nids_model.py
