📌 Overview
Intravenous (IV) cannulation is a fundamental yet often challenging medical procedure, especially for patients with poor vein visibility. This project proposes a deep learning-powered solution to detect subcutaneous forearm veins using Near-Infrared (NIR) imaging, segment the vascular structures, and intelligently recommend optimal injection sites.

We developed and evaluated two architectures:

🔬 Hybrid Attention Transformer U-Net (HATU-Net) for accurate binary segmentation using transformer-based attention.

🧠 Deep Feature Cascade U-Net (DFC-UNet) for multi-task learning, providing both vein segmentation and anatomical point regression for clinical site selection.

🎯 Features
✅ Advanced vein segmentation with U-Net-based models

📍 Anatomical injection site selection using AI-driven metrics (linearity, size, location)

📊 Multi-task learning (segmentation + anatomical regression)

🖼️ Real-time image processing using OpenCV and NIR image preprocessing

🌐 Flask web interface for clinical usability

🧪 Evaluation on diverse, annotated NIR dataset

🧪 Models
🔷 1. HATU-Net (Hybrid Attention Transformer U-Net)
Transformer encoder in bottleneck

Attention gates in decoder

Optimized for binary segmentation (vein vs background)

Dice Loss + AdamW optimizer

🔶 2. DFC-UNet (Deep Feature Cascade U-Net)
Multi-task: Segmentation + Regression of anatomical landmarks (ACF)

Supports 3-class segmentation (background, arm, vein)

Cascaded convolutional blocks for deeper feature learning

🔍 Methodology
📸 Preprocessing
CLAHE for local contrast enhancement

Gaussian & bilateral filtering

Laplacian sharpening for vein edge clarity

🧠 Training
Dice Loss / BCE Loss

Data augmentation (Albumentations, Torchvision)

Evaluation metrics: Dice Score, IoU, Accuracy, PSNR

📈 Results
Model	Dice Score	IoU	Accuracy	Regression Support
HATU-Net	~0.79	~0.73	High	❌
DFC-UNet	0.8015	0.7364	High	✅ Yes
SegNet / U-Net	Lower	Lower	High	❌

✅ DFC-UNet outperforms baselines in both segmentation and injection site prediction.

🖥️ Flask Web Application
Upload NIR image

See:
  Raw image
  Segmented vein mask
  Labeled injection sites
  Clinical scoring (linearity, size, depth)

🏥 Clinical Relevance
This tool aids:

Pediatric and geriatric patients

Darker skin tones or obese individuals

Emergency situations with time constraints

💡 Improves first-attempt success rate and reduces patient trauma

