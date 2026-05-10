<div align="center">

<br/>

```
███████╗ █████╗ ███████╗████████╗ █████╗ ██████╗ ██╗
██╔════╝██╔══██╗██╔════╝╚══██╔══╝██╔══██╗██╔══██╗██║
█████╗  ███████║███████╗   ██║   ███████║██████╔╝██║
██╔══╝  ██╔══██║╚════██║   ██║   ██╔══██║██╔═══╝ ██║
██║     ██║  ██║███████║   ██║   ██║  ██║██║     ██║
╚═╝     ╚═╝  ╚═╝╚══════╝   ╚═╝   ╚═╝  ╚═╝╚═╝     ╚═╝
```

# 🚀 Deploying Machine Learning Models with FastAPI

**Production-ready ML model serving — fast, clean, and scalable.**

[![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100%2B-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-Latest-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://docker.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)

<br/>

> *"A model that isn't deployed is just a research project."*  
> This repo bridges that gap — beautifully.

<br/>

</div>

---

## 📌 Table of Contents

- [✨ Overview](#-overview)
- [🏗️ Architecture](#️-architecture)
- [📁 Project Structure](#-project-structure)
- [⚙️ Tech Stack](#️-tech-stack)
- [🚀 Getting Started](#-getting-started)
- [🔌 API Reference](#-api-reference)
- [🧪 Running Tests](#-running-tests)
- [🐳 Docker Deployment](#-docker-deployment)
- [📊 Example Predictions](#-example-predictions)
- [🤝 Contributing](#-contributing)
- [📜 License](#-license)

---

## ✨ Overview

This project demonstrates how to **train, serve, and deploy a machine learning model** as a production-grade REST API using **FastAPI** — one of the fastest Python web frameworks available.

Whether you're working with classification, regression, or NLP models, this template gives you a clean, scalable foundation to expose your ML models via HTTP endpoints — ready for real-world consumption.

### 🌟 Key Highlights

| Feature | Details |
|---|---|
| ⚡ **Ultra-fast API** | Powered by FastAPI + Uvicorn ASGI server |
| 🤖 **ML Integration** | Plug-and-play model loading (scikit-learn, joblib) |
| 📄 **Auto Docs** | Swagger UI & ReDoc out of the box |
| 🔒 **Validation** | Pydantic schemas for type-safe request/response |
| 🐳 **Containerized** | Docker-ready for any cloud deployment |
| 🧪 **Tested** | Pytest-based test suite included |

---

## 🏗️ Architecture

```
┌──────────────────────────────────────────────────────────┐
│                        CLIENT                            │
│              (Browser / Postman / App)                   │
└────────────────────────┬─────────────────────────────────┘
                         │  HTTP Request (JSON)
                         ▼
┌──────────────────────────────────────────────────────────┐
│                    FastAPI Server                        │
│  ┌─────────────────────────────────────────────────┐    │
│  │              Pydantic Validation                │    │
│  │         (Input schema enforcement)              │    │
│  └────────────────────┬────────────────────────────┘    │
│                       │                                  │
│  ┌────────────────────▼────────────────────────────┐    │
│  │              Prediction Router                  │    │
│  │          /predict  /health  /info               │    │
│  └────────────────────┬────────────────────────────┘    │
│                       │                                  │
│  ┌────────────────────▼────────────────────────────┐    │
│  │              ML Model (joblib)                  │    │
│  │         Loaded once at startup                  │    │
│  └─────────────────────────────────────────────────┘    │
└──────────────────────────────────────────────────────────┘
                         │  JSON Response
                         ▼
                    ✅ Prediction
```

---

## 📁 Project Structure

```
Deploying-Machine-Learning-Models-with-Fast-API/
│
├── 📂 app/
│   ├── 📄 main.py              # FastAPI app entry point
│   ├── 📄 model.py             # Model loading & prediction logic
│   ├── 📄 schemas.py           # Pydantic request/response schemas
│   └── 📂 routers/
│       └── 📄 predict.py       # Prediction endpoint router
│
├── 📂 models/
│   └── 📄 ml_model.joblib      # Serialized trained model
│
├── 📂 notebooks/
│   └── 📄 training.ipynb       # Model training notebook
│
├── 📂 tests/
│   └── 📄 test_api.py          # API test suite
│
├── 📄 requirements.txt         # Python dependencies
├── 📄 Dockerfile               # Docker container config
├── 📄 docker-compose.yml       # Multi-service orchestration
└── 📄 README.md                # You are here 👋
```

---

## ⚙️ Tech Stack

| Layer | Technology |
|---|---|
| 🌐 **Web Framework** | [FastAPI](https://fastapi.tiangolo.com/) |
| ⚡ **ASGI Server** | [Uvicorn](https://www.uvicorn.org/) |
| 🤖 **ML Framework** | [scikit-learn](https://scikit-learn.org/) |
| 📦 **Model Serialization** | [Joblib](https://joblib.readthedocs.io/) |
| ✅ **Data Validation** | [Pydantic v2](https://docs.pydantic.dev/) |
| 🧪 **Testing** | [Pytest](https://pytest.org/) + [HTTPX](https://www.python-httpx.org/) |
| 🐳 **Containerization** | [Docker](https://docker.com/) |

---

## 🚀 Getting Started

### Prerequisites

- Python **3.9+**
- pip / conda
- (Optional) Docker

---

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/osamashabih6960/Deploying-Machine-Learning-Models-with-Fast-API.git
cd Deploying-Machine-Learning-Models-with-Fast-API
```

### 2️⃣ Create a Virtual Environment

```bash
python -m venv venv

# Activate it:
# On macOS/Linux:
source venv/bin/activate

# On Windows:
venv\Scripts\activate
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Train & Save the Model

```bash
# Run the training notebook or script:
python train.py
```

> This generates `models/ml_model.joblib` — the serialized model loaded by the API.

### 5️⃣ Launch the API Server

```bash
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

🟢 **Server running at:** `http://localhost:8000`  
📖 **Interactive Docs:** `http://localhost:8000/docs`  
📚 **ReDoc:** `http://localhost:8000/redoc`

---

## 🔌 API Reference

### `GET /health`
Check if the API is alive and the model is loaded.

```json
// Response 200 OK
{
  "status": "healthy",
  "model_loaded": true
}
```

---

### `GET /info`
Get metadata about the deployed model.

```json
// Response 200 OK
{
  "model_name": "RandomForestClassifier",
  "version": "1.0.0",
  "features": ["feature_1", "feature_2", "feature_3"]
}
```

---

### `POST /predict`
Submit input features and receive a prediction.

**Request Body:**
```json
{
  "features": [5.1, 3.5, 1.4, 0.2]
}
```

**Response:**
```json
{
  "prediction": 0,
  "label": "setosa",
  "confidence": 0.97
}
```

**cURL Example:**
```bash
curl -X POST "http://localhost:8000/predict" \
     -H "Content-Type: application/json" \
     -d '{"features": [5.1, 3.5, 1.4, 0.2]}'
```

---

## 🧪 Running Tests

```bash
pytest tests/ -v
```

Expected output:

```
tests/test_api.py::test_health_check          PASSED  ✅
tests/test_api.py::test_predict_valid_input   PASSED  ✅
tests/test_api.py::test_predict_invalid_input PASSED  ✅
tests/test_api.py::test_model_info            PASSED  ✅

============= 4 passed in 0.87s =============
```

---

## 🐳 Docker Deployment

### Build & Run with Docker

```bash
# Build the image
docker build -t fastapi-ml-app .

# Run the container
docker run -d -p 8000:8000 fastapi-ml-app
```

### Using Docker Compose

```bash
docker-compose up --build
```

> 🚀 The API will be available at `http://localhost:8000`

---

## 📊 Example Predictions

Here's an end-to-end example using Python's `requests` library:

```python
import requests

url = "http://localhost:8000/predict"

payload = {
    "features": [6.3, 2.9, 5.6, 1.8]
}

response = requests.post(url, json=payload)
print(response.json())

# Output:
# {'prediction': 2, 'label': 'virginica', 'confidence': 0.91}
```

---

## 🤝 Contributing

Contributions are what make the open-source community amazing! 🙌

1. **Fork** the repository
2. **Create** your feature branch: `git checkout -b feature/amazing-feature`
3. **Commit** your changes: `git commit -m 'Add some amazing feature'`
4. **Push** to the branch: `git push origin feature/amazing-feature`
5. **Open** a Pull Request

Please make sure your code follows the existing style and includes tests. 💪

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<div align="center">

Made with ❤️ by [Osama Shabih](https://github.com/osamashabih6960)

⭐ **If this helped you, give it a star!** ⭐

</div>
