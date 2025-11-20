# 🧠 VibeLearn: AI-Adaptive Learning Platform

### *Adapting education to your mood, energy, and knowledge gaps.*

[![VibeLearn Demo](<img width="320" height="180" alt="image" src="https://github.com/user-attachments/assets/bfa44795-458f-4814-afbc-58a702740f90" />
)](https://youtu.be/NuquJz_gWXs)
*(Click the image above to watch the full demo)*

---

## 🚀 Project Overview

**VibeLearn** is a full-stack RAG (Retrieval-Augmented Generation) application that personalizes study materials in real-time. Unlike standard "Chat with PDF" apps, VibeLearn uses a **multi-agent AI architecture** to restructure entire curriculums based on the user's emotional state and performance history.

**Status:** 🔒 *Proprietary Source Code (Available for review during interviews)*

---

## ⚙️ Technical Architecture

I engineered a cost-efficient pipeline to handle large-scale content generation without hitting API rate limits or cost spikes.

### 1. The "Architect & Builder" Pattern
To solve the problem of expensive LLM tokens, I split the generation process:
* **The Architect (Gemini 1.5 Pro):** Reads the full document context *once* to design a pedagogically sound, 10-topic course outline. High intelligence, low frequency.
* **The Builders (Gemini 1.5 Flash):** A background asynchronous task that generates the specific lesson content, key points, and quizzes for each topic in parallel loops. High speed, low cost.
* **Result:** Reduced API costs by **90%** and generation time by **9x** compared to single-model approaches.

### 2. The "Vibe-Aware" Engine
The backend adjusts the learning parameters based on user inputs (Mood/Energy):
* **Stressed/Low Energy:** Generates simplified analogies, encouraging tone, and enforces shorter study timers (Pomodoro adaptation).
* **Focused/High Energy:** Generates technical, dense explanations and enables extended deep-work timers.

### 3. The Adaptive Feedback Loop
* The system tracks user performance at the **topic level** (not just the quiz level).
* Failed concepts (<70% score) are automatically logged into a persistent **"Review Queue"**.
* The Dashboard dynamically links users back to the exact chunk of content they struggled with, closing the learning loop.

---

## 🛠️ Tech Stack

* **Frontend:** React, TypeScript, Tailwind CSS, Lucide React.
* **Backend:** Python, FastAPI, AsyncIO.
* **Database:** Supabase (PostgreSQL + pgvector for RAG retrieval).
* **AI Models:** Google Gemini 1.5 Pro (Reasoning), Gemini 1.5 Flash (High-Throughput).
* **Embedding:** SentenceTransformers (`all-MiniLM-L6-v2`).

---

## 📸 Screenshots

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/5d0929fa-cef9-4eed-a7b1-4c9f165a051e" />
<img width="1919" height="1076" alt="image" src="https://github.com/user-attachments/assets/f0a8b575-c75b-4a7e-9489-266f6cf9b20a" />
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/4ab5c31c-7b78-4f80-b47a-d64eccb79d6a" />
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/372b05d2-127c-4539-a81a-bad977febd43" />
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/9b759dc3-1faa-4c18-af20-43613308a2a0" />
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/a557b58e-2176-4c14-b98e-0e39778ae937" />
<img width="1919" height="979" alt="image" src="https://github.com/user-attachments/assets/69e82cbb-0522-4669-b9a9-3883169d6671" />
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/cfcd93a8-6c0a-49f9-9320-c60cba92061d" />
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/8c26f2ca-e1ce-4bf7-86ea-b8940bf110a1" />
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b9443048-c6c1-4c25-be43-646217d753d9" />
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b1ba2980-e1ca-47ce-9551-cf26c33f0b32" />

---

## 👨‍💻 About the Developer

Built by **Banda Sri Hari**. I am a Full-Stack Engineer passionate about building AI systems that solve real user problems.

* [LinkedIn](https://www.linkedin.com/in/sri-hari-48321b297/)
