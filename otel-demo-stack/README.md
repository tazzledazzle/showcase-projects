# 📊 OTel Demo Stack

[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.104+-009688?logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-Latest-3050A0?logo=opentelemetry&logoColor=white)](https://opentelemetry.io/)
[![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)

> End-to-end observability demonstration with OpenTelemetry instrumentation, distributed tracing, and metrics collection.

## 🎯 Overview

**Problem:** Demonstrate end-to-end observability with OpenTelemetry: one service, one worker, traces and metrics flowing to a backend (collector / Grafana or similar).

**Solution:** A minimal "observability in a box" setup: an instrumented API, an instrumented worker, OTLP export to an OpenTelemetry Collector, with W3C trace context propagation. Includes an SRE-facing **OpenTelemetry Verification Guide** and optional CI that checks the OTel health endpoint.

**What this demonstrates:** Designing and documenting an end-to-end observability pipeline and writing SRE verification docs—aligned with Temporal Worker observability, OTel verification guides, and OTLP/Datadog-style workflows.

---

## 📦 Contents

| Component | Description |
|-----------|-------------|
| **api** | Small FastAPI service with OTel instrumentation; exposes `/api/health` and `/api/health/otel` |
| **worker** | Minimal Python worker that does periodic tasks and emits spans/metrics with W3C trace context propagation |
| **collector** | OpenTelemetry Collector config (OTLP in, export to stdout or Prometheus/OTLP) |
| **docker-compose** | Runs api, worker, and collector for local use |

📚 **Verification Guide:** See [docs/opentelemetry-verification-guide.md](docs/opentelemetry-verification-guide.md) for detailed steps to confirm traces and metrics are flowing correctly.

---

## 🚀 How to Run

### Using Docker Compose (Recommended)

```bash
docker compose up --build
```

### Endpoints

- 🌐 **API:** http://localhost:8000  
- ✅ **Health Check:** http://localhost:8000/health  
- 📊 **OTel Health:** http://localhost:8000/api/health/otel  

### Usage

Trigger a request to the API; the worker runs on an interval. Traces and metrics are sent to the collector (see collector logs or configure a backend in `collector/otelcol.yaml`).

### Verification

📖 **Verification steps:** See [OpenTelemetry Verification Guide](docs/opentelemetry-verification-guide.md) for detailed instructions on validating your observability pipeline.

---

## 📄 License

MIT License - see the LICENSE file for details.

---

[← Back to Showcase Projects](../README.md)
