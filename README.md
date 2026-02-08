# 🕵️‍♂️ Deep Fake Detector using Deep Learning

This project implements a **Deep Fake video detection system** using **Deep Learning and Computer Vision**.  
It classifies videos as **real or fake** by extracting facial frames and analyzing them with a CNN-based model.

---

## 🚀 Project Overview

- Videos are split into frames
- Faces are detected using OpenCV
- A **MobileNetV2** CNN (transfer learning) is used for classification
- Frame-level predictions are aggregated into a **video-level result**
- Output includes both **label** and **confidence probability**

---

## 🧠 Technologies Used

- Python  
- TensorFlow / Keras  
- OpenCV  
- NumPy & Pandas  
- MobileNetV2 (Transfer Learning)  

---

## 📁 Project Structure

```
Deep Fake Detector using DL/
│
├── train/
│   ├── real/
│   └── fake/
│
├── test/
│
├── train_model_fast.py
├── predict_fast.py
├── dataset-metadata.json
├── gitignore.txt
└── README.md
```

---

## 📂 Dataset Notice

⚠️ **Important**

The **`train/`** and **`test/`** folders have **NOT been uploaded** to this repository because the dataset is **too large in size**.

Expected structure:
- `train/real/` → real videos  
- `train/fake/` → fake videos  
- `test/` → test videos  

Place the dataset locally following the above structure before running the code.

---

## 🏋️‍♂️ Training the Model

Run the following command:

```bash
python train_model_fast.py
```

This will:
- Extract frames from videos
- Train the deep learning model
- Save the trained model as:

```
deepfake_fast.h5
```

---

## 🔍 Running Predictions

After training, run:

```bash
python predict_fast.py
```

This will generate a `submission.csv` file containing:
- Predicted label (0 = Real, 1 = Fake)
- Prediction probability (confidence score)

---

## 📊 Output Format

`submission.csv`

| filename | label | probability |
|--------|------|-------------|
| video1.mp4 | 1 | 0.87 |
| video2.mp4 | 0 | 0.12 |

---

## 🧪 Model Highlights

- CNN-based Deep Learning model
- Transfer learning with MobileNetV2
- Face-focused frame extraction
- Efficient and lightweight inference
- Video-level prediction aggregation

---

## 📌 Notes

- Python 3.x required
- GPU recommended but not mandatory
- Designed for academic and learning purposes

---

## 👨‍🎓 Author
- Umang Nagaji Vekariya
- Harshit Sharma Thakur

