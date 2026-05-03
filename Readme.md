# 🤖 LangGraph Stock Market Assistant

An intelligent AI agent built using **LangGraph, Groq (LLaMA 3), and Gradio** that can:

* Answer user queries
* Use tools (stock market lookup via Screener.in)
* Evaluate its own responses
* Iterate until the task meets defined success criteria

---

## 🚀 Features

* 🧠 **Agentic Workflow** using LangGraph
* 🛠️ **Tool Integration** (Stock data via Screener.in)
* 🔁 **Self-Evaluating Loop** (feedback-driven improvement)
* ⚡ **Fast Inference** using Groq (LLaMA 3 models)
* 💬 **Interactive UI** with Gradio
* 🧾 **Custom Success Criteria** for each query

---

## 🏗️ Architecture

The agent follows a structured loop:

User Input → Worker (LLM) → Tools (if needed) → Worker → Evaluator →
↳ Continue (if criteria not met)
↳ End (if completed / needs user input)

---

## 🧰 Tech Stack

* **LangGraph** – Agent workflow orchestration
* **LangChain** – LLM abstraction & tool binding
* **Groq API** – Fast LLaMA 3 inference
* **Gradio** – UI interface
* **BeautifulSoup + Requests** – Web scraping (Screener.in)
* **Python**

---

## 📦 Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/langgraph-stock-assistant.git
cd langgraph-stock-assistant
```

---

### 2. Install dependencies (using uv)

```bash
uv sync
```

*or*

```bash
pip install -r requirements.txt
```

---

### 3. Setup environment variables

Create a `.env` file in the root directory:

```env
GROQ_API_KEY=your_api_key_here
```

⚠️ Do NOT commit this file.

---

## ▶️ Running the App

```bash
python app.py
```

*or if using notebook:*

```bash
jupyter notebook
```

Then run all cells.

---

## 💡 Example Usage

**User Input:**

```
Get stock details for TCS
```

**Success Criteria:**

```
Include company fundamentals and key ratios
```

The agent will:

* Search stock data
* Use tools if needed
* Evaluate its response
* Improve until criteria is satisfied

---

## 🔐 Security Notes

* API keys are stored in `.env` (not committed)
* Never expose your keys publicly
* Rotate keys if accidentally leaked

---

## 📁 Project Structure

```
├── app.py / notebook.ipynb
├── tools/
├── .env              # ignored
├── .gitignore
├── requirements.txt
└── README.md
```

---

## 🚀 Future Improvements

* 🔄 Streaming responses (real-time typing)
* 📊 Better stock data extraction
* 🧠 Multi-agent collaboration
* 🌐 Deployment (HuggingFace / Docker)

---

## 🙌 Acknowledgements

* LangChain & LangGraph
* Groq API
* Gradio

---

## ⭐ If you like this project

Give it a star ⭐ on GitHub!
