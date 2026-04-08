Overview

This project implements a Retrieval-Augmented Generation (RAG) Chatbot that answers questions based on a research paper:

“AI Ethics: Integrating Transparency, Fairness, and Privacy in AI Development”

The chatbot uses:

Document chunking
Vector embeddings
Semantic search
LLM-based response generation

It allows users to query the document and get accurate, context-aware answers.

Architecture

The workflow is built using a node-based pipeline (as shown in your diagram):

PDF → Text Splitter → Embeddings → Vector Store → Retriever → LLM → Answer
Components Explained
Recursive Character Text Splitter
Splits the document into chunks
Chunk Size: 1000
Overlap: 200
File Loader
Loads the PDF:
AI_Ethics_Integrating_Transparency_Fairness_and_Privacy.pdf
Google Gemini Embeddings
Model: gemini-embedding-001
Converts text into vector format
In-Memory Vector Store
Stores embeddings
Enables semantic search (Top K = 4)
Mistral AI (LLM)
Model: mistral-tiny
Temperature: 0.9
Generates human-like responses
Buffer Memory
Maintains conversation context
Conversational Retrieval QA Chain
Combines:
Retriever (vector search)
LLM (answer generation)
Memory (chat history)
How It Works

PDF is loaded and split into chunks
Each chunk is converted into embeddings
Embeddings are stored in vector database
User asks a question
System retrieves most relevant chunks
LLM generates answer based on retrieved context 
"C:\OneDrive\Desktop\rag.png"

About the Dataset

The chatbot is trained on a research paper covering:

Transparency in AI
Fairness & Bias Prevention
Privacy & Data Protection
Global AI Policies (EU, US, China)

Key insights:

Ethical AI requires balancing transparency, fairness, and privacy
Different regions prioritize ethics differently
Bias mitigation and audits are essential for responsible AI
Tech Stack
LLM: Mistral AI
Embeddings: Google Gemini
Vector Store: In-Memory
Framework: LangChain / Flow-based builder
Data Source: PDF Research Paper
Installation
git clone https://github.com/your-username/rag-chatbot.git
cd rag-chatbot

Install dependencies:

pip install -r requirements.txt
Setup
Add API Keys:
Mistral AI Key
Google Generative AI Key
Configure environment variables:
MISTRAL_API_KEY=your_key
GOOGLE_API_KEY=your_key
Run the Project

Start your workflow (depending on tool used):

npm start
 or
python app.py
Example Queries
“What are the key principles of AI ethics?”
“How does the EU approach AI regulation?”
“What methods reduce bias in AI systems?”
“Explain fairness in AI”
Features

 Context-aware responses
 Document-based Q&A
 Conversational memory
 Ethical AI-focused knowledge
 Fast semantic retrieval

Future Improvements
Add persistent vector database (Pinecone / FAISS)
Multi-document support
UI dashboard
Integration with Power BI
Real-time document upload
Contributing

Author: Ridhima 

