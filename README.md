# Brain Tumor Detection Using CNN, LSTM & CNN-LSTM Hybrid Models

This project focuses on detecting brain tumors using grayscale MRI images by implementing three deep learning architectures: **Convolutional Neural Networks (CNN)**, **Long Short-Term Memory (LSTM)**, and a **CNN-LSTM hybrid model**.

---

## 🧠 Project Objective

To develop a robust deep learning model capable of accurately classifying MRI images into **four tumor types**, helping in early diagnosis and reducing human error.

---

## 📁 Dataset Overview

- **Source**: [Mention the dataset source here, e.g., Kaggle or your university lab]
- **Type**: Grayscale MRI images
- **Classes**: 
  - Glioma Tumor
  - Meningioma Tumor
  - Pituitary Tumor
  - No Tumor
- **Image Format**: JPEG / PNG (Resized to 128x128)

---

## 🔄 Data Preprocessing

- **Grayscale conversion** (to reduce input complexity)
- **Image resizing** to 128x128
- **Normalization** (pixel scaling between 0 and 1)
- **Augmentation**:
  - Rotation
  - Flipping
  - Zooming
  - Shifting
- **One-hot encoding** for multiclass labels
- **Batching and prefetching** for optimized data loading

---

## 🧰 Model Architectures

### ✅ CNN Model
- 3 Convolutional layers with ReLU activation
- Batch Normalization and MaxPooling
- Fully Connected Dense layers
- Dropout layer to prevent overfitting
- Softmax output for classification

### ✅ LSTM Model
- Input reshaped to time-series format
- LSTM layers for sequence learning
- Fully connected dense layers and dropout

### ✅ CNN-LSTM Hybrid Model
- CNN layers extract spatial features
- Features reshaped and passed to LSTM
- Combines spatial + temporal understanding

---

## ⚙️ Training Configuration

- **Optimizer**: Adam (`learning_rate=0.0005`)
- **Loss Function**: Categorical Crossentropy
- **Metrics**: Accuracy
- **Epochs**: 50
- **Callbacks**: 
  - Learning rate scheduler
  - ReduceLROnPlateau for dynamic learning adjustment

---

## 📊 Results

| Model       | Test Accuracy |
|-------------|---------------|
| CNN         | ~93.7%        |
| LSTM        | ~83.1%        |
| CNN-LSTM    | ~84.9%        |

---

## 🧪 Future Improvements

- Experimenting with deeper architectures (ResNet, EfficientNet)
- Hyperparameter tuning
- Using colored images for more detailed features
- Deploying as a web application for medical use

---

## 📌 How to Run

```bash
# Clone the repo
git clone https://github.com/yourusername/brain-tumor-detection.git
cd brain-tumor-detection

# Install dependencies
pip install -r requirements.txt

# Run training
python Glioma Detection.py
