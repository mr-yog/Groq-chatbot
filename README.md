# Groq Chatbot 🚀

This project demonstrates how to build a simple **AI-powered chatbot** using the **Groq API** and the **LLaMA 3.3 70B Versatile model**. The chatbot processes user queries and returns intelligent responses in real-time.

## 🔧 Features
- Uses **Groq’s LLaMA 3.3-70B model**
- Handles natural language queries
- Lightweight and beginner-friendly
- Secure setup with environment variables
- Easy to extend for custom use cases

## 📂 Project Structure
├── Groq Chatbot.ipynb   # Jupyter Notebook with code and demo  
├── README.md            # Documentation  

## ⚡ Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/groq-chatbot.git
cd groq-chatbot
```

### 2. Install Dependencies
```bash
pip install groq
```

### 3. Set Up API Key Securely
Instead of hardcoding the key, store it in your environment variables:

#### Linux / macOS
```bash
export GROQ_API_KEY="your_api_key_here"
```

#### Windows (PowerShell)
```powershell
setx GROQ_API_KEY "your_api_key_here"
```

Then access it in your notebook:
```python
import os
from groq import Groq

api_key = os.getenv("GROQ_API_KEY")
client = Groq(api_key=api_key)
```

### 4. Run the Notebook
```bash
jupyter notebook Groq\ Chatbot.ipynb
```

## 🚀 Example Usage
```python
chat_completion = client.chat.completions.create(
    messages=[{"role": "user", "content": "Who is the Prime Minister of India?"}],
    model="llama-3.3-70b-versatile",
)
print(chat_completion.choices[0].message.content)
```

**Output:**
```
The current Prime Minister of India is Narendra Modi.
```

## 📌 Future Improvements
- Add **multi-turn conversations**
- Build a **web interface** (Streamlit/Gradio)
- Integrate with **messaging apps** like Slack, WhatsApp, or Telegram

## 📜 Project Description
A simple AI chatbot built with Groq API and LLaMA-3.3-70B. This project demonstrates how to connect to Groq securely using environment variables, process user queries, and generate intelligent responses. Easy to set up, extendable for multi-turn conversations, chat interfaces, or real-world applications.
