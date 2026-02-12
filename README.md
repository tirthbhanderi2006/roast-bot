# 🔥 RoastBot

RoastBot is a RAG-based AI chatbot that delivers savage, personalized burns using a local knowledge base and NVIDIA NIM.

## 🏗️ Architecture

```
User Input → RAG Retrieval (FAISS) → Context + Prompt → NVIDIA NIM (LLaMA 3.1) → Savage Roast
```

- **RAG Pipeline:** Chunks roast data → Embeds with SentenceTransformer → Stores in FAISS → Retrieves relevant context per query
- **LLM:** NVIDIA NIM (Meta LLaMA 3.1 8B Instruct) via OpenAI-compatible API
- **Memory:** Conversation history for context-aware follow-up roasts
- **UI:** Streamlit chat interface

## 🚀 Setup

```bash
cd roastbot-challenge
pip install -r requirements.txt
```

Create a `.env` file:

```
NVIDIA_API_KEY=your_nvidia_api_key_here
```

> Get a free API key at: https://build.nvidia.com/

Run the bot:

```bash
streamlit run app.py
```

## 📁 Files You Can Edit

```
roastbot-challenge/
├── .gitignore          # Git ignore rules for local/dev artifacts
├── app.py              # Main Streamlit app + NVIDIA NIM integration
├── rag.py              # RAG pipeline (FAISS + SentenceTransformer)
├── prompt.py           # System prompt for roasting
├── memory.py           # Conversation history management
├── requirements.txt    # Python dependencies
└── data/
    └── roast_data.txt  # Roast knowledge base
```

