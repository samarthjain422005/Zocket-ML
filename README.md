# Zocket-ML

# Web Summarizer

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
    A[Input: Website URL] --> B[Scrape Text with Selenium]
    B --> C[Preprocess & Clean Text]
    C --> D[Split into Overlapping Chunks]
    D --> E[Sentence Transformer Embeddings]
    E --> F[Store in FAISS Vector DB]
    F --> G[Per-chunk Analysis with Gemini]
    G --> H[Final Summary Synthesis with Gemini]
    H --> Z[Output: Website Summary]

Here's the `README.md` in clean **Markdown format** with only:

* ✅ Description
* ✅ System architecture
* ✅ Requirements and setup instructions

---

````markdown
# 🧠 Gemini + SentenceTransformer Web Summarizer

This project summarizes any webpage using a combination of:

- **Selenium** for scraping,
- **Text preprocessing and chunking**,
- **SentenceTransformer embeddings** stored in **FAISS**,
- **Google Gemini Pro** for understanding and summarizing content.

Implemented entirely in a single **Jupyter Notebook**, it outputs a structured and concise summary of the webpage content.

---

## 🧩 System Architecture

```mermaid
graph TD
    A[🌐 Input: Website URL] --> B[🕷️ Scrape with Selenium]
    B --> C[🧹 Preprocess Text]
    C --> D[✂️ Chunk Text (with Overlap)]
    D --> E[🔗 Embed with SentenceTransformer]
    E --> F[🗂️ Store in FAISS Vector DB]
    F --> G[📑 Analyze Chunks via Gemini]
    G --> H[🧠 Synthesize Final Summary]
    H --> I[📤 Output: Structured Webpage Summary]
````

---

## Requirements and Setup

### Python Version

Ensure you're using **Python 3.9+**.

### Install Required Libraries

Then install all dependencies with:

```bash
pip install -r requirements.txt
```

For Jupyter Notebook support:

```bash
pip install notebook ipykernel
```

### Gemini API Key

Add your Gemini API key by updating the notebook:

```python
from google.generativeai import configure
configure(api_key="YOUR_GEMINI_API_KEY")
```

### Run the Notebook

```bash
jupyter notebook
```

---

```

