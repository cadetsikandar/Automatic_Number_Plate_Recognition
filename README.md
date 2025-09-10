# 🚗 Automatic Number Plate Recognition (ANPR)

This project implements a real-time **Automatic Number Plate Recognition system** using:
- YOLOv11 for number plate detection
- EasyOCR + Tesseract for text recognition
- SQLite for logging results

## 📂 Project Structure
```bash
Automatic_Number_Plate_Recognition/
├── data/                # sample video/images (tiny, or add .gitignore)
│   ├── plates/           # saved crops
│   └── anpr_logs.db      # sqlite db (optional, can be ignored in .gitignore)
├── models/
│   └── best.pt           # YOLO trained weights (or link in README)
├── src/
│   └── anpr.py           # your main code (single file or modularized later)
├── requirements.txt      # pip dependencies
├── demo                  # video
└── README.md             # project description

````


## ⚙️ Installation
```bash
git clone https://github.com/cadetsikandar/Automatic_Number_Plate_Recognition.git
cd Automatic_Number_Plate_Recognition
pip install -r requirements.txt
````

📊 Features

Real-time license plate detection

OCR with error correction

Saves plate crops

Stores recognized plates in SQLite

Exports output video with bounding boxes + FPS


🛠️ Training

The YOLOv11 model was trained on a custom number plate dataset (annotated using Roboflow
).
You can fine-tune your own model with:

yolo task=detect mode=train model=yolov11n.pt data=data.yaml epochs=100 imgsz=640

📜 License

This project is licensed under the MIT License – feel free to use it for research and personal projects.


---

## 🔹 Step 5: Commit & Push
```bash
git init
git add .
git commit -m "Initial commit: ANPR project"
git branch -M main
git remote add origin https://github.com/cadetsikandar/Automatic_Number_Plate_Recognition.git
git push -u origin main
