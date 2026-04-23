 Personalized Learning Assistant

*Making learning interactive and engaging through AI-powered challenges*

## 📖 Overview
Personalized Learning Assistant is an intelligent learning platform designed to help students practice and master their school subjects through interactive challenges. The application allows users to upload educational materials (like PDFs) and generates customized multiple-choice questions based on the content, tailored to their preferred difficulty level.

## ✨ Features

### 📚 Document Processing
- **PDF Upload**: Upload educational materials in PDF format
- **Text Extraction**: Automatically extracts and processes text from uploaded documents
- **Smart Parsing**: Identifies key concepts and topics from the material

### 🎯 AI-Powered Challenges
- **Adaptive Difficulty**: Questions generated based on user-selected difficulty (easy, medium, hard)
- **Context-Aware**: Questions are directly derived from the uploaded material
- **Multiple Choice Format**: Clean, easy-to-answer question format
- **Immediate Feedback**: Get explanations for correct and incorrect answers

### 🏆 User Experience
- **Simple Interface**: Clean, intuitive design focused on learning
- **Progress Tracking**: Monitor improvement over time
- **Responsive Design**: Works on desktop and mobile devices

## 🛠️ Technologies Used

### Frontend
- **React.js** - Frontend library for building user interfaces
- **Vite** - Fast development server and build tool
- **Tailwind CSS** - Utility-first CSS framework
- **Clerk** - Authentication and user management

### Backend
- **FastAPI** - Modern, fast web framework for building APIs
- **Python** - Backend programming language
- **SQLAlchemy** - SQL toolkit and ORM
- **LangChain** - Framework for developing applications with LLMs
- **Ollama** - Local LLM (Llama 3.2) for question generation
- **ChromaDB** - Vector database for document storage and retrieval

### Development Tools
- **Git** - Version control
- **Docker** - Containerization
- **Poetry** - Python dependency management

## 🚀 Getting Started

### Prerequisites
- Node.js (v16+)
- Python (3.9+)
- Ollama (with Llama 3.2 model)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Bethelakande/Just-some-shii.git
   cd Just-some-shii
   ```

2. **Set up the backend**
   ```bash
   cd backend
   poetry install
   poetry shell
   uvicorn main:app --reload
   ```

3. **Set up the frontend**
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

4. **Start Ollama**
   Make sure Ollama is running with the Llama 3.2 model:
   ```bash
   ollama pull llama3.2
   ```

## 🎯 Why I Built This

I created StudyBuddy AI to help my brother with his school work. Traditional study methods can be passive and less engaging, so I wanted to build a tool that would:

1. **Make learning active** through interactive challenges
2. **Save time** by automatically generating questions from study materials
3. **Adapt to different learning styles** with varying difficulty levels
4. **Be accessible** from anywhere, anytime

## 🚀 Future Improvements

### Enhanced AI Interaction
- **Conversational AI**: Allow users to ask follow-up questions about the material, making the learning experience more interactive and personalized
- **Personalized Learning Paths**: AI that adapts to the user's strengths and weaknesses, suggesting specific topics for improvement
- **Voice Interaction**: Support for voice commands and responses to make the app more accessible

### Expanded Features
- **Subject-Specific Templates**: Custom question formats for different subjects (math, science, history, etc.)
- **Peer Challenges**: Allow users to create and share challenges with classmates
- **Offline Mode**: Basic functionality without internet connection
- **Mobile App**: Native mobile experience for on-the-go learning

### Advanced Analytics
- **Performance Tracking**: Detailed insights into learning progress over time
- **Weakness Identification**: AI-powered analysis of areas needing improvement
- **Study Recommendations**: Personalized suggestions for what to study next based on performance

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Thanks to the open-source community for the amazing tools and libraries
- Special thanks to my brother for being the inspiration and first user!

---

Made with ❤️ by [Bethelakande] | [GitHub](https://github.com/Bethelakande)