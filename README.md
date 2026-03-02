<div align="center">
 
![logo](assets/logo_rounded.png)

<h1 align="center"><strong>⚕️ Multi-Agent Medical Assistant</strong></h1>
<h4 align="center">Production-Oriented Multi-Agent AI System for Medical Q&A, Research Retrieval & Diagnostic Assistance</h4>

![Python](https://img.shields.io/badge/Python-3.11+-blue?style=for-the-badge&logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-0.3+-teal?style=for-the-badge)
![LangChain](https://img.shields.io/badge/LangChain-0.3+-teal?style=for-the-badge)
![Qdrant](https://img.shields.io/badge/Qdrant-1.13+-red?style=for-the-badge)
![FastAPI](https://img.shields.io/badge/FastAPI-0.115+-teal?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-Enabled-blue?style=for-the-badge&logo=docker)

</div>

---

## 📌 Overview

This project is a **production-oriented Multi-Agent AI Healthcare System** built to handle:

- 🩺 Medical Question Answering  
- 📚 Research Paper Retrieval with RAG  
- 🖼️ Medical Image Analysis (CV Models)  
- 🌐 Real-time Web Search for Updated Medical Knowledge  

Unlike a basic chatbot, this system uses **agent orchestration with LangGraph**, enabling multiple specialized agents to collaborate through structured workflows.

This project demonstrates practical implementation of:

- Multi-Agent System Design
- Retrieval-Augmented Generation (RAG)
- Hybrid Search (Sparse + Dense Retrieval)
- Semantic Chunking with Structural Awareness
- Confidence-Based Agent Routing
- Guardrails for Safe Medical Responses
- Human-in-the-Loop Validation
- Production Deployment using Docker

---

## 🧠 System Architecture

The system follows a graph-based orchestration model:

1. User Query → Router Agent  
2. Medical Reasoning Agent OR RAG Agent OR Web Search Agent  
3. Confidence Scoring  
4. Agent-to-Agent Handoff (if required)  
5. Final Verified Response  

The architecture ensures:
- Reduced hallucination
- Controlled reasoning flow
- Modular extensibility
- Production scalability

---

## ✨ Key Features

### 🤖 Multi-Agent Architecture
Task-specialized agents coordinated using **LangGraph workflows**.

### 🔍 Advanced RAG Pipeline
- Document parsing using **Docling**
- Markdown-based structured extraction
- LLM-driven semantic chunking
- Query expansion with domain-specific medical terminology
- Hybrid Retrieval:
  - Dense embeddings
  - BM25 sparse keyword search
- Cross-Encoder reranking (HuggingFace)
- Source citation links in responses

### 🏥 Medical Imaging Module
- Chest X-ray Classification
- Skin Lesion Segmentation
- Brain Tumor Detection (Pipeline Ready)

### 🌐 Real-Time Web Search Agent
Fallback mechanism when RAG confidence is low.

### 📊 Confidence-Based Routing
Log probability & retrieval confidence used to decide:
- Whether to answer
- Whether to reroute
- Whether to trigger web search

### ⚔️ Guardrails
Input and output validation to prevent:
- Unsafe medical suggestions
- Hallucinated facts
- Non-medical drift

### 👨‍⚕️ Human-in-the-Loop
Designed to allow medical professional review before final diagnosis output.

---

## 🛠️ Technology Stack

| Layer | Technologies |
|-------|-------------|
| Backend | FastAPI |
| Agent Orchestration | LangGraph + LangChain |
| Vector Database | Qdrant |
| Embeddings | Gemini / OpenAI / Compatible LLM |
| Document Parsing | Docling |
| Reranking | HuggingFace Cross Encoder |
| CV Models | PyTorch |
| Web Search | Tavily API |
| Voice | ElevenLabs |
| Deployment | Docker |

---

## 🚀 Installation

### Option 1 — Docker (Recommended)

```bash
git clone <your-repo-link>
cd Multi-Agent-Medical-Assistant
