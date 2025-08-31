# 🎙 Murf AI Voice Agent

A modern, production-ready voice-to-voice conversational AI agent with a sleek dark interface and robust architecture. Talk naturally with AI and get spoken responses in real-time.

## ✨ Features

- *Voice Conversations* - Speak naturally and get AI responses in voice  
- *Modern UI* - Dark theme with glass-morphism design and smooth animations  
- *Real-time Processing* - Fast speech recognition and response generation  
- *Session Management* - Maintains conversation context  
- *Responsive Design* - Works on desktop, tablet, and mobile  
- *Type Safety* - Pydantic schemas for robust API validation  
- *Service Architecture* - Clean separation of concerns with dedicated service classes  
- *Production Ready* - Optimized code with proper error handling  

## 🏗 Architecture

### Service-Based Design
- *STT Service* - AssemblyAI speech-to-text integration  
- *LLM Service* - Google Gemini AI processing  
- *TTS Service* - Murf AI text-to-speech generation  
- *Type Safety* - Pydantic models for request/response validation  

### Tech Stack
- *Backend*: FastAPI (Python) with Pydantic validation  
- *Frontend*: HTML5, CSS3, JavaScript (optimized)  
- *Speech-to-Text*: AssemblyAI  
- *AI Model*: Google Gemini 2.5 Flash  
- *Text-to-Speech*: Murf AI  

## 🚀 Quick Setup

### Prerequisites
- Python 3.8+  
- Modern web browser with microphone access  

### Installation

1. *Clone the repository*
```bash
git clone https://github.com/MdMohameenQureshi/AI-Voice-Agent.git
cd AI-Voice-Agent
Install dependencies

bash
Copy code
pip install -r requirements.txt
Configure API keys

Copy the example environment file and add your API keys:

bash
Copy code
cp .env.example .env
Edit .env with your API keys:

env
Copy code
# AssemblyAI Configuration (Speech-to-Text)
AssemblyAI_API_KEY=your_assemblyai_api_key_here

# Google Gemini Configuration (Language Model)  
GOOGLE_API_KEY=your_google_gemini_api_key_here

# Murf AI Configuration (Text-to-Speech)
MURF_API_KEY=your_murf_api_key_here
Run the application

bash
Copy code
uvicorn main:app --reload
Open in browser

http://localhost:8000

🎮 Usage
Click the toggle button to start/stop recording

Speak clearly into your microphone

The AI will process your speech and respond with voice

Continue the conversation naturally

📁 Project Structure
bash
Copy code
murf-ai-voice-agent/
├── main.py              # FastAPI server with clean endpoint handlers
├── schemas.py           # Pydantic models for type safety
├── services/            # Service layer architecture
│   ├── __init__.py      # Service exports
│   ├── stt_service.py   # AssemblyAI speech-to-text service
│   ├── llm_service.py   # Google Gemini LLM service
│   └── tts_service.py   # Murf AI text-to-speech service
├── templates/           
│   └── index.html       # Optimized voice interface
├── static/
│   ├── style.css        # Consolidated modern dark theme
│   └── script.js        # Optimized voice recording functionality
├── .env                 # API configuration (create from .env.example)
├── .env.example         # Environment template
├── requirements.txt     # Python dependencies
└── README.md            # Documentation
🔧 API Endpoints
The application provides clean, type-safe API endpoints with Pydantic validation:

POST /stt/transcribe - Speech-to-text transcription

POST /tts/echo - Text-to-speech with transcription echo

POST /llm/query - LLM query processing with audio response

POST /agent/chat/{session_id} - Full voice agent conversation

GET / - Web interface

All endpoints return structured responses with proper error handling.

🔑 API Keys Setup
AssemblyAI (Speech-to-Text)
Sign up at AssemblyAI

Get your API key from the dashboard

Add to .env as AssemblyAI_API_KEY

Google Gemini (Language Model)
Visit Google AI Studio

Create a project and generate an API key

Add to .env as GOOGLE_API_KEY

Murf AI (Text-to-Speech)
Register at Murf AI

Subscribe to get API access

Add to .env as MURF_API_KEY

🚀 Development
Local Development:

bash
Copy code
uvicorn main:app --reload --host 0.0.0.0 --port 8000
Production:

bash
Copy code
uvicorn main:app --host 0.0.0.0 --port 8000
🎯 Recent Updates
Code Quality Improvements
✅ Pydantic Schemas - Added type safety with comprehensive validation models

✅ Service Architecture - Separated 3rd party integrations into dedicated service classes

✅ Code Cleanup - Removed unused imports, variables, and redundant code

✅ Frontend Optimization - Consolidated CSS, cleaned HTML structure, optimized JavaScript

✅ Error Handling - Improved error handling across all services and endpoints

✅ Production Ready - Optimized for deployment with proper configuration management

Architecture Benefits
Maintainability - Clean separation between API logic and service integrations

Testability - Service classes can be easily mocked and tested

Type Safety - Pydantic models prevent runtime errors and improve API documentation

Scalability - Modular design allows easy addition of new services

Reliability - Comprehensive error handling and graceful degradation

Made with ❤ by MdMohameenQureshi
