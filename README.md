# Local LLM PDF Query System (No API Key Required)

This project enables querying collections of PDF documents (research papers, reports, etc.) using a local Hugging Face LLM (`flan-t5-large`) and vector-based retrieval with FAISS — all running in a Google Colab notebook, without needing an OpenAI API key.

---

## Features

- ✅ Upload and organize PDFs into weighted folders (e.g., `papers1/`, `papers2/`)
- ✅ Automatically extract, chunk, and embed content using `MiniLM`
- ✅ Weight documents based on folder importance (e.g., `papers1 → 3`, `papers2 → 7`)
- ✅ Retrieve top relevant chunks and generate answers using `flan-t5-large`
- ✅ Fully local and open-source — works without internet inference or paid APIs

---

## How It Works

1. **Ingest PDFs:** Reads PDFs from subfolders inside `all_papers/`
2. **Assign Weights:** Folder-level importance used to prioritize answers
3. **Embed Chunks:** Uses `all-MiniLM-L6-v2` for document embeddings
4. **Retrieve & Rank:** Retrieves top matches with FAISS and applies custom scoring
5. **Generate Answer:** Context passed to `flan-t5-large` via a structured prompt

---

## Tech Stack

- [LangChain](https://github.com/langchain-ai/langchain) — prompt & retrieval pipeline
- [Hugging Face Transformers](https://huggingface.co/docs/transformers) — Flan-T5 inference
- [FAISS](https://github.com/facebookresearch/faiss) — fast similarity search
- [PyMuPDF](https://github.com/pymupdf/PyMuPDF) — PDF extraction
- [MiniLM](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2) — embeddings

---