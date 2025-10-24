# 🏥 APAM - Smart Medicine Adherence Assistant

**AI-Powered Medication Management System with Pill Recognition, Intelligent Reminders & Medical Chatbot**

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.9+-blue.svg)
![React](https://img.shields.io/badge/react-18+-61dafb.svg)
![FastAPI](https://img.shields.io/badge/fastapi-0.100+-009688.svg)

---

## 🌟 Features

### 🤖 AI & Machine Learning
- **Pill Recognition**: YOLOv8-based image classification for automatic pill identification
- **Medical Chatbot**: Google Gemini LLM for intelligent medical guidance
- **Smart Insights**: AI-powered adherence analytics and personalized recommendations

### 💊 Medication Management
- Complete CRUD for medications (name, dosage, schedule, stock)
- Smart reminders with multiple notification channels
- Low stock alerts and refill notifications
- Medication history tracking

### 📊 Analytics & Gamification
- Real-time adherence statistics (daily, weekly, monthly)
- Interactive charts (adherence trends, time distribution)
- Achievement system with badges and streaks
- Personalized AI insights

### 🔐 Security & MLOps
- JWT Authentication with OAuth2
- Password hashing (bcrypt)
- Docker containerization
- Prometheus monitoring (`/metrics`)
- CI/CD with GitHub Actions

---

## 🏗️ Tech Stack

| Layer | Technologies |
|-------|-------------|
| **Frontend** | React 18, Tailwind CSS, Recharts, Lucide Icons |
| **Backend** | FastAPI, Python 3.9+, Asyncio |
| **ML/DL** | YOLOv8 (Ultralytics), PyTorch |
| **LLM** | Google Gemini API |
| **Database** | PostgreSQL 15 |
| **MLOps** | Docker, Prometheus, GitHub Actions |
| **Auth** | JWT, OAuth2, Passlib |

---

## 🚀 Quick Start

### Prerequisites
- Docker & Docker Compose
- Python 3.9+
- Node.js 18+

### 1️⃣ Clone Repository
```bash
git clone https://github.com/your-username/APAM-Smart-Medicine-Assistant.git
cd APAM-Smart-Medicine-Assistant
```

### 2️⃣ Environment Setup
```bash
# Copy environment file
cp .env.example .env

# Add your API keys
GEMINI_API_KEY=your_google_gemini_key
SECRET_KEY=your_jwt_secret_key
DATABASE_URL=postgresql://user:password@localhost/apam
```

### 3️⃣ Run with Docker
```bash
# Build and start all services
docker-compose up --build

# Access the application
Frontend: http://localhost:3000
Backend API: http://localhost:8000
API Docs: http://localhost:8000/docs
Metrics: http://localhost:8000/metrics
```

### 4️⃣ Manual Setup (Development)
```bash
# Backend
cd backend
pip install -r requirements.txt
uvicorn main:app --reload

# Frontend
cd frontend
npm install
npm start

# Train ML Model (optional)
python train.py
```

---

## 📂 Project Structure
```
APAM-Smart-Medicine-Assistant/
├── backend/
│   ├── main.py              # FastAPI app
│   ├── models/              # ML models (YOLOv8)
│   ├── routers/             # API endpoints
│   ├── database/            # PostgreSQL schemas
│   ├── services/            # Business logic (LLM, ML)
│   └── train.py             # Model training script
├── frontend/
│   ├── src/
│   │   ├── components/      # React components
│   │   ├── pages/           # App pages
│   │   └── services/        # API calls
│   └── public/
├── docker-compose.yml       # Multi-container setup
├── .github/workflows/       # CI/CD pipelines
└── README.md
```

---

## 🎯 API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/health` | GET | Health check |
| `/auth/register` | POST | User registration |
| `/auth/login` | POST | User login (JWT) |
| `/medications` | GET/POST | CRUD medications |
| `/medications/{id}` | PUT/DELETE | Update/Delete med |
| `/predict` | POST | Pill image recognition |
| `/chat` | POST | Medical chatbot (LLM) |
| `/history` | GET | Adherence history |
| `/metrics` | GET | Prometheus metrics |

---

## 🧪 Testing
```bash
# Run backend tests
cd backend
pytest tests/ -v

# Run with coverage
pytest --cov=. --cov-report=html
```

---

## 📊 ML Model Performance

| Metric | Value |
|--------|-------|
| **Accuracy** | 94.5% |
| **Precision** | 93.2% |
| **Recall** | 95.1% |
| **F1-Score** | 94.1% |

*Trained on 1,200+ pill images across 15 medication classes*

---

## 🎓 Projet Fil Rouge - Simplon Compliance

✅ **Organization & Modeling**: GitHub Projects, clear phases  
✅ **Requirements Analysis**: Medical adherence use case  
✅ **Data Sources**: Local pill images + Gemini API  
✅ **AI Development**: YOLOv8 (DL) + LLM chatbot  
✅ **External Services**: Google Gemini integration  
✅ **Data Pipelines**: Async background tasks  
✅ **Deployment & MLOps**: Docker + Prometheus + CI/CD  
✅ **API Development**: FastAPI with JWT auth  
✅ **UI & Visualization**: React dashboard + charts  
✅ **Testing & Quality**: Pytest coverage  
✅ **Security & Compliance**: JWT, password hashing, GDPR-ready  

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Ahmed Bennani**  
🎓 Simplon AI Bootcamp 2025  
📧 ilhamelgharbi3@gmail.com  
🔗 [LinkedIn](#) | [Portfolio](#)

---

## 🙏 Acknowledgments

- **Simplon** for the AI formation
- **Google Gemini** for LLM API
- **Ultralytics** for YOLOv8
- **FastAPI** community

---

⭐ **Star this repo if you find it helpful!**
