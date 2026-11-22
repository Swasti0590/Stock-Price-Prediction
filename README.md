# 📈 AI Stock Price Prediction System

An AI-powered stock analysis and prediction system that combines historical stock market data, LSTM-based machine learning, and sentiment analysis to provide stock insights and price predictions.

## 🚀 Overview

The **AI Stock Price Prediction System** is a full-stack web application designed to analyze stock market data and predict future stock prices using machine learning.

The application integrates a React frontend, Node.js backend, and Python-based machine learning service to create an end-to-end stock analysis platform.

Users can enter a stock symbol to analyze its historical price data, generate predictions, analyze market sentiment, and view stock insights through an interactive dashboard.

## ✨ Features

- 📊 Historical stock price visualization
- 🤖 Stock price prediction using LSTM
- 📈 Real-time stock data fetching using Yahoo Finance
- 📰 News-based sentiment analysis
- 💡 Buy / Sell / Hold recommendation system
- 📉 Interactive stock charts
- 💾 MongoDB integration for storing predictions
- 🔗 Full-stack architecture
- ⚠️ Error handling and input validation

## 🛠️ Tech Stack

### Frontend
- React.js
- Vite
- Tailwind CSS
- Recharts

### Backend
- Node.js
- Express.js
- Axios

### Machine Learning
- Python
- Flask
- TensorFlow / Keras
- LSTM Neural Network
- Scikit-learn
- NumPy
- Pandas
- yfinance

### Sentiment Analysis
- VADER Sentiment
- News API

### Database
- MongoDB
- Mongoose

## 🏗️ System Architecture

```text
React Frontend
      │
      ▼
Node.js / Express Backend
      │
      ▼
Python Flask ML Service
      │
      ├── Stock Data (Yahoo Finance)
      ├── LSTM Price Prediction
      ├── News Sentiment Analysis
      │
      ▼
MongoDB Database
```

## ⚙️ How It Works

1. User enters a stock ticker such as `AAPL`, `TSLA`, or `MSFT`.
2. The React frontend sends a request to the Node.js backend.
3. The backend communicates with the Flask ML service.
4. The ML service retrieves historical stock data.
5. The LSTM model analyzes historical prices and generates a prediction.
6. News sentiment analysis evaluates available news headlines.
7. Prediction information is stored in MongoDB.
8. The frontend displays stock data, charts, predictions, and sentiment results.

## 📁 Project Structure

```text
Stock-Price-Prediction/
│
├── backend/
│   ├── server.js
│   ├── models/
│   ├── routes/
│   └── package.json
│
├── frontend/
│   ├── src/
│   ├── public/
│   └── package.json
│
├── ml-service/
│   ├── app.py
│   ├── train.py
│   ├── requirements.txt
│   ├── scaler.pkl
│   └── lstm_model.h5
│
└── README.md
```

## 💻 Installation & Setup

### Prerequisites

Make sure the following are installed:

- Node.js
- Python 3.x
- MongoDB
- Git
- npm
- pip

### 1️⃣ Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Navigate to the project:

```bash
cd Stock-Price-Prediction
```

### 2️⃣ Setup Backend

```bash
cd backend
npm install
```

Create a `.env` file inside the backend folder:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
```

Start the backend:

```bash
node server.js
```

### 3️⃣ Setup Machine Learning Service

Open a new terminal:

```bash
cd ml-service
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate the virtual environment on Windows:

```bash
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Create a `.env` file if required:

```env
NEWS_API_KEY=your_news_api_key
```

Start the ML service:

```bash
python app.py
```

### 4️⃣ Setup Frontend

Open another terminal:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Open the local URL provided by Vite in your browser.

## 🔌 API Endpoints

### Backend APIs

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/stock-data` | Fetch historical stock data |
| POST | `/api/predict` | Generate stock price prediction |
| POST | `/api/sentiment` | Analyze stock news sentiment |
| POST | `/api/save` | Save prediction to database |

### Machine Learning APIs

| Method | Endpoint | Description |
|---|---|---|
| POST | `/stock-data` | Fetch stock market data |
| POST | `/predict` | Generate prediction |
| POST | `/sentiment` | Perform sentiment analysis |

## 🧠 Machine Learning Model

The project uses an **LSTM (Long Short-Term Memory)** neural network for time-series stock price prediction.

### Model Details

- **Model Type:** LSTM Neural Network
- **Input:** Historical closing prices
- **Time Step:** 60 days
- **Output:** Predicted stock price
- **Preprocessing:** MinMaxScaler
- **Framework:** TensorFlow / Keras

The model processes sequential stock price data to identify patterns and generate predictions.

## 📰 Sentiment Analysis

The sentiment analysis component evaluates news headlines related to a stock.

It uses:

- News API for news data
- VADER Sentiment Analyzer
- Compound sentiment score

Sentiment is categorized into:

- 🟢 Positive
- 🔴 Negative
- 🟡 Neutral

## 📊 Database

MongoDB is used to store stock prediction records.

### Prediction Schema

```javascript
{
    stock: String,
    price: Number,
    sentiment: String,
    date: Date
}
```

## ⚠️ Limitations

- Predictions are based primarily on historical stock price patterns.
- Market volatility and external economic factors may affect accuracy.
- News APIs may have rate limits.
- Machine learning predictions are not guaranteed to be accurate.
- This project is intended for educational and research purposes only.

## 🔮 Future Improvements

- Real-time stock updates
- WebSocket integration
- Advanced prediction models
- Portfolio tracking
- User authentication
- Multi-stock comparison
- Improved sentiment analysis
- Cloud deployment

## 👩‍💻 Author

**Swasti Singh**

B.Tech – Computer Science Engineering (AI & ML)

## 📄 Disclaimer

This project is developed for educational and demonstration purposes.

Stock price predictions are experimental and should not be considered financial advice or used as the sole basis for investment decisions.
