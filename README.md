# LLM-RAG-ZC

A Retrieval-Augmented Generation (RAG) project built as part of my understanding of the RAG , exploring RAG pipelines, agentic workflows, and persistence for question-answering over a FAQ knowledge base.

## Overview

This project implements a RAG system that ingests FAQ-style documents, indexes them for retrieval, and uses an LLM to answer user questions grounded in that data. It also includes experiments with agentic loops and persistent storage of both the retrieval index and the RAG pipeline state.

## Project Structure

```
.
├── main.py                          # Entry point for running the RAG application
├── ingest.py                        # Script for ingesting and indexing FAQ data
├── rag_helper.py                    # Core RAG helper functions (retrieval, prompting, etc.)
├── agentic_rag.ipynb                # Notebook exploring agentic RAG patterns
├── afentic_loop.ipynb               # Notebook exploring an agentic loop implementation
├── persistent_rag.ipynb             # Notebook for persisting RAG components
├── persistence_rag_ingest.ipynb     # Notebook for persistent ingestion pipeline
├── lession1.ipynb                   # Course lesson notes / exercises
├── nootbook.ipynb                   # Scratch / working notebook
├── pyproject.toml                   # Project dependencies and metadata
├── uv.lock                          # Locked dependency versions (uv)
└── faq.db                           # Local FAQ database (generated, not committed)
```

## Requirements

- Python (see `.python-version` for the exact version used)
- [uv](https://github.com/astral-sh/uv) for dependency management

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/musaalamparvez/LLM-RAG-ZC.git
   cd LLM-RAG-ZC
   ```

2. Install dependencies with uv:
   ```bash
   uv sync
   ```

3. Set up any required environment variables (e.g., API keys for your LLM provider) in a `.env` file:
   ```
   OPENAI_API_KEY=your_key_here
   ```

## Usage

**Ingest data into the FAQ database:**
```bash
uv run ingest.py
```

**Run the main application:**
```bash
uv run main.py
```

**Explore the notebooks:**
Open any of the `.ipynb` files in Jupyter or VS Code to walk through the RAG, agentic, and persistence experiments interactively.

## Notes

- `faq.db`, `faq.db-shm`, and `faq.db-wal` are local SQLite database files generated at runtime and are excluded from version control via `.gitignore`.
- This is a learning project developed for the LLM Zoomcamp course; some notebooks may contain exploratory or in-progress work.

## License

Add a license of your choice (e.g., MIT) if you intend to share this project publicly.
