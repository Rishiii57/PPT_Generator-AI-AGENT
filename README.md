## LangChain Autonomous PPTX Agent

An AI agent built with LangChain that autonomously researches a topic, drafts an outline, generates custom images, and compiles everything into a ready-to-use `.pptx` PowerPoint file. **Its just the backend for now. I havent yet added the frontend to it**

---

## Overview

This project goes beyond simple text generation. It uses a **ReAct (Reasoning + Acting)** agent that can:

* Search the web for real-time information
* Generate relevant images
* Build a complete PowerPoint presentation automatically

Just provide a topic — the agent handles everything from research to final file creation.

---

## Features

*  **Web Search (DuckDuckGo)**
  Retrieves up-to-date information, facts, and statistics

*  **Image Generation (DALL·E 3)**
  Creates context-aware visuals for each slide

*  **Autonomous PPTX Generation (`python-pptx`)**
  Builds structured slides with titles, bullet points, and images

*  **ReAct Agent Workflow**
  Thinks step-by-step, decides tools, and executes tasks autonomously

---

##  Tech Stack

| Component        | Technology      |
| ---------------- | --------------- |
| Orchestration    | LangChain       |
| LLM              | OpenAI `gpt-4o` |
| Image Generation | DALL·E 3        |
| File Creation    | `python-pptx`   |
| Environment      | Python 3.8+     |

---

##  Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
```

### 2. Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Setup Environment Variables

Create a `.env` file:

```bash
touch .env
```

Add your API key:

```env
OPENAI_API_KEY=sk-your-actual-api-key-here
```

---

### 5. Run the Agent

Edit `main.py`:

```python
user_topic = "Your topic here"
```

Run:

```bash
python main.py
```

 Output:
A file named **`AI_Generated_Presentation.pptx`** will be generated.

---

##  How It Works (Architecture)

The agent follows a structured reasoning pipeline:

1. **Input**
   Receives a topic from the user

2. **Research Phase**
   Uses `web_search` tool to gather information

3. **Planning Phase**
   Generates slide structure (titles + bullet points)

4. **Image Generation**
   Calls DALL·E tool to create visuals

5. **Data Structuring**
   Converts everything into a JSON format

6. **Execution Phase**
   Uses `python-pptx` to generate the final `.pptx` file

---

##  Project Structure (Example)

```
.
├── main.py
├── tools/
│   ├── web_search.py
│   ├── image_generator.py
│   └── pptx_creator.py
├── requirements.txt
├── .env
└── README.md
```

---


##  Support

If you found this useful:

* Star  the repo
* Share with others
* Build  extensions on top of it

---

## Author

Rishiii57