🧠 MNIST Handwritten Digit Recognition using MLP

Machine Learning • Neural Networks • MLP • Image Classification • TensorFlow/Keras

A machine-learning laboratory project for handwritten digit classification using a Multi-Layer Perceptron (MLP) trained on the MNIST dataset. The project covers data exploration, preprocessing, baseline model development, controlled hyperparameter experiments, final-model evaluation, confusion-matrix analysis, and misclassification analysis.

🚀 Project Overview

The objective is to build and evaluate a neural-network model capable of recognizing handwritten digits from 0 to 9.

MNIST Dataset
      ↓
Data Exploration
      ↓
Preprocessing & Normalization
      ↓
Train / Validation Split
      ↓
Baseline MLP
      ↓
Hyperparameter Experiments
      ↓
Final Model
      ↓
Test Evaluation
      ↓
Confusion Matrix
      ↓
Misclassification Analysis

✨ Key Features

🔢 Handwritten digit classification for 10 classes (0–9)

🖼️ Visualization of MNIST samples

📊 Class-distribution analysis

🧠 Multi-Layer Perceptron neural network

⚙️ Architecture, batch-size, learning-rate, and epoch experiments

📈 Training and validation accuracy/loss analysis

⏱️ Training-time comparison

🧩 Confusion-matrix evaluation

❌ Misclassified-image analysis

💾 Model saving and reloading

🖼️ Dataset Exploration

The project visualizes sample MNIST digits and examines the distribution of the ten digit classes.



Figure: Sample MNIST images and training-set class distribution.

Recorded training-set class counts:

Digit 0 : 5923
Digit 1 : 6742
Digit 2 : 5958
Digit 3 : 6131
Digit 4 : 5842
Digit 5 : 5421
Digit 6 : 5918
Digit 7 : 6265
Digit 8 : 5851
Digit 9 : 5949

🧠 MLP Architecture

The baseline model uses two hidden layers:

Input Layer
     ↓
Dense Layer: 128 neurons
     ↓
Dense Layer: 64 neurons
     ↓
Output Layer: 10 classes

🧪 Hyperparameter Experiments

Multiple controlled experiments were performed by varying network architecture, batch size, learning rate, and number of training epochs.

Architecture:
Baseline       → (128, 64)
Arch_smaller   → (64)
Arch_wider     → (256, 128)

Batch Size:
32, 64, 128

Learning Rate:
0.001, 0.01, 0.0005

Epochs:
5, 10, 15, 20



Figure: Hyperparameter experiment results.

⏱️ Training Accuracy vs. Training Time

The experiments were also compared in terms of training accuracy and computational time.



Figure: Training accuracy versus training time across experiments.

📈 Final Model Training

The training curves show the evolution of training and validation accuracy and loss over epochs.



Figure: Final model accuracy and loss over epochs.

🎯 Final Model Performance

Training Accuracy   : 99.49%
Validation Accuracy : 97.52%
Test Accuracy       : 97.58%
Test Loss           : 0.1311
MSE                 : 0.004116

The final model achieved 97.58% accuracy on the 10,000-image MNIST test set.

🧩 Confusion Matrix

The confusion matrix provides class-wise information about correct predictions and the digit classes that are most frequently confused.



Figure: Confusion matrix of the final model on the MNIST test set.

❌ Misclassification Analysis

The final model misclassified 242 out of 10,000 test images. The following examples illustrate some of the incorrect predictions.



Figure: Examples of misclassified MNIST test images.

✅ Correctly Classified Examples

Examples of correctly classified test images are also shown to provide a visual check of successful predictions.



Figure: Examples of correctly classified MNIST test images.

💾 Model Saving and Reloading

The trained model is saved in Keras format and can be reloaded for subsequent evaluation or inference.

mnist_mlp_final.keras

Train
  ↓
Save Model
  ↓
Reload Model
  ↓
Evaluate
  ↓
Predict

🛠️ Technologies Used

Python

TensorFlow / Keras

NumPy

Pandas

Matplotlib

Seaborn

Scikit-learn

Jupyter Notebook / Google Colab

📁 Recommended GitHub Structure

MNIST-Handwritten-Digit-Recognition-MLP/
│
├── README.md
├── MNIST_MLP.ipynb
├── mnist_mlp_final.keras
│
└── output-images/
    ├── mnist-sample-distribution.png
    ├── hyperparameter-results.png
    ├── training-time-comparison.png
    ├── final-training-curves.png
    ├── confusion-matrix.png
    ├── misclassified-images.png
    └── correctly-classified-images.png

▶️ How to Run

1. Clone the repository.

2. Install TensorFlow, NumPy, Pandas, Matplotlib, Seaborn, and Scikit-learn.

3. Open the MNIST notebook in Jupyter Notebook or Google Colab.

4. Run the cells sequentially from dataset loading through evaluation.

5. Inspect the training curves, confusion matrix, and error analysis outputs.

🎓 Learning Outcomes

Machine-learning workflow design

Multi-Layer Perceptron neural networks

Image classification

Data preprocessing

Hyperparameter experimentation

Training/validation analysis

Confusion-matrix interpretation

Misclassification analysis

Model persistence and inference

🔬 Possible Future Improvements

Compare the MLP with a Convolutional Neural Network (CNN)

Experiment with dropout and regularization

Add early stopping and learning-rate scheduling

Perform per-class precision and recall analysis

Build an interactive handwritten-digit drawing interface

⭐ Project Highlights

🔢 MNIST Digit Classification
🧠 Multi-Layer Perceptron
⚙️ Hyperparameter Experiments
📈 Accuracy & Loss Analysis
⏱️ Training-Time Comparison
🧩 Confusion Matrix
❌ Misclassification Analysis
💾 Model Saving & Reloading
🐍 Python
⚡ TensorFlow / Keras

👨‍💻 Author

AmarDeep Dwivedi
M.Tech Research
Electrical Engineering — CSPML
IIT Dharwad

📜 License

This project is intended for educational and research purposes.
