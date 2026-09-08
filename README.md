```markdown
# Vocalis AI 

An open-source AI platform designed to analyze, extract, and generate writing styles using stylistic fingerprinting and verifiable author passports.

---

## Overview

Vocalis AI provides an end-to-end pipeline to analyze literary or domain-specific texts, construct quantitative style profiles, and generate content consistent with target authors or voices. The system features cryptographic "author passports" to verify stylistic authenticity and enforce licensing provenance.

## Core Features

* **Style Extraction Engine**: Quantifies lexical, syntactic, and stylistic metrics across arbitrary text corpora.
* **Dimensionality Reduction & Visualization**: Projects text embeddings and profile vectors using UMAP for cluster exploration.
* **FastAPI Backend**: Exposes REST endpoints for author profile management, token verification, text generation, and health checks.
* **Cryptographic Passport Builder**: Signs and verifies author style definitions using standard JWKS and asymmetric keypairs.
* **Configurable LLM Integrations**: Orchestrates generation prompts conditioned on calculated stylistic profiles.

---

## Project Structure

```text
├── ai_pipeline/          # Core NLP, style extraction, and verification modules
│   ├── Vocalis AI/       # Core extraction, chunking, conditioning, and passport schemas
│   └── tests/            # Test suite for AI pipeline components
├── backend/              # FastAPI application
│   ├── app/              # Routes, services, database interfaces, and configs
│   └── tests/            # Integration and endpoint test suites
├── corpus/               # Seed reference texts (e.g., Austen, Dickens, Poe)
└── Makefile              # Setup, linting, and execution workflows

```

---

## Getting Started

### Prerequisites

* Python 3.10+
* Poetry or `pip`
* Node.js (if utilizing optional UI modules)

### Installation

1. **Clone the repository:**
```bash
git clone <(https://github.com/Bhaskara-Shastry-S-P/Vocalis-AI)>
cd <Vocalis AI>

```


2. **Configure environment variables:**
```bash
cp .env.example .env
# Update the configuration in .env with your required API keys and settings

```


3. **Install dependencies:**
```bash
# AI Pipeline
cd ai_pipeline
pip install -e .

# Backend API
cd ../backend
pip install -r requirements.txt

```



---

## Running the Application

### Backend API Server

Run the FastAPI application locally:

```bash
cd backend
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

```

Access interactive API documentation at:

* Swagger UI: `http://localhost:8000/docs`
* ReDoc: `http://localhost:8000/redoc`

---

## Running Tests

Execute test suites across components:

```bash
# Run backend tests
cd backend
pytest

# Run pipeline unit tests
cd ../ai_pipeline
pytest

```

---



```

```
