# NIH- chest xray

models explored - Densenet121, used GRADCAM(inspired0
MobilnetNetV2, RestNet50V2, rf, knn, dt, svm

Problem Statement: The problem is the need for an accurate and timely interpretation of chest X-ray images to assist healthcare professionals in diagnosing and treating various lung diseases effectively.The primary objective of this proposed framework work is to detect and classify various lung diseases from standard X-ray images and Computerized Tomography (CT) scan images with the help of volume datasets.
Solution: Developing an AI-based chest X-ray prediction system that utilizes deep learning algorithms to analyse and interpret chest X-ray images. The system is capable of detecting and classifying abnormalities. The main contribution of this research is the development of this new Hybrid deep learning algorithm suitable for predicting lung disease from X-ray images.

This NIH Chest X-ray Dataset contains 30,805 distinct patients' 112,120 X-ray images labelled with diseases.
<img width="884" alt="Screenshot 2023-07-04 at 5 45 54 PM" src="https://github.com/mahima-srivastavaa/NIH-/assets/138587088/82c22cd0-3a5b-40de-8598-b86672de492e">

in nihxray notebook
Importing Libraries:

The code begins by importing various libraries required for data processing, visualization, and model training/testing.
The libraries include pandas, os, matplotlib, seaborn, scikit-learn, NumPy, TensorFlow, Keras, and OpenCV.
Loading and Preparing Data:

The code reads data from a CSV file ("Data_Entry_2017.csv") using pandas.
The data contains information about chest X-ray images and their associated labels.
The labels are processed and divided into training, validation, and test datasets.
Checking for Patient Overlap:

The code checks for overlapping patients between different datasets (train, validation, and test).
It prints the number of overlapping patients.
Data Exploration and Visualization:

The code visualizes sample chest X-ray images from the training dataset using matplotlib.
Data Preprocessing:

The code applies data augmentation and standardization using the Keras ImageDataGenerator to the training, validation, and test datasets.
Model Creation:

The code loads the DenseNet121 model, a pre-trained CNN model, without the top classification layer.
It adds a custom dense output layer for binary classification of each label.
Model Training:

The code compiles and trains the model using the ImageDataGenerators on the training dataset.
It saves the model's weights to a file.
Model Evaluation:

The code evaluates the model's performance on the test and additional test datasets.
It calculates the ROC-AUC score for each label and plots the ROC curves.
Visualization of Grad-CAM:

Grad-CAM (Gradient-weighted Class Activation Mapping) is used to visualize which regions of the input images contribute the most to the model's predictions for selected labels.
The code generates Grad-CAM heatmaps for specific images and selected labels.
Note: The code uses the Kaggle environment for execution, as evident from the paths and imports specific to Kaggle. The results and plots may vary if executed in a different environment. Additionally, the code snippet contains an undefined variable ("fitter") in the last part of model evaluation. This might lead to an error during execution.

Overall, the code demonstrates a comprehensive workflow for medical image classification using transfer learning with the DenseNet121 model.


