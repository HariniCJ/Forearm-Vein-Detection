# 🩺 AI-Based Forearm Vein Detection & Injection Site Selection

This project uses deep learning on Near-Infrared (NIR) images to detect forearm veins and recommend the best injection sites. It aims to assist in accurate and less invasive intravenous (IV) cannulation, especially in patients with difficult vein visibility.

## 📌 Project Highlights

- ✅ Forearm vein segmentation using deep learning
- 📍 Optimal injection site suggestion based on diameter, linearity & position
- 🧠 Models used: 
  - **Hybrid Attention Transformer U-Net (HATU-Net)**
  - **Deep Feature Cascade U-Net (DFC-UNet)**
- 🖼️ Preprocessing pipeline using OpenCV
- 🌐 Flask-based UI (optional deployment)

---

## 📁 Repository Structure
├── ENDSEM/ # Project assets or final submission files
├── models/hattenUnet/ # HATU-Net model architecture & weights
├── others work/ # Related references or external experiments
├── doubleConv.ipynb # DFC-UNet training notebook
├── hatunet.ipynb # HATU-Net training notebook
├── preprocessing.py # Image preprocessing (CLAHE, blur, filtering)
├── README.md # This file
├── .gitignore / .gitattributes # Git config files

## 🧠 Model Details

### 🔹 HATU-Net
- U-Net with attention gates and transformer encoder
- Binary segmentation (vein vs background)
- Suitable for precise vein structure detection

### 🔸 DFC-UNet
- Multi-task U-Net variant
- Performs both segmentation and ACF (injection point) prediction
- Higher clinical utility

---

## ⚙️ How to Run

### 1. Clone this repo

bash
git clone https://github.com/your-username/vein-detection-ai.git
cd vein-detection-ai

Run notebooks
hatunet.ipynb → Train/test HATU-Net

doubleConv.ipynb → Train/test DFC-UNet
