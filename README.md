# Enhanced Q&A Chatbot With Ollama

A simple yet powerful Q&A chatbot built using **Streamlit**, **LangChain**, and **Ollama**. This project allows you to interact with multiple open-source LLMs locally through Ollama.

---

## 🚀 Features

* Streamlit-based interactive UI
* Supports multiple open-source models (Gemma, Llama, DeepSeek, etc.)
* Customizable **temperature** & **max tokens**
* LangChain-powered prompt templating
* Easy local inference using **OllamaLLM**

---

## 📌 Project Structure

```
📦 Q&A-Chatbot
 ┣ 📜 app.py
 ┣ 📜 .env
 ┣ 📜 README.md
 ┗ 📦 (optional) requirements.txt
```

---

## ⚙️ Prerequisites

### 1. Install Python

Ensure Python **3.10+** is installed.

### 2. Install Ollama

Download & install:
[https://ollama.com/download](https://ollama.com/download)

Pull the required models:

```
ollama pull gemma:2b
ollama pull deepseek-r1:latest
ollama pull llama3.2:1b
```

### 3. Install Dependencies

Create and activate a virtual environment:

```
python -m venv venv
source venv/bin/activate        # Mac / Linux
venv\Scripts\activate           # Windows
```

Install packages:

```
pip install streamlit langchain langchain-core langchain-ollama python-dotenv
```

---

## 🔐 Environment Variables

Create a `.env` file:

```
LANGCHAIN_API_KEY=your_langchain_api_key_here
```

(Optional unless using LangSmith tracking)

---

## ▶️ Run the App

Start the Streamlit application:

```
streamlit run app.py
```

Open in browser:

```
http://localhost:8501
```

---

## 🧠 Usage

1. Select an LLM model from the sidebar.
2. Adjust temperature & max tokens.
3. Enter your question.
4. Receive an AI-generated response.

---

## 🛠️ Code Overview

### Main Logic: `generate_response()`

* Builds LangChain chain
* Runs selected Ollama model
* Returns formatted answer

### Prompt Template

```
System: You are a helpful assistant...
User: Question: {question}
```

---

## 📄 Included Models
