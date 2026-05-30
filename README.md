# AI Portfolio Advisory System

## Overview

The AI Portfolio Advisory System is a machine learning-powered investment recommendation platform that generates personalized portfolio allocations based on a user's risk tolerance, investment horizon, and financial goals.

The system combines portfolio optimization, market forecasting, sentiment analysis, and explainable AI techniques to provide data-driven investment recommendations.

The project is deployed as a cloud-hosted FastAPI application and can be accessed through a REST API interface.

---

## Features

### Risk Profiling

* Evaluates investor risk tolerance (Low, Medium, High)
* Considers investment horizon
* Generates a normalized risk score

### Market Forecasting

* ARIMA-based time series forecasting
* LSTM forecasting support (when TensorFlow is available)
* Expected return and volatility estimation

### Portfolio Optimization

* Modern Portfolio Theory (MPT)
* Sharpe Ratio Maximization
* Dynamic asset allocation recommendations

### Sentiment Analysis Layer

* Sentiment scoring framework
* News-driven return adjustments
* Easily extendable to FinBERT or other NLP models

### Explainable AI

* Human-readable portfolio recommendations
* Explains allocation decisions
* Interprets risk-adjusted performance metrics

### API Deployment

* FastAPI-powered backend
* Interactive Swagger documentation
* Cloud deployment on Render

---

## System Architecture

User Input
↓
Risk Profiler
↓
Market Forecaster (ARIMA / LSTM)
↓
Sentiment Analyzer
↓
Portfolio Optimizer (MPT)
↓
Explainability Engine
↓
Portfolio Recommendation API

---

## Technologies Used

### Backend

* Python
* FastAPI
* Uvicorn

### Machine Learning & Analytics

* NumPy
* Pandas
* Scikit-Learn
* Statsmodels
* SciPy

### Deployment

* GitHub
* Render

---

## Input Parameters

| Parameter          | Description                  |
| ------------------ | ---------------------------- |
| amount             | Investment amount            |
| investment_horizon | Investment duration in years |
| risk_tolerance     | low / medium / high          |
| goal               | growth / income / balanced   |

### Example Request

```json
{
  "amount": 100000,
  "investment_horizon": 5,
  "risk_tolerance": "medium",
  "goal": "growth"
}
```

---

## Example Response

```json
{
  "portfolio_metrics": {
    "expected_return": 0.095,
    "volatility": 0.023,
    "sharpe": 1.54,
    "risk_score": 0.37
  },
  "allocations": [
    {
      "asset": "MutualFunds",
      "percent": 47.4
    },
    {
      "asset": "Crypto",
      "percent": 47.4
    }
  ],
  "explanation": "Based on your medium risk tolerance and growth objective..."
}
```

---

## API Endpoints

### Health Check

GET /

Returns application status.

### Portfolio Analysis

POST /analyze

Generates personalized portfolio recommendations.

---

## Local Installation

Clone the repository:

```bash
git clone https://github.com/SNEHRANJAN28/ai-portfolio-advisor.git
cd ai-portfolio-advisor
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run locally:

```bash
uvicorn portfolio_advisory_fastapi:app --reload
```

Open:

```text
http://127.0.0.1:8000/docs
```

---

## Live Deployment

Render Deployment URL:

https://ai-portfolio-advisor-vab0.onrender.com

API Documentation:

https://ai-portfolio-advisor-vab0.onrender.com/docs

---

## Future Improvements

* Integration with Yahoo Finance real-time market data
* FinBERT sentiment analysis
* Pre-trained LSTM model serving
* Portfolio performance visualization
* Streamlit web interface
* User authentication
* Database integration
* Historical backtesting module

---

## Project Highlights

* End-to-end machine learning application
* Portfolio optimization using Modern Portfolio Theory
* Explainable AI recommendations
* Cloud deployment using FastAPI and Render
* REST API architecture
* Scalable modular design

---

## Author

Snehranjan

GitHub:
https://github.com/SNEHRANJAN28
