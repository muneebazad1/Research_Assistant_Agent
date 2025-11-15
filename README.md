# 🧠 AgenticRAG-ResearchHelper (ongoing)

An **Agentic Retrieval-Augmented Generation (RAG)** system for academic and scientific research assistance.  
This project aims to build a **Research Helper Agent** that allows users to upload their papers, query them, and optionally perform web-based knowledge expansion — all within an intelligent, modular agentic workflow.

---

## 🚀 Project Overview

**Goal:**  
To build an AI-powered *Research Assistant* that can:
- Retrieve and summarize insights from uploaded research papers.
- Perform real-time web searches for complementary context.
- Generate structured academic explanations.
- Eventually provide an interactive UI with FastAPI (backend) and Streamlit (frontend).

---

## 🗓️ Development Timeline

### **Day 1**
**Progress:**  
✅ Implemented a basic RAG agent workflow in Google Colab using 3 core tools:


---

### **Day 2**
**Progress:**
Today, a full **Data Ingestion Pipeline** was implemented and an advanced workflow was added, enabling seamless integration of **web search → ingestion → vector storage**.

---

### **Day 3**
**Progess:**
Build the Research & Analysis Agent which does analysis of provided data using intelligent tools and also answer queries of users using RAG pipeline



---

## 🧩 Planned Architecture

      ┌────────────────────┐
      │   Streamlit UI     │
      └────────┬───────────┘
               │ REST API
      ┌────────▼───────────┐
      │    FastAPI Backend │
      └────────┬───────────┘
               │
      ┌────────▼───────────┐
      │  Agentic RAG Core  │
      │ (LangChain + Tools)│
      └────────┬───────────┘
               │
 ┌─────────────┴──────────────┐
 │        Vector Store         │
 │      (FAISS / Chroma)       │
 └─────────────────────────────┘


---

## 🧠 Tech Stack

| Component | Technology |
|------------|-------------|
| LLM Backend | Gemini,DeepSeek |
| Framework | LangChain |
| Vector Store | Chroma |
| Web Search | DuckDuckGo Search (DDGS) |
| Frontend | Streamlit |
| Backend | FastAPI |
| Additional Models | SentenceTransformer, SciBERT, NLI models (planned) |

---

## 🤝 Contributions
Since this is an **ongoing self-learning project**, contributions and feedback are welcome.  
The project will evolve daily, and the README will be updated as progress is made.

---

## 📅 Logs
**Day 1:** Initial Colab workflow with 2 functional tools + 1 planned.  
**Day 2:** Implemented Automatic ETL Pipeline which included Data Orchestration Agent and its supported Tools.
**Day 3:** Implemented Base R&A Agent which will take the ingested Data and provide the research and further analysis based on intelligent Tools.


---

## 📜 License
MIT License — free for educational and research use.
