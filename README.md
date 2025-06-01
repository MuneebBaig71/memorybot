
# 🧠 MemoryBot: Personalized AI Agent with CrewAI + Gemini

**MemoryBot** is a memory-augmented autonomous agent built using [CrewAI](https://docs.crewai.com), Google's **Gemini API**, and persistent memory mechanisms. It is designed to answer personalized questions about a user by leveraging both static knowledge from a file and dynamic memory layers.

---

## 📌 Features

- 🤖 **Intelligent Agent**: Uses Gemini Pro 1.5 via CrewAI to understand and respond.
- 📄 **User Knowledge**: Loads personal info from a `user_preference.txt` file.
- 💾 **Memory Layers**:
  - **Long-Term Memory**: Stored in a local SQLite database.
  - **Short-Term Memory**: Contextual awareness via RAG.
  - **Entity Memory**: Entity-specific memory management via RAG.
- 🔁 **Sequential Task Handling**: Modular and extendable task pipeline.

---

## 🚀 Setup Instructions

### 1. Clone the Repo
```bash
git clone https://github.com/MuneebBaig71/memorybot.git
cd memorybot
```

### 2. Create Virtual Environment (Optional)
```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

### 3. Install Requirements
```bash
pip install -r requirements.txt
```

### 4. Environment Variable

Create a `.env` file and add your Gemini API key:
```env
GEMINI_API_KEY=your_google_gemini_api_key
```

Or export it in your shell:
```bash
export GEMINI_API_KEY=your_google_gemini_api_key
```

### 5. Create `user_preference.txt`

Add some basic user info for the agent to learn:
```
Name: Muneeb
Location: Lahore
Likes: AI, Research, Programming
Dislikes: Noise
```

---

## 🧪 Run the Agent

In your Python script or REPL:
```python
from main import deploy

response = deploy()
print(response)
```

---

## 🗃️ Project Structure

```
memorybot/
├── main.py                   # Main script containing agent logic
├── user_preference.txt       # User data file
├── my_crew1/                 # Memory directories
│   ├── long_term_memory_storage.db
│   ├── short_term1/
│   └── (entity memory path)
├── .env                      # Gemini API key (not committed)
└── requirements.txt          # Python dependencies
```

---

## 🛠️ Built With

- [CrewAI](https://docs.crewai.com)
- [Google Gemini API](https://ai.google.dev/)
- [SQLite](https://www.sqlite.org/index.html)
- [RAG Memory](https://docs.crewai.com/memory/short-term)

---

## 📌 Notes

- This project is ideal for building personalized assistants or user-centric bots.
- You can adapt the `agent` and `task` definitions for any goal-oriented use case.

---

## 📄 License

MIT License © Muneeb Baig
