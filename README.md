# Player Re-Identification in Sports Footage 

## 👋 Overview

This project solves the task of player re-identification using YOLOv8 and DeepSORT.
It detects players, ball, goalkeeper and tracks them with consistent IDs across frames.

## 📂 Project Structure
- `yolo_deepsort_track.py`: Final script with YOLOv8 + DeepSORT tracking
- `runs/detect/train2/best.pt`: Final trained model
- `data/`: Dataset config
- `report.md`: Approach, results, and challenges
- `resume.pdf`: My resume for internship consideration

## 🧠 Approach
- Annotated frames using Roboflow (76frames,5frame per second)
- Trained a YOLOv8n model for 20 epochs
- Used DeepSORT for identity tracking

## ✅ How to Run

```bash
pip install -r requirements.txt
python yolo_deepsort_track.py

⚙️ System

    Intel i5 12th Gen, 8GB RAM, Iris Xe Graphics

    All run on CPU only

🙋‍♂️ Contact

Biswajit Nahak – biswajitnahak2003@gmail.com


---

