# 🎥 AI Video Assistant

An AI-powered application that transforms video content into meaningful, structured information. Simply provide a YouTube video URL or upload an audio file to generate transcripts, summaries, action items, key decisions, and answers to questions about the content.

🔗 **Live Demo:** [Try AI Video Assistant](YOUR_LIVE_APP_LINK)

---

## ✨ Features

- **Video & Audio Processing:** Extract audio from YouTube videos and process audio files.
- **AI Transcription:** Convert audio into text using OpenAI Whisper.
- **AI-Powered Summarization:** Generate concise and meaningful summaries using Groq LLMs.
- **Automatic Title Generation:** Generate relevant titles based on video content.
- **Action Item Extraction:** Identify tasks and actionable points discussed in the content.
- **Key Decision Extraction:** Automatically identify important decisions.
- **Question Extraction:** Extract important questions from conversations or discussions.
- **AI Chat with Video:** Ask questions about the processed content using Retrieval-Augmented Generation (RAG).

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Frontend | Streamlit |
| Speech Recognition | OpenAI Whisper |
| LLM Provider | Groq |
| Speech API | Sarvam AI |
| LLM Framework | LangChain |
| Vector Database | ChromaDB |
| Embeddings | Hugging Face |
| Audio Processing | Pydub, FFmpeg |
| Video/Audio Download | yt-dlp |

## 🏗️ Project Architecture

```text
AI-Video-Assistant/
│
├── app.py
├── main.py
├── requirements.txt
├── packages.txt
│
├── core/
│   ├── transcriber.py
│   ├── summarize.py
│   ├── extractor.py
│   ├── vector_store.py
│   └── rag_engine.py
│
└── utils/
    └── audio_processor.py
```

## ⚙️ How It Works

1. **Input:** Provide a YouTube video URL or an audio file.
2. **Audio Extraction:** Extract audio from the video using yt-dlp.
3. **Transcription:** Convert audio into text using Whisper and the configured transcription services.
4. **Content Analysis:** Use Groq-powered language models to generate summaries, titles, action items, key decisions, and questions.
5. **Vectorization:** Split the transcript into chunks and generate embeddings using Hugging Face.
6. **Storage:** Store the embeddings in ChromaDB.
7. **Question Answering:** Retrieve relevant transcript sections and generate contextual answers using RAG.

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/JugalGhelani/AI-Video-Assistant.git
cd AI-Video-Assistant
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it:

**macOS / Linux**
```bash
source venv/bin/activate
```

**Windows**
```bash
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

Install FFmpeg separately if it is not already installed.

**macOS**
```bash
brew install ffmpeg
```

**Ubuntu / Debian**
```bash
sudo apt install ffmpeg
```

### 4. Configure Environment Variables

Create a `.env` file in the root directory:

```env
GROQ_API_KEY=your_groq_api_key
SARVAM_API_KEY=your_sarvam_api_key
```

Get your API keys:

- [Groq Console](https://console.groq.com/)
- [Sarvam AI](https://dashboard.sarvam.ai/)


### 5. Run the Application

**Streamlit Web Application**
```bash
streamlit run app.py
```

**Command-Line Application**
```bash
python main.py
```

## 🧠 RAG Implementation

The application uses Retrieval-Augmented Generation to answer questions based on the processed video content.

The RAG pipeline includes:

- Transcript chunking
- Text embedding generation
- Vector storage using ChromaDB
- Similarity-based document retrieval
- Context-aware answer generation using Groq

This helps the application provide answers grounded in the video transcript rather than relying only on the language model's general knowledge.

## 🔐 Environment Variables

| Variable | Description |
|---|---|
| `GROQ_API_KEY` | API key for Groq language models |
| `SARVAM_API_KEY` | API key for Sarvam AI services |
| `WHISPER_MODEL` | Optional Whisper model selection |

## 📌 Future Improvements

- Support for additional video platforms.
- Multilingual transcription and summarization.
- Downloadable transcripts and summaries.
- Export reports in PDF format.
- Improved conversation history and session management.
- More advanced RAG retrieval and response evaluation.

## 👨‍💻 Author

**Jugal Ghelani**

- GitHub: [@JugalGhelani](https://github.com/JugalGhelani)
- Live Link: https://ai-video-assistant-hfu2vbvgapptujecp9uhvj9.streamlit.app/

---

⭐ If you find this project useful, consider giving it a star!
