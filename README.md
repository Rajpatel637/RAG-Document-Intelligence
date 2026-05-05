# RAG Document Intelligence

![RAG Banner](https://img.shields.io/badge/RAG-Document--Intelligence-blue?style=for-the-badge&logo=fastapi)
![Python](https://img.shields.io/badge/Python-3.9+-blue?style=for-the-badge&logo=python)
![FastAPI](https://img.shields.io/badge/FastAPI-v0.100+-green?style=for-the-badge&logo=fastapi)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-pgvector-blue?style=for-the-badge&logo=postgresql)

## 🚀 Overview

**RAG Document Intelligence** is a high-performance, scalable Retrieval-Augmented Generation (RAG) API built with FastAPI and LangChain. It provides an ID-based document indexing and retrieval system optimized for enterprise-grade applications.

By leveraging **PostgreSQL/pgvector**, it enables fast and efficient semantic searches across large document sets, allowing you to build intelligent applications that can "chat" with your data.

## ✨ Key Features

- **📂 ID-Based Management**: Organize and query embeddings at a file-level for precision retrieval.
- **⚡ Asynchronous Architecture**: Built on FastAPI for high-concurrency and non-blocking I/O operations.
- **🔍 Vector Store Integration**: Seamless integration with `pgvector` for advanced similarity searches.
- **🛠️ Multi-Provider Support**: Compatible with OpenAI, Azure, Hugging Face, VertexAI, Ollama, and AWS Bedrock.
- **📦 Scalable Processing**: Optimized batch embedding processing for handling large datasets with minimal memory overhead.
- **🛡️ Secure & Robust**: Integrated middleware for logging, security, and error handling.

## 🛠️ Tech Stack

- **Framework**: [FastAPI](https://fastapi.tiangolo.com/)
- **Orchestration**: [LangChain](https://www.langchain.com/)
- **Database**: [PostgreSQL](https://www.postgresql.org/) with [pgvector](https://github.com/pgvector/pgvector)
- **Runtime**: [Docker](https://www.docker.com/) & [Uvicorn](https://www.uvicorn.org/)

## 🚀 Getting Started

### Prerequisites

- Python 3.9+
- Docker & Docker Compose (Optional, for easy setup)
- PostgreSQL with pgvector extension

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/RAG-Document-Intelligence.git
   cd RAG-Document-Intelligence
   ```

2. **Set up a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure Environment Variables:**
   Create a `.env` file based on the provided configuration options (see below).

5. **Run the API:**
   ```bash
   uvicorn main:app --reload
   ```

### Docker Setup

The easiest way to get started is using Docker:

```bash
docker compose up -d
```

This will spin up both the FastAPI application and a PostgreSQL database with pgvector enabled.

## ⚙️ Configuration

| Variable | Description | Default |
|----------|-------------|---------|
| `RAG_OPENAI_API_KEY` | OpenAI API Key for embeddings | Required |
| `VECTOR_DB_TYPE` | Type of vector store (e.g., `pgvector`) | `pgvector` |
| `POSTGRES_DB` | PostgreSQL database name | `rag_api` |
| `CHUNK_SIZE` | Size of text chunks for processing | `1500` |
| `CHUNK_OVERLAP` | Overlap between chunks | `100` |

*For a full list of configuration options, refer to the source code or the extended documentation.*

## 🧪 Testing

Run the test suite to ensure everything is working correctly:

```bash
pytest
```

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  Built with ❤️ for the AI Community
</p>
