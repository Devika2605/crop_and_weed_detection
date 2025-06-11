# 🌱 Crop and Weed Detection using YOLOv5

An AI-powered object detection project to identify crops and weeds using custom YOLOv5 training — with the goal of precision spraying only on weeds, reducing pesticide use and crop contamination.

---

## 🚀 Project Overview

🌾 **Problem Statement:**  
Weeds compete with crops for nutrients, water, and sunlight — reducing yield. Farmers often spray pesticides indiscriminately, harming both weeds and crops.

🎯 **Objective:**  
Build a YOLOv5-based system that detects **crops** and **weeds**, and simulates pesticide spraying **only on weeds** — increasing efficiency and safety.

---

## 🧠 Tech Stack

- YOLOv5 (Object Detection)
- Google Colab (Training & Visualization)
- Python (OpenCV, Matplotlib, Pandas)
- Keras (for Data Augmentation)
- Manual Annotation (YOLO format)

---

## 📂 Dataset

- 📸 ~1300 labeled images (original + augmented)
- 🏷️ YOLO-format bounding box annotations
- 🌾 Class `0` = Crop
- 🌿 Class `1` = Weed

> Dataset was collected manually and augmented using Keras' `ImageDataGenerator`.

---

## 🛠️ Pipeline

1. **Image Collection & Cleaning**
2. **Image Resizing (4000×3000 ➝ 512×512)**
3. **Data Augmentation (to expand dataset)**
4. **Manual Labeling (YOLO format)**
5. **Model Training with YOLOv5**
6. **Inference and Spray Simulation**
7. **Visualization & Reporting**

---

## 📊 Features & Visualizations

✅ Bounding boxes for crop (green) and weed (red)  
✅ Spray simulation on weeds (blue dot)  
✅ Batch summary table (crop vs weed counts)  
✅ Pie and bar charts of class distribution  
✅ GIF animation of predictions  
✅ Confidence score display for YOLO predictions

---

## 📈 Results

- Model trained with `yolov5s.pt` (lightweight, fast)
- Inference works on custom field images
- Visual confidence included on predictions

---

## 🎥 Demo Previews

| Original Image | Prediction with Spray |
|----------------|------------------------|
| ![orig](![agri_0_3008](https://github.com/user-attachments/assets/9651013f-41ee-493c-bb93-fe9fa9a27d78)
) | ![pred](![image](https://github.com/user-attachments/assets/a29c7fa0-4de9-4be9-8f86-7cb71f670871)
) |

---
**Detection folder- it is consisting of nearly 150 images of sample output only that much is uploded because of the huge data of output**

## 📁 Folder Structure


├── yolov5/ # YOLOv5 repo

│ ├── dataset/ # Custom dataset

│ │ ├── images/

│ │ └── labels/

│ ├── runs/detect/exp/ # YOLO predictions

├── spray_animation.gif # Spray demo

├── summary_crop_weed.csv # Class counts per image

├── crop_weed.yaml # Dataset config

└── crop_weed_detect.ipynb # Colab notebook
