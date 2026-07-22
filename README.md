# 🤖 Agentic RAG Model with Web Search

An advanced **Agentic Retrieval-Augmented Generation (RAG)** system that combines **LLMs, intelligent agents, web search, document retrieval, validation, and analytics** to produce accurate, explainable, and evidence-backed responses.

The system uses a multi-agent architecture where each agent is responsible for a specific task such as planning, retrieval, research, validation, analytics, and answer generation.

![Application Screenshot](agentic%ai.png)
---

## ✨ Features

- 🤖 Multi-Agent Agentic AI Workflow
- 🌍 Real-time Web Search (SerpAPI & DuckDuckGo)
- 📚 Retrieval-Augmented Generation (FAISS + Sentence Transformers)
- 🔍 Automatic Source Tracking
- ✅ Evidence Credibility Validation
- 📈 Analytics & Insight Generation
- 💾 Session and Output Saving
- 🌐 Flask Web Interface
- ⚡ Powered by Groq Llama 3.3 70B
- 🧩 Modular Architecture
- 📄 Report Generation Support

---

# 🏗 Architecture

```
                          User Query
                               │
                               ▼
                      Web Interface (Flask)
                               │
                               ▼
                           main.py
                               │
                               ▼
                     Supervisor Agent
                               │
      ┌───────────────┬───────────────┬──────────────┐
      ▼               ▼               ▼              ▼
 Research Agent   Retrieval Agent  Discovery    Analytics
      │               │             Agent         Agent
      ▼               ▼               │              │
 SerpAPI / DDG    FAISS Retriever     │              │
      │               │               │              │
      └──────┬────────┴───────┬───────┘              │
             ▼                ▼                      ▼
      Source Tracker   Credibility Checker     Insights
             │                │
             └────────┬───────┘
                      ▼
               Validation Agent
                      │
                      ▼
                 Answer Agent
                      │
                      ▼
               Final Response
```

---

# 📂 Project Structure

```text
agentic-rag/
│
├── agents/
│   ├── analytics.py
│   ├── answer.py
│   ├── discovery.py
│   ├── fallback.py
│   ├── research.py
│   ├── retrieval.py
│   ├── supervisor.py
│   ├── validation.py
│   └── __init__.py
│
├── config/
│   ├── settings.py
│   └── __init__.py
│
├── core/
│   ├── llm.py
│   ├── pipeline.py
│   ├── saver.py
│   ├── state.py
│   ├── SL_Outboard_Analysis_20260702_051400 (1).docx
│   └── __init__.py
│
├── tools/
│   ├── credibility.py
│   ├── ddg_search.py
│   ├── retriever.py
│   ├── search_cache.py
│   ├── serp_search.py
│   ├── source_tracker.py
│   └── __init__.py
│
├── web/
│   ├── app.py
│   ├── static/
│   │   └── style.css
│   └── templates/
│       └── index.html
│
├── main.py
├── view_outputs.py
├── requirements.txt
├── README.md
├── .env
└── new apis.txt
```

---

# ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/yourusername/agentic-rag.git

cd agentic-rag
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# 🔑 Environment Variables

Create a file named **`.env`** in the project root.

```dotenv
# Groq API Key
GROQ_API_KEY=your_api_key

# SerpAPI Key
SERP_API_KEY=your_api_key

# Groq Model
GROQ_MODEL=llama-3.3-70b-versatile

# Search Settings
MAX_SEARCH_RESULTS=15

# RAG Settings
TOP_K_CHUNKS=100

# Confidence Threshold
CONFIDENCE_THRESHOLD=0.7
```

---

# ▶ Running the Project

```bash
python main.py
```

---

## 🔄 Workflow

1. User submits a question through the Flask web interface.
2. The Supervisor Agent determines the execution plan.
3. Research Agent performs web searches using SerpAPI and DuckDuckGo.
4. Retrieval Agent retrieves relevant documents from the FAISS vector store.
5. Discovery Agent identifies additional related knowledge.
6. Analytics Agent generates insights and calculations.
7. Credibility and Source Tracker evaluate evidence quality.
8. Validation Agent verifies retrieved information.
9. Answer Agent generates the final response.
10. Results are saved and presented to the user.

---

# 📦 Output

The system automatically stores:

```
outputs/
│
├── analytics/
├── evidence/
├── runs/
└── sessions/
```

---

# 🛠 Technologies Used

- Python 3.10+
- LangGraph
- LangChain
- Groq API
- SerpAPI
- Sentence Transformers
- FAISS
- Rank-BM25
- Pydantic
- Rich
- Pandas
- NumPy
- Scikit-learn

---

# 🚀 Future Improvements

- PDF RAG
- Excel RAG
- SQL Database RAG
- Multi-modal RAG
- Image Understanding
- GraphRAG Integration
- Local LLM Support
- Streaming Responses
- Docker Deployment
- Kubernetes Support

---

# 📄 License

This project is released under the MIT License.

---

# 👨‍💻 Author

**Darshana Wijesingha**

Master's Student in Business Analytics  
University of Colombo School of Computing

GitHub:
https://github.com/darshanawijesingha

---

## ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.
