# Semantic Document Search with ChromaDB & Google Gemini

This project demonstrates how to build a local vector database for semantic search. We take a collection of text files, break them into manageable "chunks" using a smart splitting strategy, convert them into mathematical vectors using **Google Gemini**, and store them in **ChromaDB** for lightning-fast retrieval.

## 🚀 What we do in this exercise
1.  **Environment Setup:** Configuring Python to talk to Google's Generative AI servers securely.
2.  **Data Ingestion:** Loading raw `.txt` files from a local directory.
3.  **Smart Chunking:** Using `RecursiveCharacterTextSplitter` to slice documents into segments while preserving context through "overlap."
4.  **Vectorization:** Converting human language into high-dimensional vectors using the `text-embedding-004` model.
5.  **Persistence:** Storing these vectors in a local ChromaDB instance so the data survives after the script stops.
6.  **Semantic Retrieval:** Querying the database to find the most relevant document parts based on *meaning* rather than just keywords.

---

## 🛠 Requirements

### 1. Libraries & Dependencies
You will need the following Python packages:
* `chromadb`: The vector database.
* `google-generativeai`: Google's official SDK for Gemini.
* `langchain-google-genai`: LangChain integration for Gemini.
* `langchain-community` & `langchain`: Framework for document handling and splitting.

### 2. Google AI API Key
You must have a valid API Key from [Google AI Studio](https://aistudio.google.com/app/apikey).

---

## 📋 Steps to Run

### Step 1: Install Dependencies
Run the following command in your terminal or a notebook cell:
```bash
pip install -q -U chromadb google-generativeai langchain-google-genai langchain-community
