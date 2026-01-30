Pneumonia Detection Using Chest X-Ray Images

Detecting pneumonia from pediatric chest X-ray images using a Convolutional Neural Network (CNN).

---
This project applies **deep learning (CNNs)** to classify chest X-ray images as:
- **Pneumonia**
- **Normal**

---
Dataset
- **Name:** Chest X-Ray Images (Pneumonia)
- **Images:** 5,856 JPEG images
- **Age Group:** Pediatric patients (1–5 years)
- **Source:** Guangzhou Women and Children’s Medical Center, China
- **Provider:** Paul Mooney (Kaggle)

🔗 Dataset link:  
https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia

---
Data Preprocessing
The following preprocessing steps were applied:
- **Normalization:** Pixel values scaled to `[0, 1]`
- **Resizing:** Images resized to `224 × 224`
- **Data Augmentation:**
  - Rotation (±15°)
  - Width & height shift (±10%)
  - Shear transformation
  - Zoom (±10%)
  - Horizontal flip

These techniques help improve model generalization and reduce overfitting.
---
Model Architecture
- **Input:** 224 × 224 × 3
- **Architecture:** Convolutional Neural Network (CNN)
- **Key Features:**
  - Batch Normalization
  - Dropout for regularization
  - Global Average Pooling
- **Output:** Binary classification (Pneumonia / Normal)

---
Hyperparameters
- **Batch Size:** 32
- **Learning Rate:** 0.0001
- **Epochs:** 10
- **Optimizer:** Adam
- **Loss Function:** Binary Cross-Entropy
- **Early Stopping:** Enabled

---
Results
- Model trained and validated successfully
- Achieved strong performance on test data
- Per-class evaluation confirms reliable pneumonia detection

(Exact metrics and plots are available in the notebook.)
