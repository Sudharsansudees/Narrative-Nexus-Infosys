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

## 3️⃣ Start the backend
```bash
uvicorn backend.main:app --reload
```

## Backend runs at:
```bash
http://127.0.0.1:8000
```

## 📡 API Usage
Endpoint
```bash
POST /text/clean-and-summarize
```

## Sample Response
```bash
{
  "message": "Processed successfully",
  "preview": "First 500 characters...",
  "summary": "Generated summary text...",
  "sentiment": {
    "label": "POSITIVE",
    "score": 0.98
  }
}
```

## 🎨 Frontend Usage
Open frontend/index.html

Make sure the API URL is correct:
```bash
<span id="api-url">http://127.0.0.1:8000</span>
```
Upload or paste your text

Click Analyze to view cleaned text, summary, and sentiment

## 🧠 How It Works

BeautifulSoup removes HTML tags and unwanted markup

NLTK processes and tokenizes text

BART (facebook/bart-large-cnn) generates summaries

DistilBERT produces sentiment classification

FastAPI manages fast asynchronous API requests

## 🧭 Roadmap

 PDF / DOCX ingestion

 Multi-document summarization

 Improved UI with theme support

 Docker deployment

## 👤 Author

Built by Sudharsan M
For Infosys Internship Project

GitHub: https://github.com/sudharsansudees

