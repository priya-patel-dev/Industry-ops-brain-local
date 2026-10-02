# Ops Brain Local

An offline, on-device AI assistant and agent platform built for industrial knowledge intelligence, operations analysis, and local decision support.

## Overview
Ops Brain Local is designed for industrial and plant environments where data privacy, offline access, and fast local intelligence matter most. It supports document understanding, plant query workflows, compliance checks, and operational assistance without sending sensitive information to the cloud.

## Features
- Local document parsing for PDFs, images, Excel files, and HTML
- On-device LLM responses with citation support
- Hybrid retrieval using vector search and knowledge graphs
- Specialized local agents for maintenance, compliance, and incident review
- Streamlit-powered operational dashboard

## Tech Stack
- Frontend: Streamlit
- Backend: FastAPI
- AI/ML: Qwen2.5, Docling, spaCy, ChromaDB, NetworkX
- Deployment: Local-first / edge-ready

## Architecture
```text
[UI: Streamlit] <---> [Backend: FastAPI] <---> [RAG Pipeline]
                                              |
                    +---------------------------+---------------------------+
                    |                           |                           |
        [Docling + spaCy]          [ChromaDB]               [NetworkX]
     (Document Parsing)         (Vector Retrieval)       (Knowledge Graph)
```

## Quick Start
### 1. Install dependencies
```bash
pip install -r requirements.txt
python -m spacy download en_core_web_sm
```

### 2. Download model and quantize
```bash
python scripts/download_model.py
```

### 3. Run the unified launcher
```bash
python run.py --demo
```

This starts the sample data workflow, launches the FastAPI server, and opens the Streamlit dashboard for local operational use.

## Project Goal
To build a privacy-safe, local-first industrial intelligence system that helps teams work with operational knowledge efficiently and securely.

## My Contribution
This project reflects applied AI engineering in industrial settings, focusing on offline inference, knowledge retrieval, and local operational tooling.

## Status
Advanced prototype / applied AI project

---

*Zero bytes sent to cloud. Built for OSDHack 2026.*
