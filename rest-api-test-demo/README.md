# 🔌 REST API Test Demo

[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.104+-009688?logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![Pytest](https://img.shields.io/badge/Pytest-Latest-0A9EDC?logo=pytest&logoColor=white)](https://pytest.org/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)

> Production-grade REST API with comprehensive testing, OpenAPI documentation, and CI/CD integration.

## 🎯 Overview

**Problem:** Show a minimal but production-style REST API with a clear contract, automated tests, and runnable deployment.

**Solution:** A small FastAPI service with OpenAPI/Swagger, unit and integration tests, Docker, and CI that runs tests and builds the image.

**What this demonstrates:** Shipping a well-tested, documented service and articulating QA practices (test cases, automation)—aligned with RESTful web services, Dockerized apps, and test plans.

---

## 📦 Contents

| Component | Description |
|-----------|-------------|
| **API** | FastAPI app with CRUD-style resources (e.g. items) |
| **OpenAPI** | Interactive documentation at `/docs` and `/openapi.json` |
| **Tests** | Pytest unit and integration tests with coverage reporting |
| **Docker** | Dockerfile and docker-compose for local deployment |
| **CI** | GitHub Actions: run tests, optionally build image |

📚 **Test Strategy:** See [Test approach](docs/test-plan.md) for detailed testing methodology.

---

## 🚀 How to Run

### Local Development (No Docker)

```bash
python -m venv .venv
source .venv/bin/activate   # or .venv\Scripts\activate on Windows
pip install -r requirements.txt
uvicorn app.main:app --reload
```

🌐 **API:** http://localhost:8000  
📚 **Swagger UI:** http://localhost:8000/docs

### Using Docker (Recommended)

```bash
docker compose up --build
```

🌐 **API:** http://localhost:8000  
📚 **Swagger UI:** http://localhost:8000/docs

---

## 🧪 Running Tests

```bash
pip install -r requirements.txt
pytest -v

# With coverage report:
pytest -v --cov=app --cov-report=term-missing
```

---

## 📄 License

MIT License - see the LICENSE file for details.

---

[← Back to Showcase Projects](../README.md)
