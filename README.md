# 🧠 Emotion-Aware Chatbot with LangGraph and Ollama

This project implements a **multi-agent conversational chatbot** that classifies user messages as either **emotional** or **logical**, and routes them to the appropriate response agent accordingly. The system leverages **LangGraph**, **LangChain**, **Ollama**, and **structured output parsing** for accurate message classification and response generation.

---

## 🚀 Features

* 🌐 Uses **Ollama** with the **LLaMA 3** model for all LLM operations
* 🧠 **Message classification** into emotional or logical types using a custom structured model
* 💬 **Therapist agent** that responds with empathy and emotional support
* 📚 **Logical agent** that gives factual, analytical, and concise replies
* 🔄 Built using **LangGraph** for flexible agent orchestration
* 🔌 Uses `.env` support via `python-dotenv` for environment config

---

## 🛠️ Setup

### 1. Install Requirements

```bash
pip install langchain langgraph python-dotenv
```

Make sure you also have [Ollama](https://ollama.com/) installed and running locally, with the `llama3` model pulled:

```bash
ollama run llama3
```

### 2. Create a `.env` File

No sensitive keys are required for Ollama usage, but create a `.env` file for consistency:

```env
# .env
# Add other environment variables if needed
```

---

## 📄 Project Structure

```text
.
├── chatbot.py          # Main chatbot script
├── README.md           # Project documentation
├── .env                # Environment variables
```

---

## 📦 How It Works

1. User inputs a message.
2. Message is classified as either `"emotional"` or `"logical"` using the `MessageClassifier`.
3. Based on the classification:

   * **Therapist agent** provides emotional support.
   * **Logical agent** gives factual, to-the-point answers.
4. The assistant's reply is shown to the user.
5. The conversation continues until the user types `"exit"`.

---

## 🧪 Example Usage

```bash
$ python chatbot.py
Message: I'm feeling overwhelmed lately.
Assistant: I'm sorry to hear that you're feeling this way. It's completely valid to feel overwhelmed sometimes...
```

```bash
Message: What's the capital of Germany?
Assistant: The capital of Germany is Berlin.
```

---

## 🧼 To Exit

Type:

```
exit
```

---

## 📌 Notes

* You can customize the classification logic or response styles easily within the respective functions.
* This design is modular and extendable — perfect for multi-agent setups.

---

## 🧑‍💻 Author

**Ravindu Cooray**
Role: Developer / Designer / Engineer

---

Let me know if you want a version tailored for a GitHub page or including screenshots/logos.
