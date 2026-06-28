# 🎥 Video RAG Assistant

> An AI-powered Video Assistant that allows users to upload videos, generate transcripts, build a Retrieval-Augmented Generation (RAG) pipeline, and ask context-aware questions using Large Language Models.

![Python](https://img.shields.io/badge/Python-3.11-blue)
![LangChain](https://img.shields.io/badge/LangChain-Latest-green)
![LangGraph](https://img.shields.io/badge/LangGraph-Agent-orange)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-teal)
![Streamlit](https://img.shields.io/badge/Streamlit-Frontend-red)


---

## 📖 Overview

Video RAG Assistant is an end-to-end AI application that transforms videos into an interactive knowledge base. The system automatically extracts audio, generates transcripts, creates semantic embeddings, stores them in a vector database, and enables users to ask natural language questions grounded in the video's content.

Instead of relying solely on an LLM's knowledge, the assistant retrieves relevant transcript chunks before generating responses, resulting in more accurate, explainable, and context-aware answers.

---

## ✨ Features

- 🎥 Upload video files
- 🎙 Extract audio automatically
- 📝 Generate transcripts using Whisper
- ✂️ Intelligent text chunking
- 🔍 Semantic search using vector embeddings
- 🧠 Retrieval-Augmented Generation (RAG)
- 💬 Conversational question answering
- 📌 Timestamp-aware responses *(Planned)*
- 📚 Conversation memory
- 📄 AI-powered video summarization
- 📂 Support for multiple videos *(Planned)*
- ⚡ Fast retrieval using ChromaDB / FAISS
- 🤖 LangGraph agent workflow *(Optional)*

---

## 🏗️ Project Architecture

```text
                Upload Video
                      │
                      ▼
             Video Processing
                      │
                      ▼
              Audio Extraction
                      │
                      ▼
              Whisper Transcription
                      │
                      ▼
                Text Chunking
                      │
                      ▼
               Create Embeddings
                      │
                      ▼
            Vector Database (Chroma)
                      │
                      ▼
               User asks Question
                      │
                      ▼
          Retrieve Relevant Chunks
                      │
                      ▼
              Large Language Model
                      │
                      ▼
              AI Generated Answer
```

---

## 📂 Project Structure

```text
video-rag-assistant/
│
├── app/
│   ├── frontend/
│   ├── backend/
│   └── services/
│
├── rag/
│   ├── chunking.py
│   ├── retriever.py
│   ├── vector_store.py
│   ├── prompt.py
│   ├── chains.py
│   └── memory.py
│
├── models/
├── database/
├── uploads/
├── data/
├── utils/
├── tests/
├── notebooks/
├── docs/
│
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
├── README.md
└── run.py
```

---

# 🛠️ Tech Stack

## Backend

- Python
- FastAPI

## Frontend

- Streamlit

## LLM

- OpenAI GPT
- Gemini
- Groq (Optional)

## Frameworks

- LangChain
- LangGraph

## Speech-to-Text

- OpenAI Whisper

## Embedding Models

- BAAI/bge-small-en-v1.5
- all-MiniLM-L6-v2

## Vector Database

- ChromaDB
- FAISS

## Database

- SQLite

## Deployment

- Docker
- Hugging Face Spaces
- Render

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/video-rag-assistant.git

cd video-rag-assistant
```

---

## Create Virtual Environment

Windows

```bash
python -m venv .venv

.venv\Scripts\activate
```

Linux / Mac

```bash
python3 -m venv .venv

source .venv/bin/activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Environment Variables

Create a `.env` file

```env
OPENAI_API_KEY=
GOOGLE_API_KEY=
GROQ_API_KEY=

EMBEDDING_MODEL=BAAI/bge-small-en-v1.5
VECTOR_DB=chroma
```

---

## Run Backend

```bash
python run.py
```

or

```bash
uvicorn app.backend.main:app --reload
```

---

## Run Frontend

```bash
streamlit run app/frontend/app.py
```

---

# 🧠 How It Works

### Step 1

Upload a video.

↓

### Step 2

Extract audio.

↓

### Step 3

Generate transcript.

↓

### Step 4

Split transcript into chunks.

↓

### Step 5

Generate embeddings.

↓

### Step 6

Store embeddings inside ChromaDB.

↓

### Step 7

User asks a question.

↓

### Step 8

Retriever fetches relevant chunks.

↓

### Step 9

LLM generates the final answer using retrieved context.

---

# 📸 Demo

```
Coming Soon
```

---

# 📊 Future Improvements

- Timestamp-based citations
- Multi-video knowledge base
- OCR support for slides
- Speaker diarization
- YouTube URL support
- Hybrid Search
- Reranking
- Agentic RAG
- Multimodal RAG
- PDF + Video Chat
- Voice Chat
- Video Summary PDF Export

---

# 🧪 Testing

```bash
pytest tests/
```

---

# 📈 Roadmap

- [x] Video Upload
- [x] Audio Extraction
- [x] Whisper Transcription
- [x] RAG Pipeline
- [x] Chat Interface
- [ ] Timestamp References
- [ ] Multi Video Support
- [ ] LangGraph Agent
- [ ] Docker Deployment
- [ ] Cloud Deployment

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new branch

```bash
git checkout -b feature-name
```

3. Commit changes

```bash
git commit -m "Added new feature"
```

4. Push branch

```bash
git push origin feature-name
```

5. Open a Pull Request

---

# 📜 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Shivam Singh**

AI & Machine Learning Engineer

- GitHub: https://github.com/shivamsingh-itds
- LinkedIn: https://linkedin.com/in/shivam-singh-itds

---

## ⭐ If you found this project helpful, please consider giving it a Star!