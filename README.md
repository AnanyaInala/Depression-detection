# Depression-detection
This project focuses on detecting depression from EEG data using a Convolutional Neural Network (CNN) and providing personalized recommendations based on user survey responses. It integrates EEG signal classification, mental health survey assessment, and a GUI built with Tkinter.

🧠 Overview
EEG Signal Processing: Reads EEG datasets in .csv format and preprocesses them for classification.

CNN Model: Detects depression using a deep learning model trained on EEG features.

Survey Module: Collects additional self-reported symptoms using a 4-question Likert scale survey.

Recommendation System: Offers tailored mental health suggestions based on survey scores.

GUI: User-friendly Tkinter interface to handle EEG upload, prediction, survey, and display results.


🔧 Features
Load and process EEG data from CSV files.

Automatically train or load a CNN for depression detection.

Predict whether the EEG signals indicate "Normal" or "Depressed".

Provide a 4-question mental health survey with score interpretation.

Suggest mental health recommendations based on survey score.

📊 How It Works
EEG Upload: User uploads EEG data via the GUI.

Model Prediction: Data is passed through a CNN to classify depression.

User Survey: After selecting a record, the user completes a brief survey.

Recommendation: Based on average survey score:

Score < 2: Positive mental health message

Score 2–4: Mild support suggestions (e.g., mindfulness, exercise)

Score > 4: Recommend therapy or guided mental health support

🛠 Requirements

Python 3.x

numpy, pandas, keras, tensorflow, sklearn

tkinter (built-in for most Python installs)
📈 Dataset
The project assumes the input EEG dataset:

Is a .csv file.

Contains numerical EEG features with the last column labeled as "Label" (0 or 1).

🧪 CNN Architecture
Conv2D with 32 filters (3x3)

MaxPooling2D

Flatten layer

Dense (256 units, ReLU)

Output Dense layer with 2 classes (Softmax)

📌 Limitations
Currently works only with EEG features formatted in 18x18x3 shape.

Survey is basic; can be extended to use validated psychological scales (e.g., PHQ-9).

Not a substitute for professional mental health diagnosis.
