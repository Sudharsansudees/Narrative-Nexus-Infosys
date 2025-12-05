🌌 Narrative Nexus — Intelligent Text Exploration

Narrative Nexus is an end-to-end text processing system built using FastAPI, NLTK, BeautifulSoup, and Transformers.
It cleans raw text or HTML, generates high-quality summaries, and evaluates sentiment — all via a fast API.

✨ What This Project Does
🧼 Text Cleaning

Removes scripts, tags, styles, and unwanted HTML noise.

📘 Text Summarization

Uses facebook/bart-large-cnn for high-quality abstractive summaries.

💭 Sentiment Analysis

Provides emotional tone (Positive / Negative / Neutral) with confidence.

🏗️ Project Structure
nexusnarrative/
│
├── backend/
│   ├── main.py                 # FastAPI entry point
│   ├── routes/
│   │   └── text_routes.py      # API routes
│   ├── text_process/
│   │   ├── cleaner.py          # Cleaning logic
│   │   └── cleaned/            # Saved cleaned files
│   └── models/                 # Optional cached HF models
│
├── frontend/
│   └── index.html              # UI for interacting with the API
│
└── requirements.txt

⚙️ Backend Setup (FastAPI)
1️⃣ Create and activate a virtual environment
pip install uv
uv venv
source .venv/bin/activate       # Windows: .venv\Scripts\activate

2️⃣ Install dependencies
uv pip install -r requirements.txt

3️⃣ Run the backend
uvicorn backend.main:app --reload


Backend runs at:

http://127.0.0.1:8000

📡 API Usage
Endpoint
POST /text/clean-and-summarize

Sample Response
{
  "message": "File cleaned, summarized, and analyzed successfully!",
  "preview": "First 500 chars...",
  "summary": "AI-generated summary text...",
  "sentiment": {
    "label": "POSITIVE",
    "score": 0.987
  }
}

🎨 Frontend Setup

Open frontend/index.html

Ensure the API URL is correct:

<span id="api-url">http://127.0.0.1:8000</span>


Upload or paste text

Click Analyze

🧠 How It Works

NLTK cleans and tokenizes text

BeautifulSoup strips HTML elements

BART (facebook/bart-large-cnn) creates summaries

DistilBERT detects sentiment

FastAPI connects everything through endpoints

🧰 Offline Model Usage (Optional)
from transformers import pipeline

summarizer = pipeline(
    "summarization",
    model="facebook/bart-large-cnn",
    cache_dir="./nexusnarrative/models"
)


Enable:

export TRANSFORMERS_OFFLINE=1

📘 Roadmap

 Multi-document summarization

 PDF and DOCX ingestion

 Docker deployment

 Enhanced frontend

👤 Author

Developed by Sudharsan M
Infosys Internship Project
GitHub: https://github.com/sudharsansudees
