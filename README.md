# AI Customer Support Agent (n8n + Gemini + Pinecone)

This project is an intelligent automated customer support agent built with n8n. It monitors a Gmail inbox, filters for support-related queries, and uses an **AI Agent with RAG (Retrieval-Augmented Generation)** to generate accurate, context-aware replies based on your knowledge base.

<img width="856" height="368" alt="image" src="https://github.com/user-attachments/assets/c40ee14c-9720-4d51-adc8-dd022fcb9102" />


## ✨ How It Works

1.  **Email Trigger:** Monitors incoming emails via the **Gmail Trigger**.
2.  **Classification:** Uses an AI **Text Classifier** to determine if the email is "Customer Support" related or "Other". Non-support emails are ignored.
3.  **AI Agent (The Brain):**
    * Receives the customer's query.
    * **Tool Usage:** Automatically queries a **Pinecone Vector Database** to find relevant company policies or troubleshooting steps.
    * **Response Generation:** Uses **Google Gemini** to draft a friendly, helpful reply based *only* on the retrieved data.
4.  **Response:** (Optional) You can add a Gmail node at the end to automatically send the reply.

## 🛠️ Tech Stack

* **Orchestration:** [n8n](https://n8n.io/)
* **LLM:** Google Gemini (PaLM API)
* **Vector Database:** Pinecone
* **Email Service:** Gmail

