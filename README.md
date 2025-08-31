# 🎙️ Voice AI Agent – Project Plan (MVP)

This document describes the requirements, roadmap, and setup steps for building a **Voice AI Agent** using **FastAPI (backend)** and **React (frontend)** with **OpenAI services (Whisper, GPT-4o-mini, TTS)**.  
The goal is to create an MVP voice assistant that supports **real-time conversation**.

---

## 🔹 Project Requirements

### Functional
1. Real-time voice conversation with the AI agent.
2. Speech-to-Text (ASR) for user input.
3. Text generation with LLM (GPT-4o-mini).
4. Text-to-Speech (TTS) for AI voice response.
5. Streaming responses (live transcription + audio).
6. WebRTC support for audio input/output.
7. React UI:
   - Microphone button (start/stop).
   - Live transcript subtitles.
   - Audio playback of AI voice.

### Non-functional
- Low latency (< 2 seconds).
- Easy local setup for prototyping.
- Free-tier/trial services (no costs).

---

## 🔹 Tech Stack

- **Backend**: FastAPI + Pipecat pipeline
- **Frontend**: React + WebRTC
- **ASR (Speech-to-Text)**: OpenAI Whisper API
- **LLM**: OpenAI GPT-4o-mini
- **TTS**: OpenAI TTS (or ElevenLabs for voice variety)
- **Infra**: Docker (optional), HTTPS (future)

---

## 🔹 Accounts & Setup

### 1. OpenAI
- Sign up at [OpenAI](https://platform.openai.com/).
- Get your **API Key**: [API Keys](https://platform.openai.com/account/api-keys).
- Free trial credits included.

APIs used:
- **ASR (Whisper)** → `audio.transcriptions`
- **LLM (GPT-4o-mini)** → `chat.completions` (supports streaming)
- **TTS** → `audio.speech.create`

---

### 2. ElevenLabs (Optional – for better voices)
- Sign up at [ElevenLabs](https://elevenlabs.io/).
- Get your **API Key** in your profile.
- Free plan: 10,000 characters per month.
- Endpoint:  
  `https://api.elevenlabs.io/v1/text-to-speech/{voice_id}`

---


## 🔹 Checklist (MVP)

- [Done] Register OpenAI → get API Key  
- [Done] Register ElevenLabs → get API Key  
- [Done] Build FastAPI endpoints (`/transcribe`, `/chat`, `/tts`)  
- [ ] Integrate Whisper (ASR)  
- [ ] Integrate GPT-4o-mini (LLM)  
- [ ] Integrate TTS (OpenAI/ElevenLabs)  
- [ ] Create React component `VoiceAgent`  
- [ ] Implement WebRTC audio stream  
- [ ] Test full cycle: speech → AI response → voice output  

---

## 🔹 Next Steps (after MVP)

- Session handling (conversation history per user).  
- RAG (Retrieval-Augmented Generation) with external documents.  
- Embeddings + vector database (pgvector, Weaviate).  
- Multi-user sessions with scaling.  
- Deploy with HTTPS.  

---

