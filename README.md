
# AI/ML Internship Assignment - Groq API

## Objective
This assignment demonstrates the implementation of two core tasks using **Groq APIs** (OpenAI SDK compatible):
1. **Conversation Management & Summarization**
2. **JSON Schema Classification & Information Extraction**

The purpose is to manage conversational data, perform summarization, and classify user chats with structured extraction using only standard Python and the OpenAI client.

---

## 📂 Repository Structure
```
AI_ML_Groq_Assignment/
│
├── Groq_Assignment.ipynb   # Main Google Colab notebook with full implementation
├── README.md               # This file
└── requirements.txt        # list of dependencies
```

---

## 🛠 Technologies Used
- **Python 3.x**  
- **OpenAI Python Client** (compatible with Groq API)  
- **Standard Libraries**: `os`, `json`, `requests`  
- **Groq API** for model access

---

## Task 1: Conversation Management & Summarization
**Features implemented:**
- Maintain a running conversation history of user-assistant chats.
- Summarize conversation after every `k` turns (`k=3` by default).
- Truncate conversation history by:
  - Number of turns
  - Number of characters

**Example usage:**
```python
conv = ConversationManager(k=3)
conv.add_message("user", "Hi, I want to learn about AI.")
conv.add_message("assistant", "Sure! AI means Artificial Intelligence.")
conv.add_message("user", "Can you tell me about Machine Learning?")
print(conv.history)
```

---

## Task 2: JSON Schema Classification & Information Extraction
**Features implemented:**
- Extract user information from chat (name, email, phone, location, age).  
- Validate output against a predefined JSON schema.

**Example usage:**
```python
chat_text = "Hi, I'm Alice Johnson, email: alice@mail.com, phone: 9876543210, 23 years old, Bangalore."
user_info = extract_info(chat_text)
print(user_info)
```

**Expected Output:**
```json
{
  "name": "Alice Johnson",
  "email": "alice@mail.com",
  "phone": "9876543210",
  "location": "Bangalore",
  "age": 23
}
```

---

## How to Run
1. Open the Google Colab notebook: [Groq_Assignment.ipynb](https://colab.research.google.com/drive/1OtvPCz43R_sFPRpdd8PjeIWkxQbStgJD?usp=sharing)  
2. Set your Groq API key:
```python
os.environ["GROQ_API_KEY"] = "YOUR_GROQ_API_KEY"

```python
os.environ["GROQ_API_KEY"] = "YOUR_GROQ_API_KEY"
```
3. Run all cells sequentially.  
4. Observe:
   - Conversation management and summarization in Task 1  
   - JSON schema extraction in Task 2  

---

## Notes
- No frameworks are used; only standard Python + OpenAI client.  
- Ensure your API key is valid and has access to `openai/gpt-oss-20b`.  
- Conversation summarization triggers automatically after every `k` turns.  
- Structured extraction guarantees JSON output according to the schema.

---

## Contact
**Name:** Roopendra Mardala
**Email:** mardalaroopendra@gmail.com  
**Phone:** 8519804772
