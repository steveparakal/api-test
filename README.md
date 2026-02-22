# ⚡ ML Model REST API

> **Backend / MLOps Project** | Python | FastAPI | Machine Learning | REST API

---

## 📌 Overview

A production-style REST API built with **FastAPI** that serves a trained machine learning model as an endpoint. The project covers the full ML deployment pipeline — from training a model, to wrapping it in a secure API, to serving it with a production-grade ASGI server.

This project demonstrates practical MLOps skills: taking a model beyond a notebook and deploying it as a usable, authenticated web service.

---

## ⚙️ How It Works

1. **Model Training** — `train_model.py` trains and serialises the ML model to disk
2. **API Layer** — FastAPI loads the trained model and exposes it via a REST endpoint
3. **Authentication** — Requests are secured with an API key via a `.env` config
4. **Serving** — The app is served using **Uvicorn**, a high-performance ASGI server

---

## 🗂️ Project Structure

```
api-test/
├── app/                  # FastAPI application (routes, model loading, logic)
├── run.py                # App entry point
├── train_model.py        # Model training & serialisation script
├── requirements.txt      # Python dependencies
├── clear_pycache.bat     # Utility script to clear Python cache
└── .gitignore
```

---

## 🛠️ Tech Stack

| Component | Tool |
|---|---|
| Language | Python 3.x |
| API Framework | FastAPI |
| ASGI Server | Uvicorn |
| ML Library | scikit-learn / joblib |
| Auth | API Key via `.env` |

---

## 🚀 Getting Started

**1. Clone the repo**
```bash
git clone https://github.com/steveparakal/api-test.git
cd api-test
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Train the model**
```bash
python train_model.py
```

**4. Create a `.env` file**
```
API_KEY=your_secret_key
```

**5. Start the API**
```bash
uvicorn run:app --reload
```

The API will be live at `http://127.0.0.1:8000`. Interactive docs available at `http://127.0.0.1:8000/docs`.

---

## 💡 Key Concepts Demonstrated

- **ML model deployment** — moving a trained model into a live REST API
- **FastAPI** — modern, async Python web framework with automatic OpenAPI docs
- **API key authentication** — securing endpoints with environment-based secrets
- **Separation of concerns** — training, serving, and routing kept modular

---

## 👤 Author

**Steve George Parakal** | [GitHub](https://github.com/steveparakal)
