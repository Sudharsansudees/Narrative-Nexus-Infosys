📌 Narrative Nexus – Topic Modeling & Sentiment Analysis Platform

Narrative Nexus is an end-to-end text analysis platform that performs topic modeling on the 20-Newsgroups dataset and applies sentiment analysis to user-entered text.
It includes a Flask web interface, a trained ML model, and a premium-style UI for seamless interaction.

🚀 Features

🧠 Topic Modeling using LDA on the 20-Newsgroups dataset

😊 Sentiment Analysis (Positive / Negative / Neutral)

🌐 Flask Web Application with modern UI

📊 Interactive Results showing topic distribution

🏗️ Clean and scalable project structure

💾 Model training script included (train_topic_model.py)

🗂️ Project Structure
Narrative-Nexus/
│── static/
│   ├── css/
│   ├── js/
│   └── images/
│── templates/
│   ├── index.html
│   └── result.html
│── models/
│   ├── lda_model.pkl
│   ├── vectorizer.pkl
│   └── sentiment_model.pkl
│── train_topic_model.py
│── sentiment.py
│── web_app.py
│── README.md
│── requirements.txt

🛠️ Technologies Used

Python

Flask

Scikit-learn

NLTK

Joblib

HTML, CSS, JavaScript

🔧 Installation & Setup
1️⃣ Clone the repository
git clone https://github.com/your-username/narrative-nexus.git
cd narrative-nexus

2️⃣ Create and activate a virtual environment
python -m venv venv
venv\Scripts\activate   # Windows

3️⃣ Install dependencies
pip install -r requirements.txt

4️⃣ Train the topic model (optional)
python train_topic_model.py

5️⃣ Run the web application
python web_app.py

🌟 How It Works
1. Topic Modeling

Uses LDA to extract the dominant topic from the text and provide keyword distribution.

2. Sentiment Analysis

Classifies text into:

Positive

Negative

Neutral

3. Web Interface

Users can:

Enter text

View extracted topic

View sentiment result

📸 UI Preview

(Add images when you upload screenshots)

📦 Requirements

See requirements.txt
Typical libraries include:

flask
scikit-learn
joblib
nltk

🤝 Contributing

Pull requests are welcome!
For major updates, please open an issue to discuss changes.

📄 License

MIT License

👨‍💻 Author

Sudharsan M
Final Year CSE | AI Enthusiast
GitHub: https://github.com/sudharsansudees
