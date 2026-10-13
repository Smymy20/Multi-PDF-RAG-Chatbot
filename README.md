# 📚 Multi-PDF RAG Chatbot

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![LangChain](https://img.shields.io/badge/LangChain-Framework-000000?style=for-the-badge&logo=chainlink&logoColor=white)](https://www.langchain.com/)
[![ChromaDB](https://img.shields.io/badge/Vector%20Store-ChromaDB-FF6F61?style=for-the-badge)](https://www.trychroma.com/)
[![Cohere](https://img.shields.io/badge/Rerank-Cohere-390099?style=for-the-badge)](https://cohere.com/)
[![Streamlit](https://img.shields.io/badge/UI-Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

An production-grade **Retrieval-Augmented Generation (RAG)** application built to query multiple PDF documents concurrently. The system mitigates hallucinations by combining dense vector retrieval, sparse keyword matching (BM25), and neural reranking—delivering precise, context-grounded responses complete with source citations.

---

## 🌟 Key Features

* **Multi-PDF Ingestion & Chunking:** Dynamically load, parse, and split multi-page PDF documents into optimized overlapping chunks using `RecursiveCharacterTextSplitter`.
* **Hybrid Retrieval Strategy:** Merges semantic similarity search (**ChromaDB**) with exact keyword matching (**BM25**) for high-recall document fetching.
* **Cohere Neural Reranking:** Re-scores and filters retrieved contexts using Cohere’s Rerank API to pass only the most relevant passages to the LLM.
* **Conversational Memory:** Tracks multi-turn dialogue context while filtering context using dynamic metadata constraints.
* **Source Attribution & Grounding:** Provides clear page-level citations and text snippets for full verification of generated answers.
* **Interactive Dashboard:** Built with **Streamlit** for real-time PDF processing, dynamic uploads, and multi-turn chat interaction.

---

## 🏗️ System Architecture
