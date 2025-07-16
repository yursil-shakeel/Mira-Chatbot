# 🍽️ Restaurant Chatbot
**🔗 Demo:** [Click here to try the chatbot](https://bot.dialogflow.com/e1628923-f06c-408d-917d-d1e07d96d091)

---

## 📘 Project Overview

The **Restaurant Chatbot** is a smart conversational AI assistant that enables users to place and track food orders through natural language. Built with **Google Dialogflow**, **FastAPI**, and **MySQL**, the chatbot streamlines the ordering experience by allowing users to add items, remove them, complete their order, and check order status — all through a user-friendly chat interface.

This project is intended as a backend-integrated AI prototype, with plans to embed it into a web-based food ordering system.

---

## ✅ Key Features

- 🧾 **Order Management**: Add, remove, and review food items in an ongoing order.
- 🛍️ **Order Completion**: Finalize and save orders to a MySQL database with total amount displayed.
- 🚚 **Order Tracking**: Check the status of a previously placed order using its order ID.
- 🧠 **Context Handling**: Supports multi-turn conversations with session tracking.
- 🗃️ **Database Integration**: Persistent backend via MySQL to manage real orders and item details.

---

## 💡 Project Purpose

This chatbot was developed as a part of a backend-integrated AI project to demonstrate real-time NLP-driven restaurant automation using Dialogflow and FastAPI.

---

## ⚙️ Setup Instructions

### Prerequisites

- Python 3.8+
- MySQL Server (e.g., MySQL 8.0)
- Ngrok (for HTTPS tunneling)
- Dialogflow agent setup

### Backend Setup (FastAPI)

1. Clone this repo and navigate to the backend directory:
   ```bash
   cd backend
Install dependencies:

bash
Copy
Edit
pip install fastapi uvicorn mysql-connector-python
Run the FastAPI server:

bash
Copy
Edit
uvicorn main:app --reload
Use ngrok to expose the server:

bash
Copy
Edit
ngrok http 8000
Paste the HTTPS ngrok URL into Dialogflow's Fulfillment section.

🧠 Dialogflow Configuration
Intents handled:

order.add - context: ongoing-order

order.remove - context: ongoing-order

order.complete - context: ongoing-order

track.order - context: ongoing-tracking

Enable webhook fulfillment for these intents in the Dialogflow console.

Extract the session ID from outputContexts to manage in-progress orders.

📦 Folder Structure
bash
Copy
Edit
RestaurantChatbot/
├── backend/
│   ├── main.py                # FastAPI app (webhook endpoint)
│   ├── db_helper.py           # Handles MySQL queries
│   ├── generic_helper.py      # Session and string utilities
│   └── extra/                 # Optional helper scripts
├── README.md
🔗 Deployment (Future Plan)
The chatbot is designed to be embedded into a web interface using Dialogflow Messenger or a custom chat UI, providing a complete AI-based restaurant ordering experience.

🛡️ License
This project is released under the MIT License, allowing free use, modification, and distribution.
