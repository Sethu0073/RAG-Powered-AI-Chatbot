# RAG-Powered AI Chatbot

A Retrieval-Augmented Generation (RAG) chatbot built with **LangChain**, **Ollama**, and **LLaMA2** to deliver context-aware, knowledge-grounded responses via an interactive **Streamlit** interface.

---

## 🚀 Features

- **Retrieval-Augmented Generation (RAG):** Enhances accuracy by retrieving relevant context before generating responses.  
- **LangChain Orchestration:** Manages retrieval, prompt creation, and response generation seamlessly.  
- **Ollama + LLaMA2:** Runs LLaMA2 locally for efficient, on-device language model inference.  
- **Streamlit UI:** Interactive and responsive chat interface with document upload support.  
- **Flexible Knowledge Sources:** Accepts PDF uploads as a knowledge base.

## 🧠 How It Works

This chatbot uses the following workflow:

1.  **Document Ingestion:** Documents in the `data` directory are loaded and parsed.
2.  **Text Chunking:** The documents are split into smaller, manageable chunks of text.
3.  **Vector Embeddings:** Each chunk is converted into a numerical representation (embedding) using a sentence transformer model.
4.  **Vector Store:** The embeddings are stored in a FAISS vector store for efficient similarity search.
5.  **User Query:** When a user asks a question, the query is also converted into an embedding.
6.  **Similarity Search:** The vector store is searched for the most similar text chunks to the user's query.
7.  **LLM Augmentation:** The user's query and the retrieved text chunks are passed to a large language model (LLM).
8.  **Response Generation:** The LLM generates a response based on the provided context, which is then displayed to the user.

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

## 🛠️ Installation

2.  **Clone the repository:**

    ```bash
    git clone [https://github.com/Sethu0073/RAG-Powered-AI-Chatbot.git](https://github.com/Sethu0073/RAG-Powered-AI-Chatbot.git)
    cd RAG-Powered-AI-Chatbot
    ```

3.  **Create a virtual environment:**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

4.  **Install the dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

5.  **Set up environment variables:**

    Create a `.env` file in the root of the project and add your API keys:

    ```
    OPENAI_API_KEY="YOUR_OPENAI_API_KEY"
    ```

## ▶️ Usage

1.  **Add your documents:**

    Place your PDF, TXT, or other supported documents in the `data` directory.

2.  **Run the application:**

    ```bash
    streamlit run app.py
    ```

3.  **Open your browser:**

    Navigate to `http://localhost:8501` to start chatting with your documents!

## ⚙️ Configuration

You can customize the chatbot's behavior by modifying the `config.py` file. This includes changing the LLM, the embedding model, and other parameters.

## 🤝 Contributing

Contributions are welcome! If you have any ideas, suggestions, or bug reports, please open an issue or submit a pull request.

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/your-feature`).
3.  Make your changes.
4.  Commit your changes (`git commit -m 'Add some feature'`).
5.  Push to the branch (`git push origin feature/your-feature`).
6.  Open a pull request.

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
