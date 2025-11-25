# CoreBox U-Net Segmentation

This project implements **Core Column Segmentation** based on the paper  
**Baraboshkin et al., 2022 — “Core-Column Extraction Using Template-Like Augmentation”**.  
The goal is to extract core columns from core box images using **U-Net segmentation**.

This repository contains:

- `Run Model.ipynb` — Jupyter Notebook to train and test the U-Net model  
- `/dataset/images` — input core box images  
- `/dataset/jsons` — labelme polygon annotations  
- `/dataset/masks` — generated masks from JSON annotation  
- Training pipeline, augmentation, visualization, and post-processing code

---

## 🚀 Features

- U-Net segmentation with ResNet encoder  
- Albumentations for heavy augmentation  
- Labelme → Mask conversion  
- Visualization of predictions  
- Post-processing to extract core columns  
- CPU-compatible training (can run on normal laptops)

---

## 🧠 Workflow

1. **Prepare dataset**
   - Images in `dataset/images/`
   - Label polygons in `dataset/jsons/`
   - Convert JSON → mask using the notebook

2. **Train model**
   - Run `Run Model.ipynb`
   - Configure:
     - image size
     - batch size
     - augmentation
     - number of epochs

3. **Evaluate**
   - Visualize predicted masks
   - Compare prediction vs ground truth

4. **Post-processing**
   - Remove noise
   - Split merged cores
   - Extract bounding boxes of each core

---

## 📁 Folder Structure
corebox-unet/
│
├── Run Model.ipynb
├── dataset/
│ ├── images/
│ ├── jsons/
│ └── masks/
└── README.md

---

## 📦 Dependencies
torch
torchvision
segmentation-models-pytorch
albumentations
opencv-python
numpy
matplotlib
scikit-learn

