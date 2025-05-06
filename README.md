# Project Documentation: RimalAI - Saudi Culture & Heritage Chatbot 🌟

## 1. Project Goal and Architecture 🎯

### Goal 🚀
**RimalAI** is an intelligent conversational agent designed to provide information about Saudi Arabian landmarks, Vision 2030 initiatives, cultural heritage, and Arabic poetry. The system integrates cutting-edge technologies like **Natural Language Processing (NLP)**, **Speech Recognition**, **Text-to-Speech**, and **Image Generation** to deliver an interactive and multimedia-rich user experience. 

### Architecture 🏗️
The system follows a modular architecture with the following key components:

#### Data Processing & Embeddings 📊
- Loads structured JSON datasets (`Rimal_AI_Lastdataset.json`, `arabic_poems_Lastdataset.json`).
- Combines relevant fields (e.g., descriptions, metadata) and generates embeddings using **Sentence Transformers** (`all-MiniLM-L6-v2`).
- Stores embeddings in **FAISS** for efficient similarity search.

#### Language Model (LLM) & QA System 🤖
- Uses **OpenAI’s GPT-4o** for generating intelligent responses.
- Implements a **RetrievalQA** chain to fetch context-aware answers from the **FAISS** vector store.

#### Multimedia Tools 🎥🎤
- **Text-to-Speech (TTS)**: Utilizes **gTTS** for Arabic/English voice responses.
- **Speech Recognition**: Leverages **pvrecorder** and **speech_recognition** for voice input.
- **Image Generation**: Uses **DALL-E 3** to create culturally relevant images.
- **Poem Generation**: Custom prompts for generating Arabic poetry, including translations.

#### Agent Orchestration 🔧
- Uses **LangChain’s OpenAI Functions Agent** to dynamically select tools (QA, TTS, image/poem generation) based on user queries.

#### User Interaction 👥
- Supports both text and voice input/output with language detection (via **langid**), allowing for a smooth interaction in Arabic and English.

## 2. Methodology 🧑‍🔬

### Development Process 🛠️

#### Data Preparation 📂
- Combined structured JSON datasets into a unified format.
- Extracted key fields (e.g., descriptions, metadata) for embedding generation.

#### Embedding & Retrieval 🔍
- Used **HuggingFace’s Sentence Transformers** to generate embeddings.
- Stored embeddings in **FAISS** for fast similarity search and retrieval.

#### Model Integration 🧠
- Fine-tuned **GPT-4o** for generating context-aware responses.
- Implemented **RetrievalQA** to fetch relevant passages from **FAISS**.

#### Tool Integration 🔌
- Integrated **gTTS** for TTS and **pvrecorder** for speech recognition.
- Incorporated **DALL-E 3** to generate culturally relevant images.

#### Testing & Validation ✅
- Tested QA accuracy with a variety of sample queries.
- Validated voice interaction and multimedia outputs to ensure smooth user experience.

## 3. Setup ⚙️

### Requirements 📋
- Python 3.9+  
- Libraries (see `requirements.txt` below for full list)

### Installation 🖥️
Clone the repository:

```bash
pip install -r requirements.txt
```

Set up environment variables (.env):
```bash
OPENAI_API_KEY=your_openai_key
MAPBOX_API_KEY=your_mapbox_key
GOOGLE_SEARCH_API_KEY=your_google_key
```

### 4. **🔮** future improvements.
- Expand dataset coverage (include more landmarks and poems).
- Optimize FAISS retrieval speed for faster query responses.
- Add real-time translation support for better multilingual interaction.


نسخ
تحرير
