# AI-Driven-Crowd-Detection-System
A real-time crowd counting system using **CSRNet (Congested Scene Recognition Network)**.  
This project estimates the number of people in video streams or pre-recorded footage by generating density maps and summing them.

---

## 📂 Project Structure

```
├── Crowd_detection_live.ipynb   # Jupyter notebook for live crowd detection
├── model.py                     # CSRNet model architecture
├── partBmodel_best.pth          # Pretrained weights (ShanghaiTech Part B)
├── videos & outputs/            # Sample videos and output storage
└── README.md                    # Project documentation
```

---

## ✨ Features

✅ **Patch-based Inference** – Handles high-resolution frames by splitting into 384×384 patches for improved accuracy.  
✅ **Pretrained CSRNet** – Based on VGG-16 frontend and dilated convolution backend.  
✅ **Live Headcount Overlay** – Displays real-time headcount on video frames.  
✅ **Video Input Support** – Works on both webcam streams and recorded videos.  

---

## 🧠 Model Architecture

CSRNet consists of:
1. **Frontend** – VGG-16 layers (pretrained on ImageNet).
2. **Backend** – Dilated convolutions for large receptive fields without losing resolution.
3. **Output Layer** – Generates a single-channel density map; summing it gives total headcount.

---

## ⚙️ Installation

### 1. Clone the repository
```bash
git clone https://github.com/your-username/CSRNet-Crowd-Detection.git
cd CSRNet-Crowd-Detection
```

### 2. Create and activate a virtual environment (recommended)
```bash
conda create -n csrnet_env python=3.9
conda activate csrnet_env
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

## 🚀 Usage

### 1. Running in Jupyter Notebook
Open `Crowd_detection_live.ipynb` and update:

```python
input_path = "path_to_your_video.mp4"
model_path = "partBmodel_best.pth"
```

Then run all cells.

### 2. Keyboard Controls
- **ESC** → Exit live video window.

---

## 📊 Output

The system overlays the predicted headcount on each frame in real-time:

```
Count: 125
```

Example:  

![Demo](link-to-your-sample-image-or-gif)

---

## 🗂 Dataset

- The model is pretrained on **ShanghaiTech Part B Dataset**.
- You can fine-tune it for your dataset by modifying the notebook.

---

## 🤝 Contributing

Pull requests and suggestions are welcome!
Contact - shrutimahanty25@gmail.com

---

## 📜 License

This project is licensed under the **MIT License**.





