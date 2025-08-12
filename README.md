# 🛒 DMart Complaint Routing Bot 🤖

An **AI-powered complaint handling system** for **DMart** customers, built with **n8n**, **Pinecone**, and **OpenAI**.  
Integrates with a **Telegram Bot** 📱 to automatically route and respond to customer complaints using **real complaint & FAQ datasets** 📂.

---

## 📌 Description
AI-powered DMart Complaint Routing Bot with Telegram + n8n workflows, Pinecone vector search, and OpenAI embeddings.  
Automates complaint handling, matches queries to FAQs, and responds instantly with accurate resolutions.

---

## 🚀 Features

- 📱 **Telegram Bot Integration** — Chat with customers via [@DMartSupport_bot](https://t.me/DMartSupport_bot)  
- 🧠 **AI-Powered Matching** — Finds the best FAQ using semantic search  
- 🔍 **Pinecone Vector Search** — Fast, scalable similarity search  
- ⚡ **n8n Automation** — Fully automated routing and FAQ answering  
- 📂 **Realistic Dataset** — 30+ DMart complaints and 30+ FAQs  
- 🔗 **Seamless Integrations** — OpenAI, Telegram API, Pinecone, Google Drive  

---

## 🎥 Demo

**Example Interaction:**  

**User:** "I bought milk from DMart and it was expired."  
**Bot:** "Please visit the store with your purchase bill and the expired item. DMart has a return/replacement policy for expired goods, and you will be provided with a fresh product or a refund."  

**User:** "Can I cancel my DMart Ready order after payment?"

**Bot:** "Yes, you can cancel your DMart Ready order after payment, but only before order processing starts. You can do this via the app or website. Refunds usually take 5–7 working days."

### 5️⃣ Activate Bot  
- Start both workflows in n8n  
- Chat via [@DMartSupport_bot](https://t.me/DMartSupport_bot)  
---

## 📊 Workflow Diagram

**Diagram 1 — Vector Update Workflow**

📂 Google Drive Dataset → 🤖 n8n Vector Update Workflow → 🧠 OpenAI Embeddings → 🔍 Pinecone Index Update

**Diagram 2 — Complaint Routing Workflow**

🛒 Telegram Bot → 🤖 n8n Complaint Routing Workflow → 🧠 OpenAI Embeddings + 🔍 Pinecone Vector Search → 📜 FAQ Match → 💬 Customer Reply
---

## 📂 Project Structure

```
📁 data/
 ├── dmart_complaints.csv         # 📝 Real DMart-style complaints  
 ├── dmart_faq_list.csv           # 📚 DMart FAQs with answers  
📁 workflows/
 ├── Complaint Routing.json       # 🤖 n8n workflow for Telegram bot  
 ├── Vector Complaint Routing Assist.json # 🔍 n8n workflow for Pinecone updates  
```

---

## ⚙️ How It Works

1. 📂 **Data Loading** — Complaints & FAQs stored in Google Drive  
2. 🧠 **Embedding & Indexing** — OpenAI embeddings + Pinecone search  
3. 📱 **Telegram Handling** — Bot receives messages & matches best FAQ  
4. ⚡ **Instant Reply** — Sends an accurate resolution back to the customer  
5. 🔄 **Auto-Update** — Vector index refreshed when datasets change  

---

## 🔧 Setup Instructions

### 1️⃣ Clone Repository
```bash
git clone https://github.com/yourusername/dmart-complaint-routing-bot.git
cd dmart-complaint-routing-bot
```

### 2️⃣ Install n8n  
Follow [n8n Installation Guide](https://docs.n8n.io/getting-started/installation/).

### 3️⃣ Import Workflows  
- In n8n, import `Complaint Routing.json` and `Vector Complaint Routing Assist.json`.

### 4️⃣ Configure Credentials  
- 🤖 **Telegram Bot API Token** — Create via BotFather  
- 🧠 **OpenAI API Key** — For embeddings & responses  
- 🔍 **Pinecone API Key** — For vector storage & search  
- ☁ **Google Drive Auth** — To access datasets  

---

## 📊 Data Files

| File | Description |
|------|-------------|
| 📝 `dmart_complaints.csv` | Contains DMart complaint examples |
| 📚 `dmart_faq_list.csv` | FAQs with clear, concise answers |

---

## 🤝 Contributing  
Pull requests welcome! Please follow coding and workflow best practices.

---

## 📜 License  
MIT License — Free to use & modify.
