# MindMate AI — AI Mental Wellness Companion
> **Hackathon Prototype** | Calm • Safe • Modern • Premium • Student Friendly • AI-Powered

MindMate AI is an empathetic, student-centered GenAI wellness companion built for academic hackathons. It assists students experiencing coursework pressure, fatigue, lack of focus, and daily routine challenges — functioning strictly as a supportive companion, **NOT** as a medical diagnosis or therapy system.

---

## 🌟 Live Demo & Quick Launch

### 1. Prerequisites
- **Node.js (v18+)**
- *(Optional)* Python 3.10+ if running the FastAPI backend.

### 2. Start Application (Single Step)
From the project root:
```bash
# Start backend server (Express on port 5000)
npm run server

# In another terminal: start frontend client (Vite on port 3000)
npm run client
```

Now open: **[http://localhost:3000](http://localhost:3000)** in your browser!

*(Alternatively, run the FastAPI backend using `python -m uvicorn main:app --reload` inside the `server/` directory).*

---

## 🚀 Hackathon Demo Mode
At the top of the interface, the **Judge Demo** toolbar provides 1-click execution for 5 essential student scenarios:
1. **Academic Stress**: 3 assignments due, tight deadlines -> Generates step-by-step triage & 4-4-4-4 Box Breathing.
2. **Poor Sleep**: Late-night phone doomscrolling & fatigue -> Generates 20-20-20 screen detox & hydration pauses.
3. **Difficulty Concentrating**: Brain fog & open tabs -> Generates 25-minute Pomodoro focus block.
4. **Feeling Overwhelmed**: Emotional exhaustion -> Generates grounding reflection & mindful journaling.
5. **Building a Healthy Routine**: Habit anchors, hydration, and study blocks.

---

## 📦 Curated Dataset

The complete structured dataset used by the prototype is located in:
📁 [`dataset/mental_wellness_dataset.json`](file:///c:/Users/AMD/OneDrive/Desktop/hackspace/dataset/mental_wellness_dataset.json)

It is also directly inspectable and downloadable in-app under the **Dataset Explorer** tab:
- **Conversational Scenarios**: Academic stress, sleep deprivation, procrastination, burnout, loneliness, imposter syndrome. Each scenario includes sample student utterances, non-clinical supportive suggestions, and linked activity IDs.
- **Safety Escalation Taxonomies**: Danger keyword triggers, crisis response protocols, and student idiom exemptions (e.g. *"this exam is killing me"*).
- **Wellness Activities Catalog**: 12 structured activities across Relax, Focus, Move, and Reflect categories.
- **Daily Habits & Goal Templates**: Hydration targets, focus blocks, movement breaks, screen-free time.
- **Campus & Crisis Support Schemas**: Institutional contact directory and 24/7 crisis lifelines.

---

## 🛡️ Safety & Crisis Escalation Protocol
MindMate AI enforces strict safety guardrails:
- Does **not** provide psychological diagnosis or clinical therapy.
- Non-medical disclaimers are prominently displayed across every page and chat interaction.
- If high-risk language or self-harm keywords are detected, the system immediately suspends standard dialogue and surfaces the **Crisis Modal** with direct 1-click buttons for:
  - **988 Suicide & Crisis Lifeline** (24/7 Call/Text)
  - **Crisis Text Line** (Text `HOME` to `741741`)
  - **The Trevor Project** (`1-866-488-7386`)
  - **Campus Security / Student Care Center**

---

## 🏗️ Architecture & Technology Stack
- **Frontend**: React 18, Vite, Tailwind CSS, Lucide React, Recharts, Canvas Confetti.
- **Backend API**:
  - Node.js Express server (`server/server.js`) with contextual intent matcher and safety classifier.
  - Python FastAPI alternative (`server/main.py`) with Pydantic models.
- **Audio Synthesizer**: Web Audio API ambient sound generator (Rain / Pink noise) & Web Speech API Text-to-Speech companion reader.
- **Data Privacy**: Client-side local storage isolation with a transparent **"Wipe Local History"** privacy control.
