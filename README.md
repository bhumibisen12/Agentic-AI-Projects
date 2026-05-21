# 🤖 Nexus-COO Command Center

An Autonomous AI Operations Agent designed to act as a Virtual Chief Operating Officer (COO). This system monitors enterprise databases, automates supply chain decisions, analyzes competitor pricing, tracks logistics delays, and independently drafts & dispatches supplier communications through an interactive web dashboard.

---

## 🚀 Key Features

- **Autonomous Supply Chain Management**: Automatically detects low stock levels ($Current\_Stock < Reorder\_Level$) and creates context-aware purchase order (PO) drafts.
- **Competitor Pricing & Profit Optimization**: Queries live product tables to benchmark company pricing against competitors and returns real-time pricing strategy recommendations.
- **Logistics & Shipment Tracking**: Identifies delayed shipping routes and dynamically calculates risk mitigation paths.
- **Automated Email Pipeline**: Integrated with secure SMTP gateways (Gmail App Passwords / Mailtrap Sandbox) to send bulk automated business updates.
- **Interactive Control Center**: Built entirely on **Streamlit** with responsive quick-command action toggles and real-time database visualization state-tracking.

---

## 🛠️ Tech Stack & Architecture

- **Frontend & UI Engine**: Streamlit Framework
- **Core Brain & Reasoning**: LangGraph / State-Based Agentic Workflow
- **Large Language Model (LLM)**: Accessed securely via **OpenRouter API**
- **Database**: SQLite3 (Relational Management System)
- **Email Delivery Protocol**: Python `smtplib` + `email.mime` configurations

---

## 📁 Repository Structure

```text
├── app.py                  # Streamlit Web Dashboard UI & Session State Logic
├── nexus_coo_agent.py      # Core AI Agent Logic, Database Tooling, and Routing
├── email_sender.py         # Automated Email Gateway with Rate-Limit Padding
├── nexus_coo.db            # Local SQLite Database (Inventory, Products, Shipments)
└── README.md               # Project Documentation Terminal
```
## ⚙️ Configuration & Environment Variables

OPENROUTER_API_KEY="your_openrouter_llm_key_here"
GMAIL_USER="your_configured_account@gmail.com"
GMAIL_APP_PASSWORD="your_16_digit_google_app_password" # Generated via Google 2FA Security Terminal
# OR if sandboxing:
MAILTRAP_USER="your_mailtrap_smtp_username"
MAILTRAP_PASS="your_mailtrap_smtp_password"

## 🚀 How to Run Locally
1. Clone the Workspace
   git clone [https://github.com/bhumibisen12/Agentic-AI-Projects.git](https://github.com/bhumibisen12/Agentic-AI-Projects/new/main?filename=README.md))
cd Agentic-AI-Project

2. Install Dependencies
   pip install streamlit pandas sqlite3 secure-smtplib

3. Launch the Application Control Center
   streamlit run app.py

