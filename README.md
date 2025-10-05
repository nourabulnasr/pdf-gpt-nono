# 📘 AI PDF Chatbot – Built by Nounie

> A Streamlit web app that lets you upload any PDF and chat with it — powered by LangChain, FAISS, and OpenAI GPT models.

---

## 🚀 Overview
This project turns static PDFs into **interactive, intelligent documents**.  
Upload a research paper, report, or contract — then **ask questions** in natural language and get context-aware answers instantly.

I built this to understand how **RAG (Retrieval-Augmented Generation)** works and how AI agents can retrieve, reason, and respond based on private data.

---

## 🧠 How It Works
1. **Upload a PDF**  
   The app extracts all text and splits it into small, overlapping chunks.
2. **Embed & Store**  
   Each chunk is converted into a numerical vector using `OpenAIEmbeddings`, then stored in a **FAISS** vector database.
3. **Ask a Question**  
   Your query is embedded the same way. FAISS finds the most relevant chunks.
4. **Generate Answer**  
   The retrieved chunks + your question are sent to an LLM (GPT-3.5 / GPT-4).  
   The model answers based only on your PDF’s content.
5. **Display in Streamlit**  
   Clean, minimal chat interface built with Streamlit.

---

## 🧰 Tech Stack
- **Python 3.11+**
- **Streamlit** – Web UI  
- **LangChain** – RAG pipeline framework  
- **FAISS** – Vector search engine  
- **OpenAI API** – Text embeddings & LLM  
- **PyPDF2** – Text extraction  

---

## 🧑‍💻 Run Locally

```bash
git clone https://github.com/nourabulnasr/AI-PDF-Reader.git
cd AI-PDF-Reader
python -m venv .venv
.venv\Scripts\activate    # or source .venv/bin/activate
pip install -r requirements.txt
