# AI Examination System

> An Intelligent Examination Platform powered by **OCR, NLP, Speech Recognition, Computer Vision, and Behavioral Analytics** for automated assessment and cheating detection.

# 📖 Overview

The **AI Examination System** is a comprehensive intelligent examination platform designed to automate the evaluation of:

* Handwritten Exams
* Typing-Based Exams
* Online Video-Based Exams

The system combines multiple AI technologies including:

* **OCR (EasyOCR)** for handwritten answer extraction
* **NLP (Sentence Transformers)** for semantic answer evaluation
* **Whisper Speech-to-Text** for oral exam transcription
* **Computer Vision (MediaPipe/OpenCV)** for video proctoring
* **AI Content Detection** for identifying AI-generated answers
* **Behavioral Analytics** for detecting cheating patterns

---

# Features

## 1. Handwritten Exam Evaluation

### Capabilities

* Upload scanned handwritten answer sheets
* Automatic text extraction using OCR
* Image preprocessing for improved recognition
* Semantic answer scoring
* Automatic student information extraction
* Spelling-aware grading system

### Pipeline

```text
Handwritten Image
        ↓
Image Preprocessing
        ↓
EasyOCR Text Extraction
        ↓
Question Parsing
        ↓
Semantic Similarity Scoring
        ↓
Marks Assignment
        ↓
Result Generation
```

### Technologies

* EasyOCR
* OpenCV
* Pillow
* Sentence Transformers

---

## 2. Typing Test Monitoring

### Capabilities

* Real-time answer monitoring
* Copy-paste detection
* AI-generated text detection
* Automatic answer evaluation
* Integrity report generation

### Cheating Detection

The system tracks:

* Sudden large text insertions
* Copy-paste behavior
* AI-generated responses
* Typing patterns

### Example

```text
Student Types Answer
          ↓
Keystroke Monitoring
          ↓
Paste Detection
          ↓
AI Content Detection
          ↓
Answer Scoring
          ↓
Integrity Report
```

---

## 3. Online Meeting Examination

### Capabilities

* Upload recorded exam videos
* Speech transcription
* Video proctoring
* Face tracking
* Head pose estimation
* Gaze tracking
* Audio anomaly detection

### Video Analysis

Detects:

* Multiple faces
* Student absence
* Looking away from screen
* Excessive head movement
* Drowsiness
* Yawning
* Suspicious behavior

### Audio Analysis

Detects:

* Multiple speakers
* Background conversations
* Audio spikes
* Suspicious noise patterns

---

## 4. Teacher Dashboard

### Features

* Student result management
* Performance analytics
* Cheating reports
* Export results
* Examination statistics
* Test history

### Dashboard Metrics

* Total Students
* Tests Submitted
* Cheating Cases
* Individual Scores
* Integrity Reports

---

# System Architecture

```text
                    AI Examination System

 ┌────────────────────────────────────────────────────┐
 │                    Streamlit UI                    │
 └────────────────────────────────────────────────────┘
                           │
      ┌────────────────────┼────────────────────┐
      │                    │                    │
      ▼                    ▼                    ▼

Handwritten Test      Typing Test      Online Meeting Test

      │                    │                    │
      ▼                    ▼                    ▼

 OCR Module       Paste Detection     Video Proctoring
 NLP Scoring      AI Detection        Audio Analysis
 Answer Parsing   Score Generation    Speech Recognition

      └────────────────────┼────────────────────┘
                           ▼

                  Teacher Dashboard
                           │
                           ▼

                    Results Database
```

---

# AI Models Used

| Model                        | Purpose                      |
| ---------------------------- | ---------------------------- |
| all-MiniLM-L6-v2             | Semantic Similarity Scoring  |
| EasyOCR                      | Handwritten Text Recognition |
| Whisper Base                 | Speech-to-Text               |
| roberta-base-openai-detector | AI Text Detection            |
| MediaPipe FaceMesh           | Face & Gaze Tracking         |
| OpenCV                       | Computer Vision Processing   |

---

# Project Structure

```text
AI-Examination-System/
│
├── app.py
├── requirements.txt
├── README.md
│
├── models/
│
├── uploads/
│
├── reports/
│
├── screenshots/
│
└── notebooks/
    └── IPCV_Project_Final.ipynb
```

---

# Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/AI-Examination-System.git

cd AI-Examination-System
```

---

## Create Virtual Environment

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### Linux/Mac

```bash
source venv/bin/activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Required Packages

```txt
streamlit
torch
opencv-python
numpy
Pillow
easyocr
sentence-transformers
transformers
openai-whisper
mediapipe
moviepy
librosa
pyspellchecker
```

---

# Run Application

```bash
streamlit run app.py
```

Open:

```text
http://localhost:8501
```

---

# Examination Workflow

## Step 1: Load AI Models

Navigate to:

```text
Setup Models
```

Load:

* Sentence Transformer
* EasyOCR
* Whisper
* AI Detector

---

## Step 2: Create Exam

Navigate to:

```text
Manage Exam
```

Add:

* Questions
* Model Answers
* Marks Distribution

---

## Step 3: Conduct Exam

Choose:

* Handwritten Test
* Typing Test
* Online Meeting Test

---

## Step 4: Analyze Results

View:

* Scores
* Similarity Metrics
* Cheating Reports
* Student Performance

---

# Scoring Methodology

## Semantic Similarity Scoring

```python
Cosine Similarity(
    Student_Embedding,
    Model_Answer_Embedding
)
```

### Score Rules

| Similarity  | Result                   |
| ----------- | ------------------------ |
| ≥ 0.50      | Full Marks               |
| 0.30 – 0.49 | Partial Marks            |
| < 0.30      | Keyword-Based Evaluation |

---

## Enhanced Spelling-Aware Scoring

```text
Final Score =
70% Semantic Similarity
+
30% Spelling Quality
```

---

# Cheating Detection Mechanisms

## Typing Test

✔ Copy-Paste Detection

✔ AI-Generated Text Detection

✔ Behavioral Monitoring

---

## Online Exam

✔ Multiple Face Detection

✔ No Face Detection

✔ Gaze Tracking

✔ Head Pose Estimation

✔ Drowsiness Detection

✔ Yawning Detection

✔ Multiple Speaker Detection

✔ Audio Spike Detection

---

# Future Improvements

* Real-Time Webcam Proctoring
* Live Examination Sessions
* Face Recognition Authentication
* Object Detection (Phone Detection)
* LLM-Based Answer Evaluation
* Multi-Language OCR Support
* Cloud Deployment
* Analytics Dashboard with Charts
* LMS Integration
* Automated Question Generation

---

# Learning Outcomes

This project demonstrates practical implementation of:

* Natural Language Processing (NLP)
* Optical Character Recognition (OCR)
* Computer Vision
* Speech Recognition
* Behavioral Analytics
* AI-Based Proctoring
* Semantic Similarity Scoring
* Streamlit Web Development
* Deep Learning Model Integration

---

# Authors

**Muhammad Ahsan**

AI Engineer | Machine Learning Engineer | Computer Vision Enthusiast

### Skills

* Artificial Intelligence
* Machine Learning
* Deep Learning
* Computer Vision
* NLP
* Generative AI
* MLOps
* Python Development

---

