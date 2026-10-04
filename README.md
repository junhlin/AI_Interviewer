# Adaptive AI Technical Interviewer

> **An AI interviewer that learns what you know and decides what to ask next.**

Built for the **Nebius × NVIDIA Global AI Hackathon 2026**, this project uses **NVIDIA Nemotron through Nebius Token Factory** to create adaptive technical interviews for engineering candidates.

## 💡 How It Works

Unlike a traditional interview that follows a fixed question list, the system continuously builds a model of the candidate's knowledge.

```text
Question
   ↓
Candidate Answer
   ↓
Evaluate Understanding
   ↓
Update Skill Model
   ↓
Identify Knowledge Gap
   ↓
Choose Next Question
   ↓
Repeat
```

For example, if a candidate understands basic capacitors but struggles with parasitic inductance, the next question can specifically test that concept.

## 🎯 Core Features

* **Adaptive questioning** based on the candidate's previous answers
* **Candidate skill model** tracking strengths and weaknesses
* **Misconception detection**
* **Role-specific interviews** based on company and position
* **RAG** for company/role knowledge
* **Final diagnostic report**
* **NVIDIA model comparison** for quality, latency, and cost

## 🤖 NVIDIA Models

Different Nemotron models can handle different tasks:

| Model                  | Purpose                                        |
| ---------------------- | ---------------------------------------------- |
| **Nemotron Super**     | Reasoning, evaluation, misconception detection |
| **Nemotron Lightning** | Fast question generation and routine tasks     |
| **Nemotron Nano**      | Lightweight tasks                              |
| **Nemotron Ultra**     | Advanced reasoning / benchmarking              |

All models are accessed through **Nebius Token Factory**, so the application does not need to manage GPUs or model infrastructure.

## 🏗️ Architecture

```text
Frontend
Next.js / React
      ↓
FastAPI Backend
      ↓
Adaptive Interview Engine
      ↓
Nebius Token Factory
      ↓
NVIDIA Nemotron
      ↓
Candidate Knowledge Model
```

### Tech Stack

* **Frontend:** Next.js, React, TypeScript, Tailwind
* **Backend:** Python, FastAPI
* **AI:** Nebius Token Factory + NVIDIA Nemotron
* **Database:** PostgreSQL + pgvector
* **RAG:** Vector search + embeddings

## 🚀 Roadmap

* [ ] Connect to Nebius Token Factory
* [ ] Call Nemotron Super
* [ ] Build answer evaluator
* [ ] Create candidate skill model
* [ ] Implement adaptive question selection
* [ ] Add role/company RAG
* [ ] Compare Nemotron models
* [ ] Build final interview UI

## 🏆 Core Idea

This is **not just an AI that generates interview questions**.

> **Every answer becomes evidence that changes what the interviewer asks next.**

The goal is to create an interview that **learns about the candidate while the interview is happening.**
