# MedRAG – Intelligent Medical Question Answering System

MedRAG is an AI-powered **Retrieval-Augmented Generation (RAG) medical chatbot** that answers healthcare-related questions using knowledge extracted from medical documents.

The system combines **vector search and large language models** to retrieve relevant medical context and generate concise, context-aware responses.

---

# Overview

Large language models often hallucinate when asked domain-specific questions.
MedRAG solves this by using **retrieval-augmented generation**, where relevant medical documents are retrieved first and then provided to the language model for accurate responses.

The system processes medical PDFs, converts them into semantic embeddings, stores them in a vector database, and retrieves the most relevant information when a user asks a question.

---

# Features

• Retrieval-Augmented Generation for accurate answers
• Semantic search over medical documents
• Vector database powered by Pinecone
• Context-aware LLM responses
• Modular pipeline for scalable AI applications
• Flask-based conversational interface

---

# Key Highlights

* Processes **100+ pages of medical knowledge documents**
* Generates **384-dimensional semantic embeddings**
* Retrieves relevant knowledge using **vector similarity search**
* Returns concise answers with **context-aware LLM reasoning**

---

# Tech Stack

**Programming**

* Python

**AI / ML**

* LangChain
* HuggingFace Sentence Transformers
* OpenAI GPT-4o-mini

**Vector Database**

* Pinecone

**Backend**

* Flask

**Infrastructure Ready**

* Docker containerization
* Architecture compatible with cloud deployment

---

# Project Structure

```
Medical-Chatbot
│
├── Data/                # Medical knowledge PDFs
├── src/
│   ├── helper.py        # Document loading & embeddings
│   ├── prompt.py        # LLM prompt templates
│
├── templates/
│   └── chat.html        # Chat interface
│
├── store_index.py       # Vector index creation
├── app.py               # Flask application
├── requirements.txt
└── README.md
```

---

# Pipeline

### 1. Document Ingestion

Medical PDFs are loaded and processed.

### 2. Text Chunking

Documents are split into smaller context chunks for efficient retrieval.

### 3. Embedding Generation

Chunks are converted into vector embeddings using Sentence Transformers.

### 4. Vector Indexing

Embeddings are stored in Pinecone for fast similarity search.

### 5. Retrieval

Relevant document chunks are retrieved based on the user query.

### 6. LLM Response Generation

The retrieved context is passed to the OpenAI model to generate a final answer.

---

# Example Query

User Question:

```
What are the symptoms of diabetes?
```

System Response:

```
Common symptoms of diabetes include increased thirst, frequent urination, fatigue, and blurred vision. These symptoms occur due to high blood sugar levels affecting the body's normal metabolic processes.
```

---

# Future Improvements

* Add medical knowledge reranking for improved retrieval quality
* Integrate clinical datasets for broader coverage
* Implement user conversation memory
* Deploy using containerized cloud infrastructure
* Add monitoring and evaluation for RAG performance

---

# License

This project is for educational and research purposes.
