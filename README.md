# Smart Waste Classification System

A Convolutional Neural Network (CNN) that classifies waste into Glass, Organic, and Paper categories with 90.5% test accuracy. Built as an Intelligent Systems final project.

## Overview

Waste misclassification is a real environmental problem — this system uses deep learning to automate sorting decisions that are often made incorrectly by hand. The model was trained on a custom dataset collected and preprocessed by the team, then evaluated against a held-out test set.

## Model Performance

- **Test Accuracy**: 90.5%
- **Glass**: 91.4% F1-score
- **Organic**: 88.4% F1-score
- **Paper**: 91.5% F1-score

Organic waste was the hardest class to classify — likely due to higher visual variability compared to glass and paper, which have more consistent textures and colors.

## Key Design Decisions

**Why CNN?** Convolutional Neural Networks are the standard architecture for image classification because they learn spatial features (edges, textures, shapes) hierarchically — early layers detect simple patterns, deeper layers combine them into object-level features. For waste images with distinct visual properties per category, CNNs outperform traditional ML approaches.

**Data preprocessing** involved collecting raw waste images, organizing them into class folders, and splitting into train/validation/test sets. Image normalization and augmentation were applied to improve generalization.

## Visualizations

![Training Plot](training_plot.png)
![Confusion Matrix](confusion_matrix.png)
![Final Results](final_results.png)

## How to Run

1. Install dependencies:
pip install tensorflow matplotlib seaborn scikit-learn pillow
2. Run the GUI application:
python waste_classifier_ui.py
3. Predict a single image:
python predict.py
## Files

- `train_model.py` - CNN architecture and training pipeline
- `evaluate.py` - Classification report and confusion matrix generation
- `predict.py` - Single image prediction script
- `waste_classifier_ui.py` - Tkinter GUI application
- `demo.py` - Live demo script
- `final_results.py` - Results summary generation

## Team — Group 7, Intelligent Systems

- Samuel Amihere - Model Design & Training
- Mickel Murenzi - Testing, Evaluation & Presentation
- Abdulazeez Dauda - Data Collection, Preprocessing & Implementation

## Tech Stack

- Python, TensorFlow/Keras, scikit-learn, matplotlib, seaborn, Tkinter