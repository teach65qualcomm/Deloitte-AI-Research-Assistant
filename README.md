# 🔷 Deloitte AI Research Assistant

An enterprise-grade **AI-powered research assistant** built with **Streamlit, LangChain, and Azure OpenAI**.
It enables intelligent conversations, real-time web research, document analysis, and image understanding in a single platform.

---

## ✨ Overview

The Deloitte AI Research Assistant is designed to:

* Provide accurate, structured answers using AI
* Perform real-time web research
* Analyze uploaded documents and images
* Maintain conversation history with memory
* Deliver a premium, modern user experience

---

## 🚀 Features

### 💬 Conversational AI

* Chat-based interface using Streamlit
* Multi-turn conversations with context
* Clean markdown-formatted responses

### 🌐 Web Search Integration

* Uses Tavily API for real-time data
* Automatically detects when fresh info is needed
* Displays sources separately

### 📄 Document Analysis

Supports:

* PDF
* DOCX
* TXT

Extracts and injects document context into responses

### 🖼️ Image Analysis

* Upload images (PNG, JPG, etc.)
* AI analyzes and describes visual content
* Supports multimodal queries

### 🌦️ Weather Tool

* Real-time weather lookup via API

### 🧠 Memory & History

* SQLite-based chat history
* Persistent conversations
* Session-based memory

### 👤 Authentication

* User login/signup
* Secure password hashing
* Role support (admin/user)

### 🎨 UI/UX

* Custom dark theme
* Deloitte-inspired design
* Clean chat and source display

---

## 🏗️ Architecture

```
Frontend (Streamlit)
        ↓
Application Logic (Python)
        ↓
LangChain Agent
        ↓
Azure OpenAI (LLM)
        ↓
Tools:
  - Web Search (Tavily)
  - Weather API
  - Document Context
  - Image Analysis
        ↓
SQLite Database
```

---

## 📂 Project Structure

```
.
├── app.py                  # Main application
├── research_assistant.db   # App database
├── agent_memory.db         # Agent memory
├── .env                    # Environment variables
├── requirements.txt        # Dependencies
└── README.md
```

---

## ⚙️ Setup Instructions

### 1. Clone Repository

```bash
git clone https://github.com/your-username/deloitte-ai-assistant.git
cd deloitte-ai-assistant
```

### 2. Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate     # Mac/Linux
venv\Scripts\activate        # Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file:

```
MODEL_ENDPOINT=your_azure_endpoint
CHAT_MODEL_NAME=your_model_name
AZURE_OPENAI_API_KEY=your_api_key
api_version=2024-08-01-preview

TAVILY_API_KEY=your_tavily_api_key
WEATHER_API_KEY=your_weather_api_key
```

### 5. Run the App

```bash
streamlit run app.py
```

---

## 🧩 Key Components

### Database

* SQLite storage
* Tables: users, conversations, messages, documents

### Agent System

* LangChain tool-calling agent
* Tools:

  * Web search
  * Weather
  * Document context
  * Image analysis

### File Processing

* PDF → PyMuPDF
* DOCX → python-docx
* TXT → native parsing
* Images → Base64 encoding

### UI

* Sidebar (history + uploads)
* Chat interface
* Source chips

---

## 🔒 Security

* Password hashing (SHA-256)
* No plaintext credentials
* Environment-based API keys

---

## 📈 Future Improvements

* Vector database (FAISS / Pinecone)
* Semantic document search
* Role-based access control
* Cloud deployment (Azure / AWS)
* Streaming responses

---

## 🤝 Contributing

1. Fork the repository
2. Create a new branch
3. Commit your changes
4. Submit a pull request

---

## 👨‍💻 Author

Built as an **AI-powered research assistant system** inspired by enterprise-grade solutions.

---

## ⭐ Support

If you like this project, please ⭐ the repository!

