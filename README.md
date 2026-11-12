# 🕵️ The Last Question
### An AI-Powered Persian Detective Mystery Game

<p align="center">
  <strong>Every suspect has a story. Every answer hides a secret. Can you find the truth?</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-Backend-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/AI-Powered-8A2BE2?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Language-Persian-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-In%20Development-yellow?style=for-the-badge" />
</p>

---

## 🎬 About The Project

**The Last Question** is an AI-powered detective mystery game where players take on the role of an investigator solving a mysterious murder case.

Seven suspects. One victim. Countless secrets.

Your mission is to investigate the case, question every suspect, analyze their answers, discover hidden contradictions, and ultimately identify the murderer.

But be careful...

**Not everyone is telling the truth.**

Unlike traditional detective games with fixed dialogue options, this project is designed around AI-powered conversations. Players can ask questions in natural Persian, allowing investigations to feel more dynamic and interactive.

## 🎯 Game Features

- 🕵️ **Seven Suspects:** Investigate seven characters, each with their own identity and background.
- 💬 **AI-Powered Conversations:** Ask suspects questions using natural language.
- 🧠 **RAG-Based Knowledge:** Use character-specific documents as a knowledge source for investigations.
- 📁 **Case Information:** Access information about the victim, crime scene, estimated time of death, and available evidence.
- ⚖️ **Final Accusation:** Choose who you believe is responsible for the murder.
- ⏳ **Investigation Timer:** Solve the case before time runs out.
- 💾 **Local Chat History:** Preserve conversations in the browser using LocalStorage.
- 🌐 **Persian Interface:** A fully Persian, right-to-left gaming experience.
- 🎨 **Dark Detective UI:** A minimal dark interface with amber accents.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core backend logic |
| FastAPI | REST API and backend services |
| HTML5 | Game structure |
| Tailwind CSS | Responsive user interface |
| JavaScript | Frontend interactions |
| LocalStorage | Browser-side conversation history |
| RAG | Context-aware character conversations |

## 🧩 How It Works

The game follows a simple investigation workflow:

1. **Start the Investigation:** The player enters the case and reviews the available suspects.
2. **Choose a Suspect:** Select one of the seven characters.
3. **Ask Questions:** Send natural-language questions to the AI-powered backend.
4. **Analyze Responses:** Investigate the answers and compare statements.
5. **Review the Evidence:** Examine the case information and available clues.
6. **Make Your Accusation:** Select the suspected murderer and submit the final decision.

## 🧠 AI & RAG Architecture

The project uses a Retrieval-Augmented Generation (RAG) approach to support character-based investigations.

The general idea is to provide the AI with relevant character-specific information before generating an answer.

This helps keep conversations connected to the game's fictional world, character backgrounds, and investigation context.

**Conceptual workflow:**

```text
Player Question
      |
      v
   FastAPI
      |
      v
Retrieve Relevant Context
      |
      v
Character Knowledge
      |
      v
AI Response Generation
      |
      v
Response to Player
```

## 📂 Project Structure

```text
The-Last-Question/
│
├── app.py
│
├── templates/
│   └── index.html
│
├── data/
│   └── case/
│
├── rag_docs/
│   └── Character Knowledge
│
├── requirements.txt
│
└── README.md
```

*The exact structure may vary depending on the current project version.*

## 🚀 Getting Started

Follow these steps to run the project locally.

### 1. Clone the Repository

```bash
git clone https://github.com/rastin-pr/the-last-question.git
```

### 2. Enter the Project Directory

```bash
cd the-last-question
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it:

**Windows:**

```bash
venv\Scripts\activate
```

**Linux / macOS:**

```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure Environment Variables

If your backend uses external AI services, configure the required API credentials in a local `.env` file according to the variables expected by `app.py`.

**Important:** Never upload API keys, passwords, or private credentials to GitHub.

### 6. Run the Application

If the FastAPI application instance is named `app` inside `app.py`, run:

```bash
uvicorn app:app --reload
```

Open your browser:

```text
http://127.0.0.1:8000
```

## 🔌 API Endpoints

The game frontend communicates with the backend through REST API endpoints.

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/suspects` | Retrieve the suspects |
| GET | `/api/case` | Retrieve case information |
| POST | `/api/chat` | Send a question to a suspect |
| POST | `/api/accuse` | Submit the final accusation |

### Example Chat Request

```json
{
  "suspect_id": "amir",
  "message": "Where were you on the night of the murder?"
}
```

## 🎨 Design Philosophy

The interface is designed to create an immersive detective atmosphere.

- Dark navy backgrounds.
- Amber and gold highlights.
- Minimal and distraction-free layout.
- Persian typography using Vazirmatn.
- Right-to-left layout.
- Responsive design for different screen sizes.

## 🔮 Future Improvements

There is plenty of room to expand the investigation experience:

- [ ] More advanced RAG retrieval and contextual memory.
- [ ] More realistic and diverse suspect personalities.
- [ ] Dynamic clues and hidden evidence.
- [ ] Investigation notebook.
- [ ] Conversation-based contradiction detection.
- [ ] Multiple murder mystery cases.
- [ ] Improved mobile experience.
- [ ] Online deployment and persistent user progress.
- [ ] More advanced AI reasoning for detective investigations.

## 👨‍💻 Developer

Created with curiosity, creativity, and a passion for programming and artificial intelligence.

**Developer:** Rastin

## ⭐ Support

If you find this project interesting, consider giving it a ⭐ on GitHub.

Every investigation starts with one question.

**Are you ready to ask the last question?**

---

<p align="center">
  🕵️ <strong>The Last Question</strong>
  <br/>
  <i>Trust no one. Question everything.</i>
</p>
