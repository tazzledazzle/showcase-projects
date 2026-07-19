# 📝 Platform Audit Template

[![Documentation](https://img.shields.io/badge/Documentation-Comprehensive-blue)](./docs)
[![SRE](https://img.shields.io/badge/SRE-Best%20Practices-success)](https://sre.google/)
[![Templates](https://img.shields.io/badge/Templates-Ready%20to%20Use-orange)](./docs)

> Reusable SRE audit framework, runbooks, and operational documentation for assessing and maintaining production services.

## 🎯 Overview

**Problem:** Teams need a repeatable way to assess service and platform maturity (deployments, observability, security, testing, docs) without ad-hoc checklists.

**Solution:** This template provides a structured audit framework, runbook examples, and SRE communications checklists you can adapt for your organization.

**What this demonstrates:** Reusable SRE/audit artifacts and runbook documentation—drawn from experience conducting data platform audits across many services and writing SRE-facing documentation.

---

## 📚 Contents

| Artifact | Type | Description |
|----------|------|-------------|
| [Service/Platform Audit Template](docs/audit-template.md) | 📋 Template | Checklist and structure for assessing service maturity (deployments, observability, security, testing, docs) |
| [Runbook: Verify OTel Pipeline](docs/runbook-verify-otel-pipeline.md) | 📖 Runbook | Step-by-step runbook to verify OpenTelemetry traces and metrics are flowing |
| [Runbook: Cost/Billing Diagnostic](docs/runbook-billing-diagnostic.md) | 📖 Runbook | Pattern for safe, read-only cost/billing diagnostics (e.g. GCP) |
| [SRE Communications Checklist](docs/sre-communications-checklist.md) | ✅ Checklist | Time zones, handoffs, incident comms, and leaving-desk protocols |
| [Telemetry-Driven Rollout Playbook](docs/rollout-playbook.md) | 🚀 Playbook | Phases (pre-release, canary, staged), metrics to watch, rollback, and documentation |
| [Diagnostic Script Pattern](scripts/README.md) | 💻 Pattern | Safe, read-only diagnostic script pattern with an example (GCP billing summary) |

---

## 🚀 How to Use

### 1. 📋 Service Audits
Copy `docs/audit-template.md` (or the checklist sections) into your wiki or repo; fill per service or platform.

### 2. 📖 Operational Runbooks
Adapt the runbooks to your stack (OTel endpoints, cloud provider, tooling).

### 3. 💬 Team Communications
Use the SRE communications checklist for onboarding or team norms.

### 4. 🚀 Rollout Planning
Use the rollout playbook when planning canary or staged releases.

### 5. 💻 Diagnostic Scripts
Use `scripts/` as a pattern for read-only diagnostics; never commit credentials.

---

## 📄 License

MIT License - Use and adapt freely.

---

[← Back to Showcase Projects](../README.md)
