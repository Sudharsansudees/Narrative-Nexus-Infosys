# 🧠 Narrative Nexus — Intelligent Text Exploration

Narrative Nexus is an end-to-end text processing system built using **FastAPI**, **Transformers**, **NLTK**, and **BeautifulSoup**.  
It transforms raw or messy text into meaningful summaries with sentiment insights.

---

## ✨ Features

- 🧼 **Text Cleaning** – Removes HTML tags, scripts, styling, and unnecessary formatting.
- 📘 **Summarization** – Generates concise, high-quality summaries using `facebook/bart-large-cnn`.
- 💬 **Sentiment Analysis** – Detects Positive, Negative, or Neutral tone with confidence scores.
- ⚡ **FastAPI Backend** – Lightweight, async, and production-ready.
- 🌐 **Simple Frontend** – Easy-to-use HTML interface for testing and demos.

---

## 🏗️ Project Structure

```text
nexusnarrative/
│
├── backend/
│   ├── main.py                 # FastAPI entry point
│   ├── routes/
│   │   └── text_routes.py      # API routes
│   ├── text_process/
│   │   ├── cleaner.py          # Cleaning logic
│   │   └── cleaned/            # Saved cleaned files
│   └── models/                 # Optional cached Transformer models
│
├── frontend/
│   └── index.html              # Simple UI for interacting with the API
│
└── requirements.txt

```
## ⚙️ Backend Setup (FastAPI)

## 1️⃣ Create and activate a virtual environment
```bash
pip install uv
uv venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
```

## 2️⃣ Install dependencies
```bash
uv pip install -r requirements.txt
```



