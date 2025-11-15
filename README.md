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
1. `retrieve_context` → retrieves most relevant chunks from uploaded research papers.  
2. `web_search_tool` → performs real web search using DuckDuckGo.  
3. `web_image_link_tool` →  fetch relevant links and images from the web relavant to query.  

**Current Features:**
- Simple command-line interaction loop.  
- Option for the user to choose between *Context Retrieval* or *Web Search*.  
- LLM integration for producing structured, academic-style responses.  

---

### **Day 2**
**Progress:**
Today, a full **Data Ingestion Pipeline** was implemented and an advanced workflow was added, enabling seamless integration of **web search → ingestion → vector storage**.

## 🔥 Core Additions Today

1)SmartLoader
- Automatically handles **PDFs, text files, and URLs**  
- Downloads PDFs when needed  
- Normalizes all input into a unified text format  

2)Chunking Function
- Uses `RecursiveCharacterTextSplitter`  
- Creates clean, consistent, RAG-optimized chunks  

3)Embedding Function
- Uses **HuggingFaceEmbeddings** (`all-MiniLM-L6-v2`)  
- Fast, lightweight, high-quality embeddings  

4)Chroma Vector Store Setup
- Stores embeddings **persistently**  
- Enables future RAG queries directly on saved vector DB  

5)data_ingestion_workflow` Tool
An end-to-end ingestion pipeline that:
1. Loads files or URLs  
2. Splits text into chunks  
3. Generates embeddings  
4. Saves vectors into ChromaDB  
5. Prints step-by-step logs for debugging  

6)search_to_ingestion Workflow
A newly added workflow that:
- Takes selected URLs from the **interactive web search tool**  
- Automatically feeds them into the ingestion pipeline  
- Builds a **real-time, always-fresh vector database** from live search results  
This turns web search into an **automated data ingestion → RAG-ready** pipeline.  

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
*Next update: Day 2 → Integrate hybrid ML tools (keyword extraction, concept clustering).*

---

## 📜 License
MIT License — free for educational and research use.
