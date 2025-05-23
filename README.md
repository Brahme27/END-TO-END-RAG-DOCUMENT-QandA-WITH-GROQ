# RAG Document Q\&A with Groq and Llama3

This is a simple Streamlit application that uses Retrieval-Augmented Generation (RAG) to answer questions based on research papers (PDFs) using Groq's Llama3 model and FAISS for vector search.

## Features

* Load and split PDF documents from a directory
* Generate embeddings using OpenAI Embeddings
* Store and retrieve documents using FAISS vector store
* Use Groq's `Llama3-8b-8192` model for answering questions based on context
* Easy-to-use Streamlit interface

##  Setup

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
```

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

3. **Create a `.env` file**

```env
OPENAI_API_KEY=your_openai_api_key
GROQ_API_KEY=your_groq_api_key
```

4. **Add your PDFs**

Place all your PDF files in the `research_papers/` directory.

## How to Use

1. Run the Streamlit app:

```cmd
streamlit run app.py
```

2. Click the **"Document Embedding"** button to create the vector store.

3. Enter your question in the text input and get answers based on the uploaded PDFs.

## 📦 Dependencies

* Streamlit
* LangChain
* langchain-groq
* langchain-openai
* FAISS
* dotenv
* openai

## Note

* Only the first 50 PDFs (or documents) are loaded for performance.
* The app uses chunking with overlap to better preserve context.
