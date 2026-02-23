# 🧠 MeetingMind AI

> **Intelligent Meeting Processing Platform** — Transform meeting recordings into structured knowledge and searchable organizational memory.

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-009688?style=flat&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![Whisper](https://img.shields.io/badge/OpenAI-Whisper-412991?style=flat&logo=openai&logoColor=white)](https://openai.com/research/whisper)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## ❗ Problem Statement

Modern teams spend significant time in meetings, yet critical information — decisions, action items, and key insights — frequently gets lost or requires tedious manual documentation. Existing tools provide transcription but lack structured intelligence extraction and contextual search across meetings.

There is a clear need for an AI-powered system that automatically converts meeting recordings into structured knowledge and enables teams to retrieve insights efficiently.

---

## 💡 Solution Overview

MeetingMind AI is a backend platform that acts as an AI-powered organizational memory engine. It automatically:

- 🎙️ Converts meeting audio into accurate transcripts
- 📋 Generates concise, structured summaries
- ✅ Extracts action items, owners, and decisions
- 🗄️ Stores knowledge for future retrieval
- 🔍 Enables natural-language queries across all past meetings

---

## 🏗️ System Architecture

```
┌────────────┐     ┌──────────────┐     ┌───────────────────┐
│   Client   │────▶│  FastAPI     │────▶│  Audio Processing │
│  (Upload)  │     │  Backend     │     │  (Whisper STT)    │
└────────────┘     └──────────────┘     └─────────┬─────────┘
                                                   │
                                                   ▼
                                        ┌───────────────────┐
                                        │    AI Models      │
                                        │  Summarization    │
                                        │  Extraction       │
                                        │  Embeddings       │
                                        └─────────┬─────────┘
                                                   │
                          ┌────────────────────────┤
                          ▼                        ▼
               ┌──────────────────┐    ┌───────────────────┐
               │   PostgreSQL /   │    │   Vector DB       │
               │   SQLite         │    │ (Chroma/Pinecone) │
               └──────────────────┘    └───────────────────┘
                          │
                          ▼
               ┌──────────────────┐
               │   Insights API   │
               │  (Search, Query) │
               └──────────────────┘
```

---

## 📦 Requirements

| Category | Technology |
|---|---|
| **Language** | Python 3.10+ |
| **Framework** | FastAPI |
| **Speech Recognition** | OpenAI Whisper |
| **NLP / Summarization** | Hugging Face Transformers |
| **Semantic Search** | Sentence Transformers |
| **Relational DB** | PostgreSQL / SQLite |
| **Vector DB** | Chroma / Pinecone |
| **Infrastructure** | Docker, AWS / GCP (optional) |
| **Other** | FFmpeg (audio processing) |

---

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

<div align="center">

**Built with ❤️ to make meetings actually useful.**

[⭐ Star this repo](https://github.com/your-username/meetingmind-ai) · [🐛 Report a Bug](https://github.com/your-username/meetingmind-ai/issues)

</div>
