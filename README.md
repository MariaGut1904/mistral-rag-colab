#  Mistral RAG Colab

It uses Mistral 7B, LlamaIndex, and HuggingFace embeddings to let you ask questions about PDFs and extract important information from them.

I made this to practice building real-world AI pipelines in an AI externship I did in April 2025 that focused on the use of AI and how it can be incorporated to help find important data in bulks of files for taking out mortgages.

---

## What It Does

You upload one or more PDFs, and it:
- Extracts the text
- Breaks it into chunks
- Builds a vector index
- Lets you ask natural questions
- Returns accurate, reranked answers from your documents

---

##  Sample Questions You Can Ask

- “What are the late payment penalties?”
- “Summarize the contract in plain English.”
- “List all financial obligations.”
- “Does it mention automatic renewal?”

---

##  Google Colab link

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1RKjFxByL43Mpl84LRZULkIS9pofJ-aun?usp=sharing)



---

##  What Was Used

- **Mistral 7B** — lightweight LLM running on GPU
- **llama-cpp-python** — efficient local inference
- **LlamaIndex** — builds the semantic index
- **HuggingFace Embeddings** — `bge-small-en-v1.5`
- **Reranker** — improves answer quality with `cross-encoder/ms-marco-MiniLM-L-6-v2`
- **pymupdf** — extracts text from PDFs

---


```bash
pip install torch llama-cpp-python==0.2.90 llama-index pymupdf llama-index-llms-llama-cpp llama-index-embeddings-huggingface sentence-transformers --extra-index-url https://abetlen.github.io/llama-cpp-python/whl/cu123
