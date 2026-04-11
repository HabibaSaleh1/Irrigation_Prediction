# Irrigation_Prediction
Project Overview
Effective irrigation management is critical for sustainable agriculture. This project utilizes a Deep Learning approach to classify irrigation needs, processing a dataset of 630,000 entries across 21 features including soil pH, moisture, rainfall, and crop growth stages.

Dataset Description
The dataset contains several categorical and numerical features:

Numerical Features: Soil_pH, Soil_Moisture, Organic_Carbon, Electrical_Conductivity, Temperature_C, Humidity, Rainfall_mm, Sunlight_Hours, Wind_Speed_kmh, Field_Area_hectare, and Previous_Irrigation_mm.

Categorical Features: Soil_Type (4 unique), Crop_Type (6 unique), Crop_Growth_Stage (4 unique), Season (3 unique), Irrigation_Type (4 unique), Water_Source (4 unique), Mulching_Used (2 unique), and Region (5 unique).

Methodology
1. Data Preprocessing
To prepare the data for the neural network, the following transformations were applied:

Scaling: RobustScaler was used for numerical features to handle outliers effectively.

Encoding:

OrdinalEncoder and OneHotEncoder were used to transform categorical variables into a machine-readable format.

Target labels (Irrigation_Need) were mapped from categorical values (Low, Medium, High) to numerical values for multi-class classification.

2. Model Architecture
The solution implements a Sequential Deep Learning Model built with TensorFlow/Keras:

Dense Layers: Multiple fully connected layers to capture complex feature relationships.

Regularization: Integrated L1 and L2 regularization alongside Dropout layers to prevent overfitting.

Stability: BatchNormalization was used to ensure stable and faster training.

Output Layer: A Softmax activation layer for 3-class classification.

3. Training and Optimization
Optimizers: Experimentation with Adam and SGD (Stochastic Gradient Descent).

Callbacks:

EarlyStopping: Monitored validation loss to stop training when improvements ceased.

ModelCheckpoint: Saved the best-performing model iteration.

Repository Structure
irrigation_prediction.ipynb: Comprehensive notebook including data exploration, preprocessing, and model training.

submission2.csv: A sample output file containing predictions for the test set.

Requirements
Python 3.x

Pandas & NumPy

Scikit-learn

TensorFlow / Keras

Matplotlib & Seaborn
