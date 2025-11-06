# FraudGuard - AI-Powered Banking Fraud Detection System

A comprehensive fraud detection system built for the Banking, Financial Services, and Insurance (BFSI) sector, featuring machine learning models, rule-based engines, and AI-powered explanations.

## 🚀 Features

### Core Functionality
- **Real-time Fraud Detection**: ML model + rule-based engine for accurate fraud prediction
- **Risk Scoring**: Advanced risk assessment with configurable thresholds
- **KYC Integration**: Document verification with AI-powered image analysis
- **Interactive Dashboard**: Real-time analytics and transaction monitoring
- **AI Assistant**: Natural language queries for fraud analytics using Google Gemini

### Advanced Capabilities
- **Explainable AI**: LLM-powered explanations for fraud predictions
- **Multi-channel Support**: Mobile, POS, ATM, and Web transaction analysis
- **Alert Management**: Automated fraud alerts with detailed reasoning
- **User Authentication**: Secure JWT-based authentication system
- **Responsive Design**: Modern React frontend with dark/light theme support

## 🏗️ Architecture

```
infosys_BFSI/
├── backend/                 # Flask API server
│   ├── src/
│   │   ├── app.py          # Main Flask application
│   │   ├── preprocessing/   # Data preprocessing modules
│   │   └── utils/          # Utility functions
│   ├── fraud_model_final/  # Trained ML models
│   ├── data/               # Training and test datasets
│   └── uploads/            # KYC document storage
├── frontend/               # React TypeScript application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Application pages
│   │   ├── context/        # React context providers
│   │   └── api.ts          # API integration
└── README.md              # This file
```

## 🛠️ Technology Stack

### Backend
- **Framework**: Flask (Python)
- **ML Libraries**: scikit-learn, pandas, numpy
- **Database**: SQLite
- **AI Integration**: Google Gemini API
- **Authentication**: JWT tokens
- **File Handling**: Werkzeug

### Frontend
- **Framework**: React 19 with TypeScript
- **Routing**: React Router DOM
- **Styling**: Tailwind CSS
- **Charts**: Recharts
- **Icons**: Lucide React, Heroicons
- **Build Tool**: Vite

## 📋 Prerequisites

- Python 3.8+
- Node.js 16+
- npm or yarn
- Google Gemini API key (optional, for AI features)

## 🚀 Quick Start

### 1. Clone the Repository
```bash
git clone <repository-url>
cd infosys_BFSI
```

### 2. Backend Setup
```bash
cd backend

# Install Python dependencies
pip install -r requirements.txt

# Set up environment variables (optional)
# Create .env file with:
# GOOGLE_API_KEY=your_gemini_api_key
# SECRET_KEY=your_secret_key

# Run the Flask server
python src/app.py
```

The backend will start on `http://localhost:5000`

### 3. Frontend Setup
```bash
cd frontend

# Install dependencies
npm install

# Start development server
npm run dev
```

The frontend will start on `http://localhost:5173`

## 📊 Usage

### 1. User Registration
- Navigate to `/signup` to create a new account
- Login with your credentials at `/login`

### 2. Transaction Analysis
- Go to "New Transaction" page
- Fill in transaction details (amount, channel, customer info)
- Upload KYC documents (optional)
- Submit for fraud analysis

### 3. View Results
- Check the dashboard for transaction history
- Review fraud alerts and risk scores
- Use the AI Assistant for natural language analytics queries

### 4. Analytics Dashboard
- Access "AI Assistant" for advanced analytics
- Ask questions like:
  - "Show me top fraud users this week"
  - "What's the fraud trend this month?"
  - "Analyze fraud by transaction channel"

## 🔧 Configuration

### Environment Variables
Create a `.env` file in the backend directory:

```env
GOOGLE_API_KEY=your_gemini_api_key_here
SECRET_KEY=your_jwt_secret_key
MODEL_WEIGHT=0.6
ALERT_RISK_THRESHOLD=0.45
USE_LLM=true
```

### Model Configuration
The system uses pre-trained models located in `backend/fraud_model_final/`:
- `model.pkl` - Main ML model
- `scaler.pkl` - Feature scaler
- `features.pkl` - Feature list
- `config.pkl` - Model configuration

## 🧪 API Endpoints

### Authentication
- `POST /api/auth/signup` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get user info

### Fraud Detection
- `POST /api/predict` - Analyze transaction for fraud
- `GET /api/transactions` - Get user transactions
- `POST /api/transactions/{id}/label` - Label transaction

### Analytics
- `GET /api/alerts` - Get fraud alerts
- `POST /api/admin/analytics/query` - AI-powered analytics queries

### AI Features
- `POST /api/llm_explanation` - Get AI explanation for prediction
- `POST /api/chatbot/check_image` - KYC document verification

## 🎯 Key Features Explained

### Fraud Detection Engine
The system combines:
1. **Machine Learning Model**: Trained on transaction patterns
2. **Rule-based Engine**: Business logic for known fraud indicators
3. **Risk Scoring**: Weighted combination of ML and rules
4. **Explainable AI**: Natural language explanations using Google Gemini

### Risk Factors Analyzed
- Transaction amount and patterns
- Account age and verification status
- Transaction timing (hours, weekends)
- Channel usage patterns
- KYC verification status
- Historical transaction behavior

## 🔒 Security Features

- JWT-based authentication
- Password hashing with Werkzeug
- Secure file upload handling
- SQL injection prevention
- CORS protection
- Input validation and sanitization

## 🚀 Deployment

### Production Build
```bash
# Frontend
cd frontend
npm run build

# Backend
cd backend
# Set environment variables
# Configure production database
# Deploy using your preferred method (Docker, AWS, etc.)
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Team

This project was developed as part of the Infosys BFSI initiative. See the [Team](frontend/src/pages/TeamPage.tsx) page for contributor information.

## 📞 Support

For support and questions:
- Check the [FAQ](frontend/src/pages/FAQPage.tsx) page
- Contact the development team
- Create an issue in the repository

## 🔮 Future Enhancements

- Real-time streaming fraud detection
- Advanced ML model ensemble
- Integration with external fraud databases
- Mobile application
- Advanced reporting and compliance features
- Multi-tenant architecture

---

**Note**: This system is designed for educational and demonstration purposes. For production use in financial institutions, additional security measures, compliance checks, and regulatory approvals may be required.