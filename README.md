# Clinical-Intelligence-System

## Problem Statement

Modern healthcare professionals struggle to keep up with rapidly growing medical literature, making it difficult to access accurate and context-relevant clinical information. Traditional keyword-based tools fail to handle complex medical queries effectively. This project aims to build a Clinical Intelligence System using RAG to deliver precise, trustworthy, and context-grounded medical answers

## Approach

- Built a Clinical Q&A RAG system: created langchain.Documents for the data, generated embeddings via Azure OpenAl and persisted them in ChromaDB for fast vector retrieval.
- Explored multi-retrieval strategies: implemented semantic search and a hybrid retriever (semantic BM25) and capped Top-K s 3 for precision.
- Improved evidence quality with GPT reranking: prompted a lightweight ranking head to reorder retrieved chunks and fed the top evidence into an instruction-tuned prompt to ground answers strictly in context (explicit fallback when unsupported).
- Evaluation: measured Contextual Precision/Recall, Answer Relevancy, Faithfulness, Hallucination with DeepEval.
