# 🧠 MNIST Handwritten Digit Recognition using MLP

<p align="center">
<b>Machine Learning • Neural Networks • MLP • Image Classification • TensorFlow/Keras</b>
</p>

A machine-learning laboratory project for handwritten digit classification using a **Multi-Layer Perceptron (MLP)** trained on the **MNIST dataset**. The project covers data exploration, preprocessing, baseline model development, controlled hyperparameter experiments, final-model evaluation, error analysis, and prediction on handwritten digit images.

---

## 🚀 Project Overview

The objective is to build and evaluate a neural-network model capable of recognizing handwritten digits from **0 to 9**.

The project follows a complete machine-learning workflow:

```text
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
      ↓
Custom Handwritten Digit Prediction
```

---

## ✨ Key Features

- 🔢 Handwritten digit classification for 10 classes (0–9)
- 🖼️ Visualization of MNIST samples
- 📊 Class-distribution analysis
- 🧠 Multi-Layer Perceptron neural network
- ⚙️ Architecture experiments
- 📦 Batch-size experiments
- 📈 Learning-rate experiments
- ⏱️ Training-time comparison
- 📉 Training and validation loss analysis
- 📈 Training and validation accuracy analysis
- 🧩 Confusion-matrix evaluation
- ❌ Misclassified-image analysis
- 💾 Model saving and reloading
- ✍️ Prediction on handwritten digit images

---

# 🖼️ Dataset

The project uses the **MNIST handwritten digit dataset**, containing grayscale images of handwritten digits from 0 to 9.

Each image is represented as a grayscale pixel array and processed before being supplied to the MLP.

Example classes:

```text
0  1  2  3  4
5  6  7  8  9
```

### Sample Visualization

```markdown
![MNIST Samples](output-images/mnist-sample-distribution.png)
```

---

# 🔍 Data Exploration

The project examines the distribution of the training samples across the ten digit classes.

The recorded class counts are:

```text
Digit 0 : 5923 examples
Digit 1 : 6742 examples
Digit 2 : 5958 examples
Digit 3 : 6131 examples
Digit 4 : 5842 examples
Digit 5 : 5421 examples
Digit 6 : 5918 examples
Digit 7 : 6265 examples
Digit 8 : 5851 examples
Digit 9 : 5949 examples
```

This provides an initial understanding of the dataset before model training.

---

# ⚙️ Preprocessing

Before training, the image data is prepared for the neural network.

The preprocessing pipeline includes:

```text
Raw MNIST Images
       ↓
Pixel Processing
       ↓
Normalization
       ↓
Input Preparation
       ↓
MLP
```

The image pixels are converted into a suitable numerical representation for the neural network.

---

# 🧠 MLP Architecture

The project uses a **Multi-Layer Perceptron (MLP)** for digit classification.

The baseline architecture uses two hidden layers:

```text
Input Layer
     ↓
Dense Layer: 128 neurons
     ↓
Dense Layer: 64 neurons
     ↓
Output Layer: 10 classes
```

The output layer corresponds to the ten possible digit labels:

```text
0  1  2  3  4  5  6  7  8  9
```

---

# 🧪 Hyperparameter Experiments

Rather than relying on a single configuration, the project evaluates multiple training configurations.

The experiments vary:

### 1. Network Architecture

```text
Baseline       → (128, 64)
Arch_smaller   → (64)
Arch_wider     → (256, 128)
```

### 2. Batch Size

```text
32
64
128
```

### 3. Learning Rate

```text
0.001
0.01
0.0005
```

### 4. Number of Epochs

```text
5
10
15
20
```

This allows the effect of different hyperparameters to be studied systematically.

---

# 📊 Experiment Results

The experiment table recorded the following configurations:

| Experiment | Architecture | Batch | Learning Rate | Epochs | Training Accuracy | Validation Accuracy |
|---|---|---:|---:|---:|---:|---:|
| Baseline | (128, 64) | 32 | 0.001 | 15 | 0.995241 | 0.977000 |
| Arch_smaller | (64) | 32 | 0.001 | 15 | 0.996926 | 0.970333 |
| Arch_wider | (256, 128) | 32 | 0.001 | 15 | 0.995741 | 0.978500 |
| Batch_64 | (128, 64) | 64 | 0.001 | 15 | 0.996556 | 0.976000 |
| Batch_128 | (128, 64) | 128 | 0.001 | 15 | 0.996685 | 0.975667 |
| LR_high_0.01 | (128, 64) | 32 | 0.01 | 15 | 0.977537 | 0.960333 |
| LR_low_0.0005 | (128, 64) | 32 | 0.0005 | 15 | 0.997333 | 0.976667 |
| Epochs_5 | (128, 64) | 32 | 0.001 | 5 | 0.987667 | 0.970000 |
| Epochs_10 | (128, 64) | 32 | 0.001 | 10 | 0.994000 | 0.974667 |
| Epochs_20 | (128, 64) | 32 | 0.001 | 20 | 0.996759 | 0.975167 |

The corresponding experiment table and training-time comparison can be included in the repository.

```markdown
![Hyperparameter Experiments](output-images/hyperparameter-results.png)

![Training Time Comparison](output-images/training-time-comparison.png)
```

---

# 📈 Final Model Training

The final model training history shows the evolution of training and validation accuracy and loss across epochs.

```markdown
![Final Training Curves](output-images/final-training-curves.png)
```

