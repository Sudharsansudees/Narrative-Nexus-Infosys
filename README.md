# 🧠 Narrative Nexus

A simple yet powerful web app built with **FastAPI + Transformers + Vanilla JS** that lets you:

- 🧹 Clean raw text or HTML content (using NLTK + BeautifulSoup)
- ✂️ Summarize the cleaned text using `facebook/bart-large-cnn`
- 💬 Analyze the **sentiment** (Positive / Negative / Neutral) of the generated summary

All in one neat, minimal dark-themed interface.

---

## 🚀 Features

- **Drag & Drop Uploads** — upload `.txt` or `.html` files directly  
- **Instant Cleaning** — removes HTML tags, scripts, and unwanted formatting  
- **AI-Powered Summarization** — compresses long text into key insights  
- **Sentiment Analysis** — interprets the emotional tone of the text  
- **FastAPI Backend** — lightweight and async  
- **Vanilla JS Frontend** — no frameworks, just clean HTML + JS  
- **Offline-ready** — supports loading models locally to avoid re-downloads  

---

### 🧩 Project Structure

├── nexusnarrative/
│ ├── backend/
│ │ ├── main.py # FastAPI entry point
│ │ ├── routes/
│ │ │ └── text_routes.py # /clean-and-summarize endpoint
│ │ ├── text_process/
│ │ │ ├── cleaner.py # Uses NLTK + BeautifulSoup
│ │ │ └── cleaned/ # Output directory
│ └── models/ # (optional) local cached transformers models
│
├── frontend/
│ └── index.html # Minimal UI
│
└── requirements.txt


---

## ⚙️ Backend Setup (FastAPI)

### 1️⃣ Create and activate a virtual environment

```bash
uv venv   # install uv using: pip install uv
source .venv/bin/activate     # on Windows: .venv\Scripts\activate

2️⃣ Install dependencies
uv pip install -r requirements.txt

3️⃣ Run the backend
uvicorn backend.main:app --reload

Backend now runs at:
http://127.0.0.1:8000

Example API Endpoint
POST /text/clean-and-summarize

Response:
{
  "message": "File cleaned, summarized, and analyzed successfully!",
  "preview": "First 500 chars...",
  "summary": "AI-generated summary text...",
  "sentiment": {
    "label": "POSITIVE",
    "score": 0.987
  }
}

💻 Frontend Setup

Open frontend/index.html in your browser.

Ensure the API base URL points to your FastAPI backend:
<code id="api-url">http://127.0.0.1:8000</code>

Upload or paste text → click Clean, Summarize & Analyze

🧠 How It Works

Text is cleaned using NLTK + BeautifulSoup

Summary generated using BART (facebook/bart-large-cnn)

Sentiment evaluated using a DistilBERT model

Response returns:

cleaned preview

summary

sentiment label + confidence score

🗂 Example Output
Input: 3-page HTML article on global warming
→ Cleaned: ~4,500 words
→ Summary: “Global emissions continue to rise as countries struggle to meet Paris targets...”
→ Sentiment: NEGATIVE (confidence: 98.7%)

🏁 Future Enhancements

 Translation support

 Multilingual sentiment detection

 Export results as .txt

 Docker deployment

 👤 Author

Built for Infosys Internship Project
Developed by Sudharsan M

📧 Contact: sudharsansudees@gmail.com.com

🔗 GitHub: https://github.com/sudharsansudees
