# financial-rag-analyzer

AI system that analyzes financial reports using **RAG (Retrieval-Augmented Generation)**, **Llama**, and **numerical extraction**.

---

## Overview

This project is an AI-based financial report analysis system that automatically extracts key numerical information from financial report PDFs and generates analytical summaries using a Retrieval-Augmented Generation (RAG) pipeline.

The system combines rule-based numerical extraction with large language models to improve accuracy and reduce hallucinations when handling financial data.

---

## Features

* Extract financial metrics from PDF financial reports
* Retrieval-Augmented Generation (RAG) for document understanding
* LLM-based financial analysis using Llama
* Numerical hallucination prevention
* Automated evaluation using multiple NLP metrics

---

## Technologies Used

* Python
* RAG (Retrieval-Augmented Generation)
* FAISS vector database
* LangChain
* Llama (LLM)
* SentenceTransformers
* HuggingFace Transformers
* PDF text extraction

---

## System Architecture

1. **PDF Parsing**

   Financial report PDFs are parsed to extract raw text data.

2. **Numerical Extraction**

   Regular expressions are used to extract key financial metrics such as:

   * Revenue
   * Pre-tax profit
   * Net income
   * Total assets
   * ROE

3. **Vector Database Creation**

   The extracted text is split into chunks and converted into embeddings using SentenceTransformer.

4. **RAG Retrieval**

   Relevant document sections are retrieved using similarity search.

5. **LLM Analysis**

   Llama generates financial analysis based on:

   * extracted numerical data
   * retrieved document context

6. **Evaluation**

   The generated summaries are evaluated using:

   * ROUGE
   * BLEU
   * BERTScore
   * Sentence-BERT similarity
   * Numerical accuracy metrics

---

## Example Workflow

1. Upload a financial report PDF
2. Extract numerical financial data
3. Build a vector database from the document
4. Retrieve relevant sections using RAG
5. Generate financial analysis using Llama
6. Evaluate output quality

---

## Installation

Install required libraries:

```bash
pip install -r requirements.txt
```

---

## Usage

Run the analysis script:

```bash
python main.py
```

Or execute the notebook in Google Colab.

---

## Project Structure

```
financial-rag-analyzer
│
├ notebook
│   └ analysis.ipynb
│
├ src
│   ├ extractor.py
│   ├ rag_analyzer.py
│   ├ evaluation.py
│   └ judge.py
│
├ requirements.txt
└ README.md
```

---

## Future Improvements

* Improve numerical extraction accuracy
* Add financial ratio calculations
* Support multiple financial report formats
* Improve RAG retrieval performance
* Add visualization of evaluation results

---

## License

MIT License

