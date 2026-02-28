🤖 RAG Customer Support Agent

An AI-powered customer support automation system built using Retrieval-Augmented Generation (RAG) architecture.
The system automatically processes incoming emails, retrieves relevant contextual knowledge using vector search, and generates intelligent, grounded responses using a Large Language Model.

Built with n8n, OpenAI, Pinecone, and Gmail API.



📌 Features

📩 Automatically triggers on new customer support emails
🔎 Retrieves context-aware knowledge using vector similarity search (Pinecone)
🧠 Uses OpenAI LLM to generate grounded responses
✉️ Sends automated reply directly via Gmail
⚙️ Modular workflow architecture using n8n
🛡️ Reduces hallucination through retrieval-based grounding



🧠 How It Works

Gmail Trigger detects incoming support email

Email content is converted into embedding

Embedding is matched against Pinecone vector database

Top relevant knowledge chunks are retrieved

Retrieved context is injected into LLM prompt

OpenAI generates a context-aware response

System automatically replies via Gmail

This ensures responses are based on company knowledge instead of generic AI outputs.



🏗️ Architecture

Gmail Trigger (Email Ingestion)

n8n AI Agent (Workflow Orchestration)

Pinecone (Vector Database Retrieval)

OpenAI Chat Model (Response Generation)

Gmail Reply Node (Automated Response)



🛠️ Tech Stack

n8n

OpenAI Chat Model

Pinecone

Gmail API

REST APIs

Vector Embeddings

RAG Architecture



🎯 Example Use Case

Customer Email:
“Where is my order? It hasn’t arrived yet.”

System retrieves:
Shipping policy + delivery timeline from vector database.

Generated Response:
Context-aware explanation based on actual company knowledge instead of generic AI assumptions.



🚀 Key Engineering Decisions

Retrieval-first architecture to reduce hallucination

Modular workflow design for scalability

Context injection before generation

Clean separation of retrieval and generation layers



🔐 Security & Configuration

API keys stored via environment variables

No sensitive data committed to repository

Designed with controlled prompt structure



📁 Repository Contents

workflow-export.json → Exported n8n workflow

architecture-diagram.png → System architecture diagram

README.md → Project documentation



🔮 Future Improvements

Add conversation memory layer

Add human escalation fallback

Add logging and monitoring

Implement confidence scoring
