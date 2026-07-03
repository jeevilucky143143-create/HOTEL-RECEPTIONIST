# ProjectVoiceBot 🎤🤖

A sophisticated voice-enabled AI assistant that combines speech-to-text, large language model processing, and text-to-speech capabilities to create a seamless conversational experience.

## 🌟 Features

- **🎤 Voice Input**: Real-time audio recording with microphone support
- **🗣️ Speech-to-Text**: Powered by Deepgram's Nova-2 model for accurate transcription
- **🧠 AI Processing**: Llama 3.1 70B model for intelligent responses via Hugging Face
- **🔊 Text-to-Speech**: ElevenLabs integration for natural voice synthesis
- **💬 Conversation Memory**: Maintains context across conversation sessions
- **🎨 Modern UI**: Clean, responsive web interface with real-time visual feedback
- **⚡ Fast Performance**: Optimized backend with detailed performance logging

## 🏗️ Architecture

```
Frontend (HTML/CSS/JS) ←→ Backend (FastAPI) ←→ External APIs
    ↓                           ↓                    ↓
Voice Recording           Speech Processing      Deepgram STT
Chat Interface           LLM Integration       Llama 3.1 70B
Audio Playback          TTS Generation        ElevenLabs TTS
```

## 🚀 Quick Start

### Prerequisites

- Python 3.8+
- Node.js (for serving frontend)
- Microphone access
- API keys for external services

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd ProjectVoiceBot
```

### 2. Set Up Virtual Environment

```bash
# Create virtual environment
python -m venv botenv

# Activate virtual environment
# Windows
botenv\Scripts\activate
# macOS/Linux
source botenv/bin/activate
```

### 3. Install Dependencies

```bash
cd backend
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file in the `backend` directory:

```env
DEEPGRAM_API_KEY=your_deepgram_api_key_here
ELEVENLABS_API_KEY=your_elevenlabs_api_key_here
```

**Note**: The Hugging Face token is automatically loaded from your Cursor MCP configuration.

### 5. Start the Backend

```bash
cd backend
uvicorn main:app --reload --host 127.0.0.1 --port 8000
```

### 6. Serve the Frontend

```bash
cd frontend
# Using Python's built-in server
python -m http.server 8080

# Or using Node.js http-server
npx http-server -p 8080
```

### 7. Open Your Browser

Navigate to `http://localhost:8080` and grant microphone permissions when prompted.

## 🔧 Configuration

### API Keys Required

1. **Deepgram API Key**: For speech-to-text transcription
   - Sign up at [Deepgram](https://deepgram.com/)
   - Get your API key from the dashboard

2. **ElevenLabs API Key**: For text-to-speech synthesis
   - Sign up at [ElevenLabs](https://elevenlabs.io/)
   - Get your API key from the dashboard

3. **Hugging Face Token**: For Llama 3.1 70B access
   - Automatically configured via Cursor MCP
   - Ensure you have access to the Llama 3.1 70B model

### Model Configuration

- **STT Model**: Deepgram Nova-2 (16kHz, mono audio)
- **LLM Model**: Meta Llama 3.1 70B via Hugging Face
- **TTS Model**: ElevenLabs Monolingual v1 with "Bill" voice

## 📱 Usage

### Voice Interaction

1. **Click the microphone button** to start recording
2. **Speak your question or request** clearly
3. **Click again to stop recording** and process your audio
4. **Listen to the AI response** as it's synthesized and played back

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.


