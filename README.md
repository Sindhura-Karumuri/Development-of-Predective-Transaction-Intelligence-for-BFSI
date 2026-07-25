# Predictive Transaction Intelligence for BFSI

A full-stack web application that detects fraudulent financial transactions in real-time using machine learning, built for the Banking, Financial Services, and Insurance (BFSI) sector.

## Features

- 🔍 Real-time fraud detection using a trained ML model
- 📊 Admin analytics dashboard with transaction trends and EDA reports
- 🤖 KYC verification bot for identity document validation
- 🔐 User authentication with protected admin routes
- 📁 CSV upload support for batch transaction analysis
- 🌙 Dark/Light theme toggle

## Tech Stack

**Frontend**
- React 19 + TypeScript
- Vite
- Tailwind CSS
- Recharts (data visualization)
- Framer Motion (animations)
- React Router DOM

**Backend**
- Python + Flask
- scikit-learn / XGBoost (ML model)
- SQLite (transactions database)
- Pandas (data preprocessing)

## Getting Started

### Backend
```bash
cd backend
pip install -r requirements.txt
python src/app.py
```

### Frontend
```bash
cd frontend
npm install
npm run dev
```

Frontend runs on `http://localhost:5173`, backend on `http://localhost:5000`.

## Project Structure

```
├── backend/
│   ├── data/              # Raw and processed datasets
│   ├── fraud_model_final/ # Trained model files
│   └── src/
│       ├── preprocessing/ # Data cleaning and model training
│       └── app.py         # Flask API
└── frontend/
    └── src/
        ├── components/    # Reusable UI components
        ├── pages/         # Route-level pages
        └── context/       # Global state management
```

## Team

Built as a group internship project by a team of 9 members.
