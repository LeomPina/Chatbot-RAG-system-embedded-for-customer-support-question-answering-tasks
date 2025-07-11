# RAG-Based Customer Service Assistant

A Retrieval-Augmented Generation (RAG) system tailored for customer service applications. This project combines semantic search with generative AI to deliver contextually accurate and informative responses to customer inquiries.

## Overview

This notebook demonstrates a complete pipeline to build a customer support chatbot using:

- **LangChain** for orchestration  
- **FAISS** for vector similarity search  
- **OpenAI Embeddings & LLM** for semantic understanding and generation  
- **Streamlit** for UI deployment  

### Features

- Load and process customer service documents  
- Embed text using OpenAI models  
- Store and retrieve context using FAISS vector store  
- Answer questions with real-time context retrieval  
- Modular LangChain architecture using `ConversationalRetrievalChain`

## 🛠Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/rag-customer-service.git
cd rag-customer-service
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

Minimal required packages:
```bash
pip install langchain faiss-cpu openai python-dotenv pypdf
```

### 3. Environment Variables

Create a `.env` file in the root directory:

```env
OPENAI_API_KEY=your_openai_api_key
```

## Usage

1. Place your support documents (PDFs) in the `data/` folder.
2. Run the notebook: `RAG_system_customer_service_task.ipynb`
3. Ask questions in natural language — the system retrieves relevant chunks and answers using OpenAI's LLM.

## Key Components

- **Document Loading**: `PyPDFLoader`, `TextLoader`
- **Text Splitting**: `CharacterTextSplitter`
- **Embedding Model**: `OpenAIEmbeddings`
- **Vector Store**: `FAISS`
- **QA Chain**: `ConversationalRetrievalChain`

## 📈 Example Questions

```bash
Q: How can I reset my account password?
Q: What is the return policy for defective items?
Q: Can I cancel my order after payment?
```

## Future Improvements

- Add a Streamlit frontend
- Explore other datasets and evaluate results
- Finetune the LLM used
- Support more file types (Word, HTML)
- Multi-turn conversation memory
- Azure/Open Source LLM support




