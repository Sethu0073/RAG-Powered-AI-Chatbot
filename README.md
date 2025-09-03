# RAG-Powered AI Chatbot

A Retrieval-Augmented Generation (RAG) chatbot built with **LangChain**, **Ollama**, and **LLaMA2** to deliver context-aware, knowledge-grounded responses via an interactive **Streamlit** interface.

---

## 🚀 Features

- **Retrieval-Augmented Generation (RAG):** Enhances accuracy by retrieving relevant context before generating responses.  
- **LangChain Orchestration:** Manages retrieval, prompt creation, and response generation seamlessly.  
- **Ollama + LLaMA2:** Runs LLaMA2 locally for efficient, on-device language model inference.  
- **Streamlit UI:** Interactive and responsive chat interface with document upload support.  
- **Flexible Knowledge Sources:** Accepts PDF uploads as a knowledge base.  

---

## 🛠️ Tech Stack

- **LLM Orchestration:** [LangChain](https://www.langchain.com/)  
- **Local LLM Serving:** [Ollama](https://ollama.com) (LLaMA2 models)  
- **Vector Search:** FAISS (or alternative vector stores)  
- **Embeddings:** OpenAI Embeddings / SentenceTransformers (configurable)  
- **Frontend:** Streamlit  
- **Language:** Python  

---

## ⚡ Getting Started

### 1. Prerequisites

- Python **3.8+**  
- [Ollama](https://ollama.com) installed and running locally  
- LLaMA2 model pulled (e.g., `ollama pull llama2`)  
- Adequate disk/memory for model storage  

---

### 2. Installation

Clone this repository:  
```bash
git clone https://github.com/Sethu0073/RAG-Powered-AI-Chatbot.git
cd RAG-Powered-AI-Chatbot
