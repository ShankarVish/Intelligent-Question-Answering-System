# 🧠 Intelligent Question Answering System (RAG + LLM)

A Retrieval-Augmented Generation (RAG) system using LangChain, OpenAI, and Pinecone to answer questions from PDFs, DOCX, TXT, or Wikipedia articles.

---

## 🔧 Main Features

- ✅ Load files (PDF, DOCX, TXT) or Wikipedia articles
- ✂️ Split text into manageable chunks
- 🔍 Embed chunks using OpenAI (`text-embedding-3-small`)
- 📦 Store & retrieve embeddings with Pinecone
- 💬 Ask questions using `GPT-3.5-Turbo` (LangChain RAG pipeline)
- 🧠 Optional memory for multi-turn chat (ConversationalRetrievalChain)
- 🔄 Interactive Q&A loop in terminal

---

## 📁 Workflow

1. **Load documents**
2. **Chunk text**
3. **Generate embeddings**
4. **Store/fetch from Pinecone**
5. **Ask questions → Get answers**
6. **(Optional)** Maintain conversation history

---

## 🧰 Tech Stack

- `LangChain`, `OpenAI`, `Pinecone`
- `PyPDFLoader`, `Docx2txtLoader`, `WikipediaLoader`
- `GPT-3.5-Turbo`, `text-embedding-3-small`
- `.env` config for API keys

---

## ▶️ Run

```bash
pip install openai langchain pinecone-client tiktoken pypdf docx2txt wikipedia
```

Set API keys in `.env`, then run your script.

---

## 📌 Example

```text
Question: What is the Bill of Rights?
Answer: The Bill of Rights refers to the first ten amendments...
```

---

## 🗑 Cleanup

Delete indexes from Pinecone with:

```python
delete_pinecone_index("your_index")  # or "all"
```

---

