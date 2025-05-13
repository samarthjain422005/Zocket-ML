# Zocket-ML

# Gemini Web Summarizer

A smart web content summarizer that:
- Scrapes and preprocesses a website's text.
- Chunks it intelligently with overlap.
- Embeds each chunk using **Sentence Transformers** and stores them in a **FAISS vector database**.
- Analyzes each chunk using **Gemini Pro** (Google Generative AI).
- Synthesizes a final coherent summary of the website.

Built in a single **Jupyter Notebook**.

---

## Features

- Headless website scraping using Selenium
- Intelligent chunking of long-form text with overlap
- Embedding with `sentence-transformers` (`all-MiniLM-L6-v2`)
- Semantic similarity storage in FAISS
- Chunk-level analysis via Gemini Pro
- Final website summary generation

---

## System Architecture

```mermaid
graph TD
    A[🌐 Input: Website URL] --> B[🕷️ Scrape Text with Selenium]
    B --> C[🧹 Preprocess & Clean Text]
    C --> D[📄 Split into Overlapping Chunks]
    D --> E[🔗 Sentence Transformer Embeddings]
    E --> F[🗂️ Store in FAISS Vector DB]
    F --> G[📑 Per-chunk Analysis with Gemini]
    G --> H[🧠 Final Summary Synthesis with Gemini]
    H --> Z[📤 Output: Website Summary]

    
