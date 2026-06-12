# DeepTrace AI

**AI-Powered Multi-Modal Deepfake Detection & Digital Media Forensics Platform**

[![Status](https://img.shields.io/badge/status-in%20development-yellow)]()
[![License](https://img.shields.io/badge/license-TBD-lightgrey)]()
[![Next.js](https://img.shields.io/badge/frontend-Next.js-black?logo=next.js)]()
[![FastAPI](https://img.shields.io/badge/backend-FastAPI-009688?logo=fastapi)]()
[![PyTorch](https://img.shields.io/badge/ML-PyTorch-EE4C2C?logo=pytorch)]()
[![PostgreSQL](https://img.shields.io/badge/database-PostgreSQL-4169E1?logo=postgresql)]()
[![Docker](https://img.shields.io/badge/devops-Docker-2496ED?logo=docker)]()

---

## Overview

DeepTrace AI is a production-grade digital media forensics platform designed to detect, classify, analyze, and explain manipulated or AI-generated content across images, videos, audio, and live webcam streams.

Unlike traditional deepfake detectors that provide only binary classification (Real / Fake), DeepTrace AI identifies specific manipulation categories, highlights suspicious regions, performs forensic analysis, and generates detailed reports.

---

## Key Features

- **Deepfake Image Detection** — Detect manipulated or AI-generated images
- **Deepfake Video Detection** — Analyze uploaded videos frame-by-frame
- **Voice Deepfake Detection** — Detect cloned and synthetic voices
- **Manipulation Classification** — Identify manipulation types:
  - Face Swap
  - Facial Reenactment
  - Lip-Sync Manipulation
  - Body Manipulation
  - AI-Generated Images
  - AI-Generated Videos
  - Synthetic Voices
- **Manipulation Localization** — Highlight suspicious regions using explainable AI heatmaps
- **Explainable AI** — Visualize model decisions using Grad-CAM
- **Metadata Forensics** — Analyze creation date, modification date, editing software, and metadata integrity
- **Deepfake Timeline Analysis** — Identify suspicious segments within videos
- **Manipulation Severity Score** — Estimate the extent of manipulation
- **PDF Forensic Reports** — Generate downloadable forensic investigation reports
- **Real-Time Webcam Verification** — Analyze live webcam streams for manipulation
- **Analysis History Dashboard** — Maintain historical forensic records

---

## Project Architecture

```
User Upload
    │
    ▼
Next.js Frontend
    │
    ▼
FastAPI Backend
    │
    ▼
AI Analysis Service
    │
    ├──────────────┬──────────────┐
    ▼              ▼              ▼
Image Pipeline  Video Pipeline  Audio Pipeline
(EfficientNet)  (X3D)           (Wav2Vec2)
    │              │              │
    └──────────────┴──────────────┘
                   ▼
        Explainability Engine (Grad-CAM)
                   ▼
            Forensics Engine
                   ▼
            Report Generation
                   ▼
       PostgreSQL + Object Storage
```

---

## Tech Stack

| Layer            | Technologies |
|------------------|--------------|
| **Frontend**     | Next.js, TypeScript, Tailwind CSS, ShadCN UI |
| **Backend**      | FastAPI, SQLAlchemy, Alembic, JWT Authentication |
| **Database**     | PostgreSQL |
| **AI / ML**      | PyTorch, OpenCV, Albumentations, Librosa, Torchaudio |
| **Explainability** | Grad-CAM |
| **DevOps**       | Docker, Docker Compose, GitHub Actions |

---

## Repository Structure

```
DeepTrace-AI/
├── apps/
│   ├── frontend/
│   ├── backend/
│   └── ml-service/
├── ml/
│   ├── datasets/
│   ├── training/
│   ├── inference/
│   ├── explainability/
│   ├── image/
│   ├── video/
│   ├── audio/
│   ├── data/
│   └── pipelines/
├── docs/
│   ├── architecture/
│   ├── deployment/
│   ├── api/
│   └── ml/
├── infrastructure/
│   ├── docker/
│   ├── nginx/
│   ├── deployment/
│   └── scripts/
├── tests/
└── .github/
    └── workflows/
```

---

## Development Status

| | |
|---|---|
| **Current Phase** | Architecture & Repository Setup |
| **Next Phase**    | System Design & Database Architecture |

---

## License

This project is currently under development. A license will be added before public release.
