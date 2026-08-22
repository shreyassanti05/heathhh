# Quantum Pulse (Medical AI)

Quantum Pulse is a full-stack healthcare application designed to assist in medical imaging analysis and predictive healthcare diagnostics using AI models.

## Overview
The application integrates deep learning models for medical imaging (such as detecting issues in kidney or skin images, and cancer CNN models) with a modern web frontend. It provides an intuitive interface for medical professionals or users to interact with AI-driven diagnostics.

## Key Features
- **Medical Imaging Analysis:** Utilizes CNN models for cancer, skin, and kidney image classification.
- **Predictive Diagnostics:** Uses tabular models (e.g., diabetes prediction) for risk assessment.
- **Modern UI:** Built with React, TypeScript, and Vite for a seamless and responsive user experience.
- **API Backend:** Python backend to serve predictions from pre-trained Keras/TensorFlow models.

## How It Works
```text
User Input (Image/Data)
 ↓
React Frontend (UI/UX)
 ↓
Python API (FastAPI/Flask)
 ↓
Model Inference (CNNs, Scikit-learn)
 ↓
Prediction Result
 ↓
Displayed to User
```

## Technologies Used
- **Frontend:** React, TypeScript, Vite
- **Backend:** Python (API)
- **AI/ML:** Keras/TensorFlow (CNN models), Scikit-Learn
- **Deployment:** Vercel (Frontend/Serverless)

## Project Structure
```text
quantum-pulse-medical-ai/
│
├── api/
│   ├── models/            # Pre-trained models (e.g., cancer_cnn_model.h5)
│   ├── services/          # Inference and logic services
│   ├── index.py           # Backend entry point
│   ├── schemas.py         # API schemas
│   └── security.py        # Security handling
├── src/                   # React frontend source code
├── package.json           # Node dependencies
├── requirements.txt       # Python dependencies
└── vite.config.ts         # Vite configuration
```

## Installation

1. Install Frontend dependencies:
   ```bash
   npm install
   ```
2. Install Backend dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

Start the development server:
```bash
npm run dev
```

## Interview Talking Points
- **Why did you choose this architecture?** I separated the frontend (React/Vite) from the backend (Python API) to allow the Python server to natively handle heavy ML workloads (Keras/TensorFlow) while keeping the frontend fast, lightweight, and deployable on Vercel.
- **How do the CNN models work?** The Convolutional Neural Networks are trained on specific medical datasets (e.g., kidney, skin). The image is preprocessed (resized, normalized) before being passed to the model, which outputs a confidence score for classification.
- **What was the biggest technical challenge?** Bridging the frontend React application with the Python backend and ensuring that large image files are securely and efficiently transmitted for inference without blocking the UI.
