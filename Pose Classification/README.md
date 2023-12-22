## Pose Classification
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
1. pillow==8.1.0
2. matplotlib==3.3.4
3. numpy==1.19.3
4. opencv-python==4.5.1.48
5. tqdm==4.56.0
6. requests==2.25.1
7. mediapipe==0.10.8

# Installation Instructions
Python Local
1. Python Environment Setup: Ensure Python is installed.
2. Library Installation: Open the terminal or command prompt and execute the following command: 
```
pip install pillow==8.1.0
pip install matplotlib==3.3.4
pip install numpy==1.19.3
pip install opencv-python==4.5.1.48
pip install tqdm==4.56.0
pip install requests==2.25.1
pip install mediapipe==0.10.8

```
Google Colab Notebook
1. Requirements: Access to a Google Colab Notebook.
2. Library Installation: Run the following command in a code cell:
```
!pip install pillow==8.1.0
!pip install matplotlib==3.3.4
!pip install numpy==1.19.3
!pip install opencv-python==4.5.1.48
!pip install tqdm==4.56.0
!pip install requests==2.25.1
!pip install mediapipe==0.10.8

```
Kaggle
1. Requirements: Access to a Kaggle Notebook environment.
2. Library Installation: Execute the following command in a code cell if additional libraries are needed:
```
!pip install pillow==8.1.0
!pip install matplotlib==3.3.4
!pip install numpy==1.19.3
!pip install opencv-python==4.5.1.48
!pip install tqdm==4.56.0
!pip install requests==2.25.1
!pip install mediapipe==0.10.8
```
# Notes
1. For Google Colab and Kaggle, some libraries might already be pre-installed in the environment.
2. Ensure the installation commands are run before importing or using the libraries in your code cells.

# Data Preparation
Required image in folder (same use for image out folder):
      Push_Up/
        image_001.jpg
        image_002.jpg
        ...
      deadlift/
        image_001.jpg
        image_002.jpg
        ...
      ...

After organizing the images, zip the folder and name it `fitness_poses_images_in.zip`.
