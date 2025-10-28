# n8n-Workflows

This repository contains n8n workflow templates that use the **Google Gemini Chat Model** and the **AI Agent** node for various automation tasks.
The workflows are saved as `.json` files and can be easily imported into your n8n instance.

## Workflows

### **1. MAIL-REPLY.json (Gmail AI Auto-Reply Agent)**

This workflow is a simple AI agent designed to trigger on new emails, generate a reply, and then send it using the Gmail node.
* **Trigger:** **Gmail Trigger** (on new email)
* **Core Logic:** **AI Agent** node using the **Google Gemini Chat Model** and the **Send a message in Gmail** tool.
* **Purpose:** Automatically draft or send replies to incoming emails based on the AI's logic.

* <img width="996" height="351" alt="Screenshot 2025-10-25 121208" src="https://github.com/user-attachments/assets/a1c506be-1fed-4c67-8db0-bfa5f75ec792" />


### **2. Telegram event booking.json (Telegram Calendar Booking Agent)**

This workflow acts as a Telegram bot that can book events in Google Calendar based on conversational input from a user.
* **Trigger:** **Telegram Trigger** (on new message)
* **Core Logic:** **AI Agent** node using the **Google Gemini Chat Model**, **Simple Memory** for conversation history, and the **Create an event in Google Calendar** tool.
* **Purpose:** Allows users to interact with a Telegram bot to schedule events in their Google Calendar.

Here is the small video of how it works.
https://youtu.be/5_7ao5Aquag?si=2e1USZll94GIlPHE


### **3. 🤖 RAG Chatbot using n8n (AI Agent + OpenAI + Pinecone)**

This project is a **Retrieval-Augmented Generation (RAG) Chatbot** built entirely using **n8n**, a no-code workflow automation tool.  
It uses **OpenAI embeddings**, **Pinecone vector storage**, and the **AI Agent** node to let users upload documents and chat with them intelligently.

## 🧩 Workflow Overview

The workflow integrates multiple nodes to implement a full RAG pipeline:
1. **Upload File** → Accepts user documents (PDF, text, etc.)
2. **Download File** → Fetches the uploaded file for processing
3. **Recursive Character Text Splitter** → Splits text into small, manageable chunks
4. **Default Data Loader** → Loads document content into the workflow
5. **OpenAI Embeddings** → Generates vector embeddings for each text chunk
6. **Pinecone Vector Store** → Stores embeddings for semantic similarity search
7. **When Chat Message Received** → Trigger for user input messages
8. **OpenAI Chat Model** → Generates responses using retrieved context
9. **AI Agent** → Combines retrieval and generation to answer context-aware questions


## 🧠 Concept: What is RAG?

**Retrieval-Augmented Generation (RAG)** combines two key AI techniques:
- **Retrieval:** Fetching the most relevant text chunks from stored documents using vector similarity.
- **Generation:** Using a language model (like GPT) to generate responses using those retrieved chunks.
This approach ensures the chatbot’s answers are **accurate**, **contextual**, and **grounded in your own data**.


## ⚙️ Tech Stack

| Component | Description |
|------------|-------------|
| **n8n** | No-code automation platform |
| **OpenAI API** | Used for generating embeddings and chat responses |
| **Pinecone** | Vector database for storing and retrieving embeddings |
| **AI Agent Node** | Handles retrieval and reasoning |
| **Text Splitter** | Splits large documents into smaller text chunks for embedding |

<img width="1042" height="345" alt="image" src="https://github.com/user-attachments/assets/187cb6c2-eaaa-4a68-b447-381f24be8621" />

Here is the small video of how it works.
https://youtu.be/vEOQVpK4Ppw
