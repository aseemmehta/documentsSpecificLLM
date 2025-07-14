A simple LLM code which doesn't require API-key. and can be run on google colab notebook to query any collection of PDF documents using a local Hugging Face LLM (like `flan-t5-base`) and vector search (FAISS).

## Features
- Upload your own PDFs (biomedical, legal, research, etc.)
- Automatically chunk and embed documents
- Ask natural language questions and get context-grounded answers
- Uses only open-source tools — no OpenAI key needed

## Tech Stack
- [LangChain](https://github.com/langchain-ai/langchain)
- [Transformers](https://huggingface.co/docs/transformers)
- [FAISS](https://github.com/facebookresearch/faiss)
- [PyMuPDF](https://github.com/pymupdf/PyMuPDF)

## Code File
- `launchAndQuery.ipynb` — the full interactive Colab notebook
