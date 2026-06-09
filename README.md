


# 🏥 MediBot AI - Medical Chatbot with LLMs, LangChain, Pinecone & Flask

A full-stack AI-powered medical chatbot that answers health-related questions using Retrieval-Augmented Generation (RAG). Built with LangChain, Pinecone vector database, Groq LLM, and deployed via Flask.

---

## 🚀 Features

- 💬 Ask any medical question and get accurate, document-grounded answers
- 🔍 RAG pipeline using LangChain for context-aware responses
- 📚 PDF medical documents ingested and stored in Pinecone vector database
- ⚡ Fast inference using Groq's free LLM (Llama 3.1)
- 🌐 Clean and responsive web UI built with Flask

---

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| LLM | Groq (Llama 3.1 8B Instant) |
| Embeddings | HuggingFace (all-MiniLM-L6-v2) |
| Vector Database | Pinecone |
| RAG Framework | LangChain |
| Web Framework | Flask |
| Frontend | HTML, CSS, JavaScript |

---

## 📁 Project Structure

```
Medical-Chatbot/
├── src/
│   ├── helper.py        # PDF loading, chunking, embeddings
│   └── prompt.py        # System prompt for the LLM
├── templates/
│   └── chat.html        # Frontend chat UI
├── static/
│   └── style.css        # Styling
├── data/                # Medical PDF files
├── app.py               # Flask application
├── store_index.py       # Pinecone index creation and data ingestion
├── requirements.txt     # Python dependencies
└── .env                 # API keys (not tracked by git)
```

---

## ⚙️ Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/Aslamvs1/Medical-Chatbot-with-LLMs-LangChain-Pinecone-Flask-AWS.git
cd Medical-Chatbot-with-LLMs-LangChain-Pinecone-Flask-AWS
```

### 2. Create and activate conda environment
```bash
conda create -n medibot python=3.10
conda activate medibot
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Set up environment variables
Create a `.env` file in the root directory:
```
PINECONE_API_KEY=your-pinecone-api-key
GROQ_API_KEY=your-groq-api-key
```

- Get your free Pinecone API key at [pinecone.io](https://www.pinecone.io)
- Get your free Groq API key at [console.groq.com](https://console.groq.com)

### 5. Add medical PDF files
Place your medical PDF documents inside the `data/` folder.

### 6. Create Pinecone index and ingest data
```bash
python store_index.py
```

### 7. Run the Flask app
```bash
python app.py
```

Open your browser and go to `http://localhost:8080`

---

## 🖥️ Demo

![MediBot AI Chat Interface](screenshots/demo.png)

---

## 📌 How It Works

1. **Data Ingestion** — Medical PDF files are loaded, split into chunks, and embedded using HuggingFace
2. **Vector Storage** — Embeddings are stored in Pinecone vector database
3. **Query Processing** — User question is embedded and similar chunks are retrieved from Pinecone
4. **Answer Generation** — Retrieved context + question are passed to Groq LLM to generate a concise answer
5. **Response** — Answer is displayed in the chat UI

---

## 🔑 Environment Variables

| Variable | Description |
|---|---|
| `PINECONE_API_KEY` | Your Pinecone API key |
| `GROQ_API_KEY` | Your Groq API key |

---

## 👨‍💻 Author

**Muhammed Aslam V S**
---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).


