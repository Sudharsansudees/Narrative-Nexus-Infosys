🧠 Narrative Nexus

A simple yet powerful text-analysis app built with Flask + Transformers + Vanilla JS that lets you:

🧹 Clean raw text or HTML content

✂️ Summarize the cleaned text

💬 Analyze sentiment (Positive / Negative / Neutral)

🎨 Access a minimal, premium dark-theme UI

All in one neat, modern interface.

🚀 Features

📂 Drag & Drop Uploads — upload .txt or .html files directly

⚡ Instant Cleaning — removes HTML tags, scripts & unwanted formatting

🤖 AI-Powered Topic Modeling — LDA based topic extraction

😊 Sentiment Analysis — interprets the emotional tone of text

🧠 ML Models Included — trained LDA + vectorizer

🌐 Flask Backend — lightweight and simple

🎨 Clean UI — minimal HTML + CSS

🧩 Modular Code Structure

🗂 Project Structure
Narrative-Nexus/
│── static/
│   ├── css/
│   ├── js/
│   └── images/
│
│── templates/
│   ├── index.html
│   └── result.html
│
│── models/
│   ├── lda_model.pkl
│   ├── vectorizer.pkl
│   └── sentiment_model.pkl
│
│── train_topic_model.py
│── sentiment.py
│── web_app.py
│── requirements.txt
│── README.md

⚙️ Backend Setup (Flask)
1️⃣ Create & activate a virtual environment
python -m venv venv
venv\Scripts\activate   # Windows

2️⃣ Install dependencies
pip install -r requirements.txt

3️⃣ Train the topic model (optional)
python train_topic_model.py

4️⃣ Run the server
python web_app.py


Backend will run at:
👉 http://127.0.0.1:5000

🧪 API Endpoint
POST /analyze

Accepts text and returns:

{
  "topic": "Science—Space",
  "keywords": ["NASA", "orbit", "planet"],
  "sentiment": "Positive"
}

🎨 Frontend Setup

Open templates/index.html

Upload or paste text

Click Analyze to see topic + sentiment results

🧠 How It Works
🟦 Topic Modeling

Uses LDA to extract the dominant topic from user text.

🟩 Sentiment Analysis

Predicts whether the text is Positive / Negative / Neutral.

🟥 UI Layer

Minimal HTML + CSS + JS files render results in a clean layout.

📦 Requirements
flask
scikit-learn
nltk
joblib

👨‍💻 Author

Sudharsan M
AI Enthusiast | CSE Final Year

GitHub: https://github.com/sudharsansudees