The final training curves show that training accuracy continues to increase while the validation accuracy improves more gradually. The training and validation losses also show the difference between fitting the training data and generalization to unseen validation data.

---

# 🎯 Final Model Performance

The final model results recorded in the project are:

```text
Training Accuracy   : 99.49%
Validation Accuracy : 97.52%
Test Accuracy       : 97.58%
Test Loss           : 0.1311
MSE                 : 0.004116
```

The final model therefore demonstrates high classification accuracy on the MNIST test set.

---

# 🧩 Confusion Matrix

A confusion matrix is used to examine the classification behavior for each individual digit class.

```markdown
![Confusion Matrix](output-images/confusion-matrix.png)
```

The diagonal entries represent correctly classified samples, while off-diagonal entries show where one digit was classified as another.

This provides more detailed information than overall accuracy alone.

---

# ❌ Misclassification Analysis

The final model produced:

```text
242 misclassified images out of 10,000 test images
```

The project visualizes examples of these incorrect predictions.

```markdown
![Misclassified Images](output-images/misclassified-images.png)
```

These examples help identify visually similar handwritten digits that can be difficult for the classifier to distinguish.

---

# ✍️ Custom Handwritten Digit Prediction

The model is also tested using handwritten digit images beyond the standard result plots.

The prediction stage demonstrates how the trained classifier can be used on an input image and return a predicted digit.

```markdown
![Custom Digit Prediction](output-images/custom-digit-prediction.png)
```

This provides a simple demonstration of using the trained model for inference.

---

# 💾 Model Saving and Reloading

The trained model is saved in Keras format:

```text
mnist_mlp_final.keras
```

The saved model can subsequently be loaded and evaluated again.

This demonstrates a complete workflow:

```text
Train
  ↓
Save Model
  ↓
Reload Model
  ↓
Evaluate
  ↓
Predict
```

---

# 📊 Evaluation Metrics

The project evaluates the model using multiple measures:

### Accuracy

Measures the fraction of correctly classified samples.

```text
Accuracy = Correct Predictions / Total Predictions
```

### Loss

The training process tracks classification loss over the epochs.

### Mean Squared Error

The project also calculates MSE as an additional numerical evaluation measure.

### Confusion Matrix

Provides class-wise information about correct and incorrect predictions.

---

# 🛠️ Technologies Used

### Programming Language

- Python

### Machine Learning

- TensorFlow
- Keras

### Numerical and Data Processing

- NumPy
- Pandas

### Visualization

- Matplotlib
- Seaborn

### Evaluation

- Scikit-learn

### Development Environment

- Jupyter Notebook / Google Colab compatible workflow

---

# 📁 Project Structure

```text
MNIST-Handwritten-Digit-Recognition-MLP/
│
├── README.md
│
├── MNIST_MLP.ipynb
│
├── mnist_mlp_final.keras
│
└── output-images/
    ├── mnist-sample-distribution.png
    ├── hyperparameter-results.png
    ├── training-time-comparison.png
    ├── final-training-curves.png
    ├── confusion-matrix.png
    ├── misclassified-images.png
    └── custom-digit-prediction.png
```

---

# ▶️ How to Run

### 1. Clone the repository

```bash
git clone <YOUR-REPOSITORY-URL>
cd MNIST-Handwritten-Digit-Recognition-MLP
```

### 2. Install the required packages

```bash
pip install tensorflow numpy pandas matplotlib seaborn scikit-learn jupyter
```

### 3. Open the notebook

Open:

```text
MNIST_MLP.ipynb
```

using Jupyter Notebook or Google Colab.

### 4. Run the notebook sequentially

The notebook performs:

```text
Dataset Loading
      ↓
Exploration
      ↓
Preprocessing
      ↓
Baseline Training
      ↓
Hyperparameter Experiments
      ↓
Final Model Training
      ↓
Evaluation
      ↓
Error Analysis
      ↓
Prediction
```

---

# 🎓 Learning Outcomes

This project provides practical experience with:

- Machine-learning workflow design
- Neural-network fundamentals
- Multi-Layer Perceptrons
- Image classification
- Data preprocessing
- Hyperparameter tuning
- Training/validation analysis
- Model evaluation
- Confusion matrices
- Error analysis
- Model persistence
- Neural-network inference

---

# 🔬 Possible Future Improvements

Potential extensions include:

- Convolutional Neural Network (CNN) comparison
- Data augmentation
- Dropout and regularization experiments
- Early stopping
- Learning-rate scheduling
- Per-class precision and recall
- ROC-style class analysis
- Interactive digit-drawing interface
- Comparison with classical ML classifiers

---

# ⭐ Project Highlights

```text
🔢 MNIST Digit Classification
🧠 Multi-Layer Perceptron
⚙️ Hyperparameter Experiments
📈 Accuracy & Loss Analysis
⏱️ Training-Time Comparison
🧩 Confusion Matrix
❌ Misclassification Analysis
💾 Model Saving & Reloading
✍️ Handwritten Digit Prediction
🐍 Python
⚡ TensorFlow / Keras
```

---

## 👨‍💻 Author

**AmarDeep Dwivedi**

M.Tech  
Electrical Engineering — CSPML  
IIT Dharwad

---

## 📜 License

This project is intended for educational and research purposes.

---

<p align="center">
<b>🔢 From Pixels → Neural Network → Classification → Analysis</b>
</p>
