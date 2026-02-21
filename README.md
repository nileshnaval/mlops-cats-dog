# 🐶🐱 MLOps Cats vs Dogs Classifier

End-to-end MLOps pipeline for image classification using PyTorch, MLflow, DVC, FastAPI, and Git.

---

## 🚀 Project Overview

This project implements a complete MLOps workflow:

- Dataset versioning using **DVC**
- Model training using **PyTorch**
- Experiment tracking using **MLflow**
- REST API deployment using **FastAPI**
- Version control using **Git**
- Container-ready structure (Docker)

The model classifies images as **Cat** or **Dog**.

---

## 📂 Project Structure
mlops-cats-dog/
│
├── app/ # FastAPI inference service
├── src/ # Training pipeline
├── data/ # Raw dataset (DVC tracked)
├── models/ # Saved model
├── mlruns/ # MLflow experiment logs
├── Dockerfile
├── requirements.txt
└── README.md


---

## 🧠 Model Details

- Custom CNN architecture
- Input size: 128x128
- Optimizer: Adam
- Loss: CrossEntropyLoss
- Epochs: 5
- Final Training Loss: ~0.25

---

## 📊 Experiment Tracking

MLflow is used to track:
- Training loss
- Model artifacts
- Run metadata

To launch MLflow UI:

```bash
mlflow ui --backend-store-uri ./mlruns


🔥 Run Training
python src/train.py


🌐 Run API
uvicorn app.main:app --reload

