# 🧠 AI Learning Assistant - Backend

*The intelligent core powering personalized learning.*

---

## 🚀 Overview

The backend of the **AI Learning Assistant** is a high-performance, AI-integrated API built with **FastAPI**. it handles the complex logic of document parsing, vector embedding, and AI-driven challenge generation using local LLM inference.

## 🛠️ Technical Architecture

### ⚡ Core Framework
- **FastAPI**: Asynchronous Python framework for building high-concurrency APIs.
- **SQLAlchemy (SQLite)**: ORM for managing user data, challenge logs, and learning progress.
- **Uvicorn**: Lightning-fast ASGI server for production deployment.

### 🤖 AI System (RAG Pipeline)
We implement a **Retrieval-Augmented Generation (RAG)** pipeline to ensure challenges are contextually grounded and accurate:
1.  **Ingestion**: Files (PDF, TXT) are uploaded and processed.
2.  **Vectorization**: Text is converted into 1024-dimensional vectors using the `mxbai-embed-large` model.
3.  **Storage**: Vectors are stored in **ChromaDB** for efficient semantic search.
4.  **Retrieval**: When a challenge is requested, relevant context is retrieved from the vector store.
5.  **Generation**: **Ollama (Llama 3.2)** uses the context and difficulty parameters to generate a structured JSON challenge.

## 📁 Source Code Breakdown

- **`src/app.py`**: The entry point, configuring CORS and assembling the router.
- **`src/routes/challenge.py`**: Handles API requests for generating new learning challenges.
- **`src/ai_generator.py`**: The "brains" of the operation—manages prompt templates and LLM chain execution.
- **`src/vector.py`**: Manages the life-cycle of document embeddings and the ChromaDB collection.
- **`src/database/`**: Contains the SQLAlchemy models and session management for relational data.

## 🔧 Installation & Setup

### Prerequisites
- Python 3.9+
- [Ollama](https://ollama.ai/) (Running locally)
- [Poetry](https://python-poetry.org/) (Recommended)

### Steps

1. **Install Dependencies**
   ```bash
   poetry install
   # OR
   pip install -r requirements.txt
   ```

2. **Pull the required models**
   ```bash
   ollama pull llama3.2
   ollama pull mxbai-embed-large
   ```

3. **Configure Environment**
   Create a `.env` in `backend/src/` with necessary database and API keys.

4. **Run the server**
   ```bash
   uvicorn src.app:app --reload
   ```

## 📈 Future Backend Roadmap

- **Advanced Chunking**: Implementing semantic chunking for better context retrieval in large documents.
- **Agentic Resource Discovery**: A new service to crawl verified educational APIs (like Khan Academy or Wikipedia) to suggest resources.
- **Multi-Tenant Vector Isolation**: Ensuring user data privacy by partitioning vector collections by user ID.
- **Voice Synthesis**: Adding an endpoint for converting generated text to speech for accessible learning.

---

Made with ❤️ by [Bethelakande]
