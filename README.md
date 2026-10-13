# 📚 Multi-PDF RAG Chatbot

An end-to-end **Retrieval-Augmented Generation (RAG)** system designed to ingest, index, and query multiple PDF documents concurrently. The application addresses common LLM limitations—such as hallucinations and outdated information—by combining semantic vector search, sparse keyword matching (BM25), and neural reranking to deliver precise, context-grounded answers accompanied by exact page-level citations.

---

### 🌟 Key Features

* **Multi-PDF Document Processing:** Ingests and parses multi-page PDF files, splitting unstructured text into optimized overlapping passages using recursive character chunking.
* **Hybrid Retrieval Architecture:** Blends dense vector search (**ChromaDB**) with sparse keyword search (**BM25**) to maximize retrieval recall across technical terms, names, and precise phrases.
* **Cohere Neural Reranking:** Re-scores and filters retrieved document chunks using Cohere's Rerank API, ensuring only the highest-quality, most relevant passages are fed to the model context.
* **Conversational Memory:** Tracks multi-turn chat history to handle follow-up questions while maintaining document-grounded focus.
* **Source Attribution & Verification:** Extracts and displays precise metadata (document name, page number, and source snippet) alongside generated answers for complete traceability.
* **Interactive Web Interface:** Provides an intuitive **Streamlit** dashboard for drag-and-drop PDF uploads, indexing status monitoring, and real-time chat interactions.

---

### 🏗️ System Architecture

[ PDF Documents ] ──► [ Text Parsing & Chunking ] ──► [ Vector Store (ChromaDB) ]
│
[ User Query ] ─────► [ Hybrid Search (Dense + Sparse) ] ──► [ Cohere Neural Rerank ]
│
[ Grounded Answer + Page Citations ] ◄── [ LLM Generation ] ◄──┘
---

### 🛠️ Core Stack

* **Language & Frameworks:** Python, LangChain
* **Vector Store:** ChromaDB
* **Reranking & Search:** Cohere Rerank API, Rank-BM25
* **Frontend UI:** Streamlit
