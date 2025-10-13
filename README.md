🩺 MediBot AI — My Intelligent Medical Chat Assistant
💡 Overview

MediBot AI is a medical chatbot powered by LangChain, HuggingFace, and Groq LLMs.
It allows users to ask health-related questions and get answers directly from medical PDFs or other documents.
The app uses Retrieval-Augmented Generation (RAG) to ensure accurate, context-based responses with source citations.

Screenshot of MediBot AI:
<img width="1814" height="959" alt="image" src="https://github.com/user-attachments/assets/d946e08d-b85b-4f6f-9dd1-56905ea1d2a5" />


🚀 Features
🧠 Retrieval-Augmented Generation (RAG) — combines document retrieval with LLM reasoning.
📚 PDF Knowledge Base — reads and indexes medical documents using FAISS.
💬 Interactive Chat Interface — built with Streamlit for real-time conversations.
🤖 Powerful AI Models — uses meta-llama/llama-4-maverick-17b (Groq) or mistralai/Mistral-7B (HuggingFace).
🔒 Environment-Based Secrets — secure API keys using .env and python-dotenv.

🧩 Tech Stack
Component	Technology
UI	Streamlit
NLP Framework	LangChain
Vector Store	FAISS
Embeddings	Sentence Transformers (all-MiniLM-L6-v2)
LLMs	Groq API / HuggingFace API
File Loader	PyPDFLoader
Environment	Python 3.10+
⚙️ Installation

Clone the Repository
git clone https://github.com/yourusername/medibot-ai.git
cd medibot-ai

Create a Virtual Environment
python -m venv .venv
.venv\Scripts\activate      # (Windows)
source .venv/bin/activate   # (Mac/Linux)

Install Dependencies
pip install -r requirements.txt

Set Up API Keys
Create a .env file in the root directory:

GROQ_API_KEY=your_groq_api_key
HF_TOKEN=your_huggingface_token

Add Your Medical PDFs
Place all PDF files in the /data folder.

Generate the Vector Database
python create_vectorstore.py

Run the Chatbot
streamlit run medibot.py

🧠 Example Use Case
You can upload medical research papers, pathology guides, or pharmacology PDFs and ask:
→ What are the histological features of sickle cell anemia?
→ Explain the mechanism of action of insulin.
→ What are the common symptoms of iron deficiency anemia?

📦 Folder Structure
medical-chatbot-main/
│
├── data/                     # Folder for medical PDFs
├── vectorstore/              # FAISS index saved here
├── medibot.py                # Streamlit chat app
├── create_vectorstore.py     # PDF → Embeddings → FAISS
├── connect_memory_with_llm.py# CLI testing script
├── .env                      # API keys
├── requirements.txt
└── README.md

🧪 Future Improvements
🧍‍♂️ Add user authentication
🌐 Allow web-based document uploads
🩸 Integrate with medical APIs (e.g., PubMed)
🧾 Enable answer citation highlighting

👩‍💻 Author
Amna 
💬 AI/ML Developer | LangChain & NLP Enthusiast
🎓 Computer Engineering, UET
📧 amna30042002@gmail.com
🔗 linkedin.com/in/amna-fiaz

🪪 License
This project is licensed under the MIT License — you’re free to use, modify, and distribute it with attribution.
