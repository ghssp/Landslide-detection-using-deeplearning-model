# Hybrid model for Landslide Detection 🌍🧠

## 📌 Project Overview

Landslides are among the most devastating natural disasters, resulting in significant human and economic loss. Early detection is critical for mitigation and rescue efforts. This project introduces an **landslide detection system** using a two-stage deep learning approach: segmentation and classification.

The system combines powerful **deep learning models**  to perform real-time landslide prediction directly in the field, even in remote areas with limited resources.we can integrate this on a raspberry pie hardware kit and can do classification of this dataset as well

---

## 🧠 Core Components

### 1. Segmentation - Hybrid Model
- **Architecture:** `EfficientNetB0 + ResUNet`
- **Purpose:** Accurately identifies and segments landslide-prone areas in satellite images.
- **Performance:**
  - Mean IoU: `84.06%`
  - Accuracy: `99.05%`
- **Process:**
  - Input images are resized to `256x256`
  - Feature extraction using EfficientNetB0
  - Segmentation using ResUNet decoder with skip connections

### 2. Classification - Binary Image Classification
- **Platform:** Raspberry Pi 3 Model B
- **Tool:** TensorFlow Lite + Flask Web Application
- **Purpose:** Classifies segmented masks into `landslide` or `non-landslide` in real-time
- **Advantages:** Lightweight, portable, and efficient for edge deployment

---

## 🧪 Performance Highlights

| Metric              | Value     |
|---------------------|-----------|
| Mean IoU (Segmentation) | 84.06% |
| Classification Accuracy | 99.05% |
| Improved Segmentation | +2.4% over existing models |
| Model Size           | Lightweight (~20MB) |

## Dataset Information
### 🧪 Dataset Preprocessing:
- Image resizing to `256x256`
- Pixel value normalization to [0, 1]
- Augmentation: rotation, brightness variation, flipping
- Label masks generated for binary segmentation (landslide vs. background)

### 🔁 Data Split:
- **Training Set**: 70%
- **Validation Set**: 15%
- **Test Set**: 15%

### 🛑 Class Balance:
- Balanced dataset with equal representation of:
  - Landslide images
  - Non-landslide images
#### 📂 Source:
- **Kaggle**:We can download datasets from this webiste,download the dataset which is balanced in both cases and diversed 
---

