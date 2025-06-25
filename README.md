# Celeb Heights – Estimating Human Height from Images Using CNN and Mask R-CNN

This repository was created as part of a dissertation project and focuses on estimating human height from images using a two-part deep learning approach:

1. **Height Classification using CNN**  
   A custom Convolutional Neural Network (CNN) is trained to classify individuals into discrete height categories based on labeled celebrity images.

2. **Human Segmentation using Mask R-CNN**  
   A pre-trained Mask R-CNN model is used to segment humans in images, allowing for future development of pixel-based height estimation.

---

## 📁 Repository Structure

- `CelebHeights.ipynb`  
  Custom CNN training and evaluation notebook:
  - Dataset loading and preprocessing
  - Data augmentation and normalization
  - CNN architecture for height classification
  - Model training and validation visualization
  - Predictions on unseen test images

- `maskrcnn.ipynb`  
  Notebook for running Mask R-CNN:
  - Setup and dependency installation
  - Pre-trained Mask R-CNN model loading
  - Inference and mask visualization
  - Saving segmented outputs

---

## 🧠 Key Techniques

- **TensorFlow / Keras**: CNN implementation and training
- **Mask R-CNN**: Person segmentation for pixel-level analysis
- **Data Augmentation**: Applied to reduce overfitting
- **Softmax Predictions**: Used for height class confidence scores

---

## 📊 Dataset

- **Training Data**: A directory of celebrity images organized into subdirectories by height class (e.g., `170`, `180`, `190`, etc.).
- **Test Data**: Additional unseen images used to evaluate model generalization.
- **Segmentation Input**: Archive of celebrity images for use with Mask R-CNN.

---

## 📈 Model Overview

### CNN Architecture

- Image size: 512x509 pixels
- Convolutional layers with increasing filters (16 → 128)
- MaxPooling and Dropout for regularization
- Dense layers for classification
- Final output layer with size equal to number of height classes

### Example Output

```bash
The person is 97.45 percent 180 cm
