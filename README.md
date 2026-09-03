# Infosys_Agentic AI for Franchise Management System

# FranchiseOps AI

### Agentic AI Platform for Intelligent Franchise Management

FranchiseOps AI is an **agentic AI-powered franchise management platform** designed to help multi-outlet businesses make faster, data-driven decisions across workforce, inventory, marketing, compliance, customer sentiment, and operations.

The platform combines **Machine Learning, Retrieval-Augmented Generation (RAG), database-grounded analysis, multilingual AI, and specialized AI agents** into a single Streamlit-based application.

---

## 🚀 Key Features

* 🤖 **9 Specialized AI Agents** for franchise operations
* 📊 **Machine Learning-based predictions and analytics**
* 🗄️ **Database-grounded responses using SQL retrieval**
* 📚 **RAG-based document question answering**
* 🌍 **Multilingual interaction using NLLB-200**
* 🧠 **Qwen2.5-powered AI responses**
* 🔍 **FAISS-based semantic document retrieval**
* 🛡️ **Grounded AI responses to reduce hallucinations**
* 📈 Interactive dashboards and business analytics
* ⚡ Natural-language Copilot for querying franchise data
* 🔐 Authentication using JWT and bcrypt

---

## 🧩 AI Agents

FranchiseOps AI consists of nine specialized agents:

| Agent                                  | Purpose                                                              |
| -------------------------------------- | -------------------------------------------------------------------- |
| **Agent 1 – Workforce Intelligence**   | Employee attrition and workforce analysis                            |
| **Agent 2 – Outlet Intelligence**      | Outlet health, revenue and performance monitoring                    |
| **Agent 3 – Inventory & Supply Chain** | Demand forecasting, stockout risk and safety-stock analysis          |
| **Agent 4 – Marketing Intelligence**   | Campaign ROI, customer acquisition and channel analysis              |
| **Agent 5 – Customer Sentiment**       | Customer feedback and sentiment analysis                             |
| **Agent 6 – Compliance & Audit**       | Compliance monitoring, anomaly detection and audit support           |
| **Agent 7 – Executive Digest**         | Management-level summaries and business insights                     |
| **Agent 8 – Translation**              | Multilingual translation of franchise information and SOPs           |
| **Agent 9 – Document RAG Studio**      | Question answering over SOPs, contracts and other uploaded documents |

---

## 🏗️ System Architecture

```text
                         ┌──────────────────────┐
                         │      User / Admin    │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │   Streamlit UI       │
                         │  Multilingual Copilot│
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │    Agent Router      │
                         └──────────┬───────────┘
                                    │
             ┌──────────────────────┼──────────────────────┐
             │                      │                      │
             ▼                      ▼                      ▼
      ┌─────────────┐       ┌──────────────┐       ┌─────────────┐
      │ SQL / DB    │       │ RAG / FAISS  │       │ ML Models   │
      │ Retrieval   │       │ Retrieval    │       │ Prediction  │
      └──────┬──────┘       └──────┬───────┘       └──────┬──────┘
             │                     │                      │
             └─────────────────────┼──────────────────────┘
                                   ▼
                         ┌──────────────────────┐
                         │     Qwen2.5 LLM      │
                         │ Grounded Generation  │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │ Verified AI Response │
                         └──────────────────────┘
```

---

## 🧠 Grounded AI Approach

A key feature of FranchiseOps AI is that the Copilot does **not directly generate answers from the language model alone**.

For a user query:

1. The Copilot identifies the appropriate agent.
2. Relevant information is retrieved from the database and/or documents.
3. SQL queries are used for structured franchise data.
4. FAISS/RAG retrieves relevant document knowledge.
5. Retrieved evidence is provided to the language model.
6. Qwen2.5 generates the final response.
7. If sufficient evidence is unavailable, the system avoids inventing information.

This approach helps provide **more reliable and evidence-based responses**.

---

## 🛠️ Technology Stack

| Category              | Technology                     |
| --------------------- | ------------------------------ |
| Frontend              | Streamlit                      |
| Backend/API           | FastAPI                        |
| Database              | SQLite                         |
| Authentication        | JWT, bcrypt                    |
| Machine Learning      | Scikit-learn                   |
| LLM                   | Qwen2.5                        |
| Translation           | NLLB-200                       |
| Vector Search         | FAISS                          |
| RAG                   | Retrieval-Augmented Generation |
| Data Processing       | Pandas, NumPy                  |
| Visualization         | Plotly                         |
| Tunneling             | ngrok                          |
| Deployment/Networking | Cloudflare                     |
| Model Hub             | Hugging Face                   |

---

## 📁 Project Structure

```text
FranchiseOps-AI/
│
├── franchise_app/
│   ├── agent1_workforce.py
│   ├── agent2_outlet.py
│   ├── agent3_franchise.py
│   ├── agent4_marketing.py
│   ├── agent5_sentiment.py
│   ├── agent6_audit.py
│   ├── agent7_executive.py
│   ├── agent8_translation.py
│   ├── agent9_rag.py
│   │
│   ├── db.py
│   ├── llm_engine.py
│   └── ...
│
├── data/
│   └── ...
│
├── documents/
│   └── ...
│
├── requirements.txt
├── README.md
└── ...
```

