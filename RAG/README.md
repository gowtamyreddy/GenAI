# 🧠 RAG Pipeline using Hugging Face, ChromaDB, and Groq LLM

---

## Goal

The goal of this project is to build a **Retrieval-Augmented Generation (RAG)** pipeline that:

- Uses **external knowledge sources** (e.g., websites) as context  
- Retrieves **semantically relevant content** for user queries  
- Generates accurate, grounded answers using **Groq-hosted LLaMA3 models**

---

## How It Works

1. Scrape live content using `WebBaseLoader`  
2. Split long text into manageable chunks  
3. Embed chunks with `all-MiniLM-L6-v2` from Hugging Face  
4. Store embeddings in **ChromaDB** (local vector store)  
5. Retrieve top-matching chunks using vector similarity  
6. Pass retrieved context into Groq's LLaMA3 model  
7. Generate intelligent, concise answers with LangChain  

---

## Steps Overview

### 🔧 Step 1: Install Dependencies

Install required Python packages using pip.

### 🔐 Step 2: Set Your Groq API Key

Set the `GROQ_API_KEY` environment variable from your Groq Console.

### 🌐 Step 3: Load Web Content

Use `WebBaseLoader` to pull live data (e.g., from IBM’s Machine Learning page).

### ✂️ Step 4: Chunk the Text

Split documents into overlapping chunks for efficient retrieval.

### 🧠 Step 5: Generate Embeddings & Store in ChromaDB

Use `all-MiniLM-L6-v2` to convert text into embeddings and store them locally.

### 🔍 Step 6: Retrieve Relevant Chunks

Use semantic similarity search to find the most relevant chunks for any query.

### 🤖 Step 7: Build the RAG Pipeline

Connect retriever → prompt → Groq LLM using LangChain’s modular components.

### 💬 Step 8: Ask Questions

Run queries like:

- “What is Machine Learning?”  
- “What are some use cases of ML?”  
- “What’s the difference between ML and DL?”  

Groq’s LLM will respond based on retrieved knowledge chunks with fast, accurate answers.
