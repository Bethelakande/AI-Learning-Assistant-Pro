# 🎓 AI Learning Assistant - Frontend

*Empowering students with AI-driven, personalized learning experiences.*

---

## 📖 Project Overview

The **AI Learning Assistant** (frontend) is a modern, responsive web application designed to transform static educational materials into interactive learning journeys. By leveraging advanced AI, the platform allows students to upload their study materials and instantly engage with customized challenges that reinforce understanding.

This project was born out of a desire to make learning more active and engaging, moving away from passive reading to active recall and application.

## ✨ Key Features

- **🔐 Seamless Authentication**: Integrated with **Clerk** for secure and easy user management.
- **📄 Intelligent Document Upload**: Support for PDF educational materials (with more formats coming soon).
- **🎯 Interactive AI Challenges**: Real-time generation of multiple-choice questions based on uploaded content.
- **⚡ Fast & Responsive**: Built with **Vite** and **React** for a snappy, high-performance user experience.
- **🎨 Modern UI**: Styled with **Tailwind CSS** for a clean, accessible, and premium interface.

## 🛠️ Tech Stack

- **Framework**: [React.js (v19)](https://react.dev/)
- **Build Tool**: [Vite](https://vitejs.dev/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **Authentication**: [Clerk](https://clerk.com/)
- **Routing**: [React Router DOM](https://reactrouter.com/)
- **API Integration**: Seamless communication with a FastAPI backend, utilizing LangChain for orchestration and Ollama for local LLM inference.

## ⚙️ Deep Dive: Backend Architecture

The backend is built for speed, privacy, and scalability. It handles the "heavy lifting" of document processing and AI generation.

### 🧠 AI & LLM Integration
- **Ollama (Llama 3.2)**: We use local LLM inference for maximum privacy and zero latency from external APIs.
- **LangChain**: Orchestrates the interaction between our vector store and the LLM.
- **RAG (Retrieval-Augmented Generation)**: Instead of just passing raw text, the backend retrieves relevant context from your documents to ensure high-accuracy question generation.

### 🗄️ Storage & Databases
- **ChromaDB**: A high-performance vector database that stores document embeddings for instant retrieval.
- **SQLite (SQLAlchemy)**: Manages relational data such as user profiles, challenge history, and progress tracking.
- **Ollama Embeddings**: Uses the `mxbai-embed-large` model to convert text into searchable mathematical vectors.

### 🛠️ Key Backend Services
- **`vector.py`**: Handles document ingestion, PDF parsing, and embedding generation.
- **`ai_generator.py`**: A robust service that manages prompt engineering and ensures the LLM returns structured, valid JSON for the frontend.
- **`routes/challenge.py`**: The primary API gateway for generating challenges and processing user answers.

### Prerequisites
- Node.js (v18+)
- npm or yarn

### Installation

1. **Install dependencies**
   ```bash
   npm install
   ```

2. **Configure Environment Variables**
   Create a `.env` file in the `frontend` root and add your Clerk keys:
   ```env
   VITE_CLERK_PUBLISHABLE_KEY=your_publishable_key
   ```

3. **Launch Development Server**
   ```bash
   npm run dev
   ```

## 🏗️ Future Improvements & Roadmap

We are constantly evolving the AI Learning Assistant to provide a more holistic educational experience. Our upcoming roadmap includes:

### 📂 Multi-Format Support
Break beyond PDF limitations. We are working on allowing users to upload:
- **Microsoft Word (.docx)** and **Text (.txt)** files.
- **Images/Photos**: Capture handwritten notes or textbook pages and process them via OCR.
- **Audio/Video**: Upload lectures or links to educational videos for transcript-based challenge generation.

### 🤖 Agentic Teaching Workflows
Moving from a "quizzer" to a "teacher". We are integrating more in-depth **Agentic Workflows** that:
- **Identify Knowledge Gaps**: The AI agent analyzes your mistakes to pinpoint exactly where you are struggling.
- **Suggest Resources**: Dynamically recommend external resources like specific YouTube tutorials, Wikipedia articles, or open-source textbooks.
- **Socratic Tutoring**: A chat interface that guides you to the answer through hints and questions rather than just providing it.

### 🧩 Deep Personalization & Accessibility
Making learning accessible to everyone. New features will include:
- **Learning Preferences**: Input your preferred style (e.g., visual, summarized, or deep-dive) to have the AI adapt its teaching method.
- **Accessibility Layers**: Enhanced support for screen readers, high-contrast modes, and simplified layouts for neurodivergent learners.
- **Adaptive Difficulty**: AI that learns your pace and adjusts the complexity of materials and questions over time.

---

Made with ❤️ by [Bethelakande]

