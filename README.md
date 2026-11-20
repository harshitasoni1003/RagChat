# Chat With Your Documents — Retrieval-Augmented Generation (RAG)

An end-to-end Retrieval-Augmented Generation (RAG) document Q&A system built with Python, ChromaDB, PyPDF, Pydantic, and the official `google-genai` SDK.

## Architecture Pipeline
`Document (.pdf / .txt / .md)` -> `Overlapping Text Chunking` -> `Dense Embeddings (gemini-embedding-001)` -> `Vector DB (ChromaDB Cosine HNSW)` -> `Top-K Similarity Retrieval` -> `Grounded Gemini LLM` -> `Cited JSON Answer`

## Modules Implemented
1. **Hallucination vs. Grounded RAG:** Empirical comparison between ungrounded generation and context-grounded answering.
2. **Document Processing & Embeddings:** PDF/TXT extraction, overlapping chunking, dense vector embeddings, and cosine similarity verification.
3. **Retrieval Quality Optimization:** Top-K retrieval with cosine distance threshold filtering and strict schema citations.
4. **Chat With Your Documents:** Modular `ChatWithDocuments` class and interactive Google Colab lab notebook.

## Quick Start
```bash
pip install -r requirements.txt
export GEMINI_API_KEY="your_api_key"
python src/chat_with_docs.py
```
