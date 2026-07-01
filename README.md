This file represents the initial prototype or experimental version of the system developed before the final release.
# NOTE : This file contains describtion for DDH and Lower-Extrimety Fracture.

# First Model : Lower-Extrimety Fracture .
What does it contain?

1. Environment Preparation
Installation of libraries.
Import of tools.
Selection of GPU.

2. Data Preparation

Includes:

Image Transformations
CLAHE
Data Augmentation
3. Classification Model Building

Based on:

DenseNet121

For classifying radiographic images.

4. Model Training

Includes:

Training
Validation
Loss Curves
5. Model Evaluation

Includes:

Classification Report
Confusion Matrix
6. Interpreting Results Using Grad-CAM

Displays the regions the model relied on during decision-making.

This helps in interpreting the AI ​​results.

7. Using YOLO

The YOLO model was used to detect injury areas within the radiographic image.

8. Injury Severity Assessment

This section includes logic for determining injury severity based on model results.

9. Final Report

This section includes:

Classification results.

YOLO results.

Injury severity.

Medical advice.

Purpose of the document

This document represents the initial version in which most of the project's concepts, such as:

Classification
GradCAM
YOLO Detection
Severity Assessment, were tested and developed before being integrated and refined into the final version.

--------------------------------------------------------------------------------------------------------

# Second Model : DDH .
Brief Description

This file contains a comprehensive system for diagnosing Developmental Dysplasia of the Hip (DDH) using artificial intelligence and deep learning techniques. It begins with classifying radiographic images, then identifies keypoints, calculates the severity of the injury, and finally provides a report and medical guidance.

What's Included?

1. Environment Setup
Installation of required libraries.
Import of all libraries.
Automatic selection of GPU or CPU.
Linking to Google Drive when using Google Colab.

2. Image Preprocessing

Includes:

CLAHE for contrast enhancement of radiographic images.

Image Normalization.

Image Transformations.

Gaussian Heatmaps for Keypoint Training. 3. Classification Model

Based on:

DenseNet121

Used to classify X-rays into:

Normal
DDH

The model is trained and evaluated using:

Accuracy
Precision
Recall
F1-score
Test-Time Augmentation (TTA)

4. Keypoint Detection Model

Includes a model based on:

DenseNet121 Encoder
Heatmap Decoder

Identifies keypoints specific to the hip joint.

It also includes:

Soft-Argmax
Heatmap Loss
PCK Metric
OKS Metric
5. Medical Measurements

Calculates important indicators such as:

Acetabular Index (AI)
Anatomical measurements necessary to determine the severity of injury.

6. Severity Assessment

This relies on measurements extracted from keypoints to determine the severity of the injury.

7. Medical Guidance

After determining the severity of the injury, the system displays:

Severity level
Appropriate medical recommendations
A simplified interpretation of the result
8. Model Training

The file contains:

Data Loading
Data Segmentation
DataLoaders
Training Loops
Validation
Evaluation
Plotting training curves
9. Full Diagnosis Pipeline

Finally, there is a complete pipeline that:

Loads the X-ray image

Classifies it
Extracts keypoints
Calculates measurements
Determines the severity of the injury
Displays the final diagnostic report

Purpose of the file

This file represents the complete, integrated system for the project, which combines all stages of diagnosis within a single notebook.
