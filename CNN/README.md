## CNN Model 
# Replication Steps
1. Clone this repository:
```
   git clone https://github.com/Fitmate-capstone/ML_Model_Development.git
```
2. Navigate to the project directory
3. Place your gym equipment images datasets in the specified directory.
4. Run the Python script for training and evaluation.

# Required Libraries
The necessary libraries for running the gym equipment image classifier script are:
1. numpy
2. pandas
3. scikit-learn
4. tensorflow
5. matplotlib

# Instalation 
Python local
1. Python Environment Setup: Ensure Python is installed.
2. Library Installation: Open the terminal or command prompt and execute the following command: 
```
pip install numpy pandas scikit-learn tensorflow matplotlib
```
Google Colab Notebook
1. Requirements: Access to a Google Colab Notebook.
2. Library Installation: Run the following command in a code cell:
```
!pip install numpy pandas scikit-learn tensorflow matplotlib

```
Kaggle
1. Requirements: Access to a Kaggle Notebook environment.
2. Library Installation: Execute the following command in a code cell if additional libraries are needed:
```
!pip install scikit-learn

```
# Notes
1. For Google Colab and Kaggle, some libraries might already be pre-installed in the environment.
2. Ensure the installation commands are run before importing or using the libraries in your code cells.

# Usage

# Data Preparation
1. Dataset: Place your gym equipment images in the  directory.
2. Data Splitting: The script will automatically split the data into training and validation sets (80:20 ratio).

# Model Training
1. Neural Network Model: The script uses Transfer Learning with MobileNetV2 for classification.
2. Training: Execute the script to train the model
3. Model Saving: The trained model will be saved as model.h5.

![Example](https://ik.imagekit.io/RifqiLukmansyah/download%20(7).png?updatedAt=1703210848214)


