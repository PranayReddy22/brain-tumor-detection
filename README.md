# 🧠 Brain Tumor Detection and Classification Using Deep Learning

This project applies deep learning techniques to classify brain MRI scans into four categories: **Glioma**, **Meningioma**, **Pituitary Tumor**, and **No Tumor**. Early and accurate detection is critical for improving patient outcomes, and this model contributes to the growing field of AI-driven medical diagnostics.

---

## 🎯 Objective

- Detect and classify brain tumors using MRI scans
- Evaluate the performance of multiple deep learning architectures
- Improve clinical decision-making through high-accuracy classification

---

## 🧪 Dataset

- Source: [Kaggle - Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri/data)
- 5712 training images and 1311 testing images
- Classes:
  - Glioma Tumor
  - Meningioma Tumor
  - Pituitary Tumor
  - No Tumor

Image preprocessing included:
- Resizing to 224x224 pixels
- Standardization and real-time augmentation using `ImageDataGenerator`
- 20% of training data used for validation

---

## 🧠 Methodology

- **Transfer Learning** applied on pre-trained models:
  - **EfficientNetB3**: Best performing
  - **MobileNetV2**: Fastest, lightest
  - **VGG16**: Strong performance, slow training
  - **ResNet50**: Deeper network with residual connections

Enhancements used:
- Early Stopping
- Batch Normalization
- Dropout Regularization
- Global Average Pooling
- Additional Conv2D layers for deeper feature extraction in some variants

---

## 📈 Results

| Model                          | Test Accuracy |
|--------------------------------|----------------|
| EfficientNetB3                 | **96.64%**     |
| MobileNetV2                    | 92.57%         |
| VGG16                          | 95.48%         |
| ResNet50                       | 94.12%         |
| VGG16 + Extra Conv Layer       | 96.89%         |
| ResNet50 + Extra Conv Layer    | 96.08%         |

- EfficientNetB3 achieved the highest accuracy with balanced speed
- MobileNetV2 was the fastest but slightly less accurate
- Adding a convolutional layer improved both VGG and ResNet performance by ~2%

---

## 🩺 Clinical Relevance

Accurate classification of brain tumors via MRI imaging is essential for early intervention and treatment planning. The results from this project indicate that deep learning—especially transfer learning with modern architectures—can assist radiologists by providing a second opinion or preliminary classification tool.

---

## 📌 Technologies Used

- Python, TensorFlow, Keras
- EfficientNet, ResNet, VGG, MobileNet
- NumPy, Matplotlib
- ImageDataGenerator for augmentation

---

## 📄 Reports

- [📊 Project Presentation](Brain_tumor_detection_PranayReddy.pptx)

---

## 📃 License

This project is licensed under the [MIT License](LICENSE).
