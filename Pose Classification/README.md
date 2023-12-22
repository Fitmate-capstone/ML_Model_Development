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
# Pose classification and repetition counting with the k-NN algorithm
Building a pose classifier that recognizes specific fitness poses and counts repetitions. In this section we describe how we built a custom pose classifier using the MediaPipe. To recognize poses we use the k-nearest neighbors algorithm (k-NN) because it's simple and easy to start with. The algorithm determines the object's class based on the closest samples in the training set.
# 1. Data Preparation
We collected image samples of the target exercises from various sources. We chose a few hundred images for each exercise, such as Push up and Deadlift. It's important to collect samples that cover different camera angles, environment conditions, body shapes, and exercise variations.
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
# 2. Run pose detection on the sample images
This produces a set of pose landmarks to be used for training. We are not interested in the pose detection itself, since we will be training our own model in the next step.

The k-NN algorithm we've chosen for custom pose classification requires a feature vector representation for each sample and a metric to compute the distance between two vectors to find the target nearest to the pose sample. This means we must convert the pose landmarks we just obtained.

To convert pose landmarks to a feature vector, we use the pairwise distances between predefined lists of pose joints, such as the distance between wrist and shoulder, ankle and hip, and left and right wrists. Since the scale of images can vary, we normalized the poses to have the same torso size and vertical torso orientation before converting the landmarks.

# 3. Train the model and count repetitions
We used the MediaPipe to access the code for the classifier and train the model.

To count repetitions, we used another Colab algorithm to monitor the probability threshold of a target pose position.4

https://ik.imagekit.io/RifqiLukmansyah/pushups-sample-out%20(2).mp4?updatedAt=1703210317710
