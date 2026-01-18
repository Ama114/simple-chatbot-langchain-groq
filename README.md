# 🤖 Simple Context-Aware Chatbot with LangChain

A simple yet powerful AI chatbot built using **Python**, **LangChain**, and **Groq API** (Llama 3). This project demonstrates how to create a chatbot that remembers conversation history, moving from a basic Q&A bot to a context-aware assistant.

## 🚀 Features

* **Fast Responses:** Uses the Groq API for ultra-fast inference with the Llama 3 model.
* **LangChain Integration:** Uses LangChain primitives for prompt management and chaining.
* **Memory Implementation:** Manually handles conversation history to simulate a continuous chat experience.
* **Beginner Friendly:** Step-by-step code structure ideal for learning AI development.

## 🛠️ Tech Stack

* [Python](https://www.python.org/)
* [LangChain](https://www.langchain.com/)
* [Groq API](https://console.groq.com/)

## 🏗️ How We Built It (Step-by-Step)

Here is the logical flow of the project:

#### Step 1: Installation 📦
First, we install the necessary libraries (`langchain` and `langchain_groq`) to communicate with the AI model.

#### Step 2: Initialize the "Brain" 🧠
We set up the **Groq API** key and initialize the `ChatGroq` model (Llama 3). This gives our chatbot the intelligence to understand and generate text.

#### Step 3: Create Prompt Templates 📝
We define **Prompts** to guide the AI.
* *System Message:* Tells the AI how to behave (e.g., "You are a helpful assistant").
* *User Message:* The actual question asked by the user.

#### Step 4: Build the Chain 🔗
We use LangChain to connect the components:
`Prompt` -> `LLM (Model)` -> `Output Parser` (to get clean text).

#### Step 5: Add Memory (Context) 📂
A standard chatbot forgets everything after one question. To fix this, we created a **History List**.
1.  We save the User's question.
2.  We save the AI's answer.
3.  We send the *entire history* back to the model with the next question so it remembers who you are!

## 📋 Prerequisites

Before running the code, make sure you have:

1.  A Google Colab environment or local Python setup.
2.  A **Groq API Key** (Get it for free at [console.groq.com](https://console.groq.com/)).

## ⚙️ Installation

Install the required libraries:

```bash
pip install langchain -qU
pip install langchain_groq -qU
