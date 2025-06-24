# DocIQ – Your Intelligent Assistant for Documents
DocIQ is a real-time PDF assistant powered by open-source LLMs and vector search. 
Upload a PDF, and immediately start chatting with it — all locally and without uploading your data to the cloud.


## DocIQ Screenshot

https://github.com/AsmaaIbrahimMoussa/DocIQ/blob/main/DocIQ.png


## Features
- Upload and preview any PDF document
- Automatic text chunking and vector embedding using BGE (BAAI/bge-small-en)
- Real-time semantic search with Qdrant
- Local language model (LLaMA 3 via Ollama) to answer questions based on document content
- Clean, minimal chat interface using Streamlit


## Tech Stack
- **Frontend**: Streamlit
- **LLM**: LLaMA 3 (via [Ollama](https://ollama.com))
- **Embeddings**: BGE (sentence-transformers)
- **Vector DB**: Qdrant (Docker-based)
- **Framework**: LangChain


## How It Works
1. Upload a PDF
2. The file is split into chunks and converted into embeddings
3. Embeddings are stored in a local Qdrant vector store
4. When you ask a question, similar chunks are retrieved
5. The LLM (LLaMA 3) uses the chunks as context and responds

## Installation

### 1. Clone the repository

~~~
```bash
git clone https://github.com/yourusername/dociq.git
cd dociq
~~~

### 2. Install dependencies

~~~
pip install -r requirements.txt
~~~

### 3. Start Qdrant (via Docker)

~~~
docker run -p 6333:6333 -p 6334:6334 qdrant/qdrant
~~~

### 4. Run Ollama with LLaMA 3

~~~
ollama run llama3
~~~

### 5. Launch the app

~~~
streamlit run app.py
~~~

