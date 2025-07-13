# 🧠 RAG Business QA Bot

A Retrieval-Augmented Generation (RAG) powered chatbot designed to answer business-related questions based on uploaded company PDFs. This project leverages OpenAI's language models, LangChain and Pinecone for intelligent document retrieval and response generation.

> 📘 Example used: TCS (Tata Consultancy Services) company profile from its official website.

---

## 🚀 Features

- ✅ Retrieval-Augmented Generation using LangChain
- 📄 Accepts any PDF with extractable business info
- 🔍 Vector-based search using Pinecone
- 🧠 Uses OpenAI embeddings and LLM (gpt-4o-mini)
- 🧾 Accurate answers with document-based context
- 💬 CLI-based QA chatbot (can be ported to UI)

---

## 🛠️ Tech Stack

| Component         | Technology Used                   |
|------------------|-----------------------------------|
| Language Model    | OpenAI `gpt-4o-mini`              |
| Embeddings        | `text-embedding-ada-002`          |
| Vector Store      | Pinecone                          |
| Framework         | LangChain                         |
| Deployment        | Google Colab                      |
| File Format       | `.pdf` (text-based documents)     |

---

## 🧩 How It Works

1. **Upload PDF**  
   Upload a document like a company profile (e.g. `TCS Information Data.pdf`) to Colab.

2. **Split into Chunks**  
   The document is divided into manageable text chunks for better retrieval accuracy.

3. **Generate Embeddings**  
   Uses OpenAI to convert each chunk into vector representations.

4. **Store in Pinecone**  
   Chunks are indexed in Pinecone using cosine similarity.

5. **Connect LLM**  
   The QA chain uses a retriever + generator combo (`gpt-4o-mini`).

6. **Ask Questions**  
   Ask business-related queries and receive factual, context-aware answers.

---

## 💬 Sample Queries

- “When was TCS founded?”
- “Who was the first CEO of TCS?”
- “What is TCS’s primary line of business?”
- “Which company did TCS surpass in 2020?”

---

## 📂 Setup Instructions

> ✅ Run entirely in **Google Colab**. No local installation required.

1. Clone the notebook or open it in Colab.
2. Upload your target PDF (`TCS Information Data.pdf` or similar).
3. Save your **OpenAI** and **Pinecone** API keys in Colab secrets:

Everything else is in the notebook itself.
