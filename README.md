# SurveillanceAI

> ML-powered market surveillance system for financial crime detection.  
> Graph analytics · Ensemble anomaly detection · LangGraph multi-agent triage

![Status](https://img.shields.io/badge/status-in%20development-orange)
![Python](https://img.shields.io/badge/python-3.11-blue)
![License](https://img.shields.io/badge/license-MIT-green)

---

## What This Is

SurveillanceAI is an open-source market surveillance system that detects anomalous trading behaviour and potential financial crime using a combination of graph analytics, ensemble ML models, and agentic LLM workflows.

Built by a forensic technology data scientist with 3 years of ML experience at a Big 4 firm.
---

## Architecture
Raw Trade Data → Neo4j Entity Graph → Anomaly Detection Ensemble → LangGraph Agent Pipeline → Alert Report

**Graph Layer** — Neo4j models trader → instrument → counterparty → alert relationships. Community detection and pathfinding surface hidden connections that tabular models miss.

**Detection Layer** — Ensemble of three models compared in benchmarks:
- Isolation Forest (fast baseline, interpretable)
- Autoencoder (learns normal behaviour distributions)
- LSTM (sequence anomalies — spoofing, layering patterns)

**Agent Layer** — LangGraph multi-agent pipeline:
1. Triage agent classifies alert severity
2. Retrieval agent pulls relevant case history via MCP
3. Analysis agent generates narrative explanation
4. Escalation agent routes to human review or auto-closes

**Explainability** — SHAP + attention visualisation. Regulators require it. It's built in from the start.

---

## Tech Stack

| Component | Technology |
|---|---|
| Graph database | Neo4j |
| ML models | scikit-learn, PyTorch, TensorFlow |
| LLM orchestration | LangChain, LangGraph |
| Embeddings / vector search | FAISS / Chroma |
| API | FastAPI |
| Dashboard | Streamlit |
| Cloud | Azure ML |
| Explainability | SHAP |

---

## Roadmap

- [ ] Neo4j schema: trader, instrument, counterparty, alert nodes
- [ ] Data ingestion pipeline (synthetic trade data)
- [ ] Isolation Forest baseline with benchmarks
- [ ] Autoencoder anomaly detector
- [ ] LSTM sequence model
- [ ] Ensemble combiner with SHAP explainability
- [ ] LangGraph multi-agent triage pipeline
- [ ] FastAPI backend
- [ ] Streamlit dashboard with live demo
- [ ] Open-source release with demo video

---

## Background

This project grew out of forensic data science work in eDiscovery and trader communications surveillance. The core insight: financial crime investigation is fundamentally a graph problem — entities, relationships, and sequences of behaviour matter more than individual data points.

The FCA's Market Abuse Regulation (MAR) defines four categories of market abuse. This system is designed with those categories in mind: insider dealing, market manipulation, unlawful disclosure, and attempted abuse.

---

## Status

**Active development — started June 2026.**  
Follow for updates. Contributions welcome once the core architecture is stable (target: October 2026).

---

## Author

Joseph Solomon — Forensic Data Scientist → ML Engineer  
[LinkedIn](https://linkedin.com/in/yourprofile) · [Portfolio](https://yoursite.com)