> Adjust the filenames above to match the exact files in your repository.

---

## 📊 Agent 3 – Inventory Intelligence

Agent 3 focuses on inventory and supply-chain decision making.

### Capabilities

* Demand forecasting
* Stockout risk prediction
* Safety-stock simulation
* Inventory anomaly detection
* SKU-level analysis
* Comparison of multiple ML models

### ML Models

The implementation uses models such as:

* Random Forest Regressor
* Gradient Boosting Regressor
* Linear Regression
* Ridge Regression
* Support Vector Regression
* Decision Tree Regressor
* MLP Regressor
* Isolation Forest

---

## 📢 Agent 4 – Marketing Intelligence

Agent 4 provides AI-driven campaign and customer acquisition analytics.

### Capabilities

* Campaign ROI forecasting
* Customer acquisition analysis
* CAC analysis
* Marketing channel comparison
* Budget simulation
* Campaign performance insights

### Marketing Channels

* Digital Ads
* Social Media
* Influencer
* Local Print
* Radio & TV
* Email Marketing

---

## 📚 Agent 9 – Document RAG Studio

Agent 9 enables users to ask questions about franchise-related documents.

Supported knowledge sources can include:

* Restaurant SOPs
* Franchise agreements
* Compliance documents
* FSSAI guidelines
* Operational manuals
* Uploaded PDF documents

### RAG Workflow

```text
PDF / Document
      │
      ▼
Document Extraction
      │
      ▼
Text Chunking
      │
      ▼
Embedding Generation
      │
      ▼
FAISS Vector Database
      │
      ▼
Similarity Search
      │
      ▼
Relevant Context
      │
      ▼
Qwen2.5
      │
      ▼
Grounded Answer
```

Example query:

> **When should employees wash their hands?**

The system retrieves the relevant section from the uploaded SOP and generates an answer based on the retrieved evidence.

---

## 🌍 Multilingual AI

FranchiseOps AI supports multilingual interaction through **Meta's NLLB-200 translation model**.

The workflow is:

```text
User Query
    ↓
Language Detection / Input
    ↓
NLLB-200 Translation
    ↓
AI Agent Processing
    ↓
Qwen2.5 Response
    ↓
NLLB-200 Translation
    ↓
Response to User
```

This allows franchise employees and managers to interact with the system in supported languages.

---

## 🔐 Authentication

The platform uses:

* **JWT** for authentication/session handling
* **bcrypt** for password hashing

This provides a basic authentication layer for accessing the franchise management platform.

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone <YOUR-GITHUB-REPOSITORY-URL>
cd FranchiseOps-AI
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

On Linux/macOS:

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file if your implementation requires API keys or model configuration.

Example:

```env
MODEL_NAME=Qwen/Qwen2.5-3B-Instruct
DATABASE_PATH=franchise.db
```

Do **not** commit API keys or passwords to GitHub.

---

## ▶️ Running the Application

Start the Streamlit application using:

```bash
streamlit run franchise_app/app.py
```

If your main application file has a different name, replace `app.py` with the correct entry point.

The application will open in your browser.

---

## 💬 Example Copilot Queries

Users can interact with the system using natural language.

Examples:

```text
Which outlets have the highest revenue?

Which products have the highest stockout risk?

What is the predicted demand for this SKU?

Which marketing channel has the best ROI?

What are the major customer complaints?

Show me outlets with compliance issues.

Give me an executive summary of franchise performance.

Translate this SOP into another language.

When should employees wash their hands?
```

---

## 🎯 Project Objectives

FranchiseOps AI aims to:

* Reduce manual franchise analysis
* Improve operational decision making
* Predict potential stockouts and workforce issues
* Monitor outlet performance
* Improve marketing decisions
* Analyze customer sentiment
* Support compliance and audits
* Enable multilingual communication
* Provide document-grounded answers
* Reduce unreliable or hallucinated AI responses

---

## 📈 Expected Impact

The platform is designed to help franchise organizations:

* Make faster business decisions
* Identify operational risks earlier
* Improve inventory planning
* Optimize marketing spending
* Improve customer experience
* Simplify compliance monitoring
* Give managers a unified AI interface for franchise operations

---

## 🔎 Reliability & Hallucination Control

FranchiseOps AI follows an evidence-first approach.

```text
User Question
      ↓
Identify Required Evidence
      ↓
Database / RAG Retrieval
      ↓
Evidence Validation
      ↓
LLM Generation
      ↓
Final Grounded Answer
```

The system is designed to distinguish between **verified information** retrieved from available data and generated strategic insights.

When relevant evidence is unavailable, the system should indicate that the information is unavailable instead of fabricating a result.

---

## 🚀 Future Enhancements

Potential future improvements include:

* Cloud database integration
* Real-time franchise data synchronization
* Advanced role-based access control
* Automated alert notifications
* Mobile application
* Advanced forecasting models
* Production-grade deployment
* Expanded multilingual support
* Automated compliance report generation

---

## 👥 Project

**FranchiseOps AI**

An AI-powered franchise operations platform combining:

**Agentic AI + Machine Learning + RAG + SQL Analytics + Multilingual AI**

---

## 📜 License

This project is developed for academic/project demonstration purposes.
