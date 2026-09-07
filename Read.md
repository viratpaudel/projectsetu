# 🌉 PROJECT SETU

### **Bridging Silence with Intelligence.**

> 🧏‍♂️ **Real-Time Indian Sign Language → Voice AI Ecosystem**

**Project Setu** is an AI-powered accessibility platform that translates **dynamic Indian Sign Language (ISL)** into natural, expressive speech in real time — enabling seamless communication during **Google Meet, Zoom, Microsoft Teams**, and other meeting platforms.

---

## 💡 The Idea

Communication shouldn't depend on whether someone can hear or speak.

Existing video-conferencing platforms provide captions, but captions still force deaf participants to communicate through text, disrupting the natural flow of conversation.

**Setu changes that.**

Instead of:

> 🖐️ Sign → 📝 Caption → 👀 Read

Setu enables:

> 🖐️ **Sign → 🧠 Understand → ✨ Refine → 🔊 Speak**

Creating a much more natural conversational experience.

---

# 🚨 THE PROBLEM

Modern meeting platforms have accessibility features, but they don't provide a native way for a deaf participant using ISL to **speak naturally into a live audio channel**.

### Current limitations

* 📝 Captions require participants to constantly read
* 🧑‍🏫 Professional ISL interpreters can be expensive
* ⏳ Interpreters aren't always available on demand
* 🖐️ Many existing solutions focus on static signs
* 🎙️ Existing solutions don't seamlessly inject translated speech into live meetings

### 🌍 The Opportunity

**18M+ Indians** rely on Indian Sign Language as their primary language.

Project Setu aims to make digital communication more accessible with a target conversational latency of:

### ⚡ `< 250ms`

---

# 🚀 THE SOLUTION

Project Setu creates a complete **ISL → Voice communication pipeline**.

### 🖐️ 01 — CAPTURE

A webcam continuously captures:

* Hands
* Facial expressions
* Body posture
* Dynamic gestures

↓

### 🧠 02 — UNDERSTAND

MediaPipe Holistic extracts **543 landmarks per frame**, which are processed by a custom sequence model.

↓

### ✨ 03 — REFINE

The recognized gesture concepts are passed through a **local Llama 3 model** to transform fragmented output into grammatically natural language.

↓

### 🔊 04 — SPEAK

Sarvam AI Bulbul V3 generates localized speech and streams it into the meeting through a virtual audio device.

---

# 🧬 SYSTEM PIPELINE

```text
             🧏‍♂️ INDIAN SIGN LANGUAGE
                       │
                       ▼
                📷 WEBCAM INPUT
                       │
                       ▼
              👁️ MEDIA PIPELINE
             MediaPipe Holistic
                       │
                       ▼
             🧠 GESTURE ENGINE
              LSTM / GRU + TFLite
                       │
                       ▼
             💬 RAW ISL CONCEPTS
                       │
                       ▼
               ✨ LOCAL LLM
                Llama 3 / Ollama
                       │
                       ▼
             📝 NATURAL LANGUAGE
                       │
                       ▼
                 🔊 VOICE AI
              Sarvam Bulbul V3
                       │
                       ▼
              🎙️ VIRTUAL AUDIO
                       │
                       ▼
       ┌───────────────┼───────────────┐
       ▼               ▼               ▼
   Google Meet       Zoom           Teams
```

---

# 🔥 KEY FEATURES

### 🖐️ Dynamic ISL Recognition

Setu isn't designed around simple static alphabets.

It processes **hands + face + posture + movement** to understand dynamic sign sequences.

---

### 🧠 On-Device Gesture Intelligence

The gesture-recognition pipeline uses TensorFlow Lite for optimized local inference.

This means the core recognition stage can operate:

> **⚡ Fast · 🔒 Private · 📴 Offline**

---

### ✨ Context-Aware Language

Raw gesture recognition can produce fragmented concepts.

For example:

```text
"Me..."
"Station..."
"Go..."
"Now..."
```

Setu transforms this into:

> **"I need to go to the station now."**

The local Llama 3 model provides grammatical and contextual refinement before speech generation.

---

### 🇮🇳 Localized Indian Speech

Using **Sarvam AI Bulbul V3**, Setu can generate natural Indian speech with support for multilingual and code-mixed communication.

From:

> 🖐️ ISL

to:

> 🔊 Natural Indian Voice

---

### 🎙️ Works With Existing Meeting Platforms

Setu doesn't require custom plugins for every video-conferencing platform.

The generated speech is routed through a **virtual audio device**, allowing meeting software to recognize it as a normal microphone.

```text
AI Generated Speech
        ↓
Virtual Audio Cable
        ↓
      🎙️ Mic
        ↓
Google Meet / Zoom / Teams
```

---

# 🛠️ TECHNOLOGY

| Technology                    | Role                           |
| ----------------------------- | ------------------------------ |
| 👁️ **OpenCV**                | Real-time camera processing    |
| 🖐️ **MediaPipe Holistic**    | Hand, face & posture landmarks |
| 🧠 **TensorFlow / Keras**     | Deep learning                  |
| ⚡ **TensorFlow Lite**         | Optimized offline inference    |
| 🔢 **NumPy**                  | Landmark processing            |
| 🤖 **Ollama / Llama 3**       | Local language refinement      |
| 🔊 **Sarvam AI Bulbul V3**    | Multilingual speech generation |
| 🎙️ **PyAudio / SoundDevice** | Audio streaming                |
| 🔌 **VB-Audio Cable**         | Virtual microphone routing     |
| 🖥️ **Streamlit / React**     | Interface & dashboard          |

---

# 🧠 WHAT MAKES SETU DIFFERENT?

### 01 — 🖐️ 543-POINT VISION

MediaPipe Holistic tracks **543 hand, face and posture landmarks per frame**, giving the system a much richer understanding of human movement.

### 02 — 🧠 LOCAL AI

The core gesture recognition and language refinement pipeline can operate locally, reducing dependency on cloud processing.

### 03 — ✨ LANGUAGE UNDERSTANDING

Setu doesn't simply convert gestures into individual words.

It understands the sequence and uses an LLM to create **natural sentences**.

### 04 — 🔊 REAL-TIME SPEECH

Speech is streamed progressively instead of waiting for an entire conversation to finish.

### 05 — 🎙️ UNIVERSAL AUDIO OUTPUT

By using a virtual microphone, Setu can communicate with existing meeting software without requiring deep platform-level integration.

---

# ⚔️ SETU VS EXISTING SOLUTIONS

| Capability          | 📝 Live Captions | 🧑‍🏫 Human Interpreter | 🌉 **Project Setu** |
| ------------------- | :--------------: | :---------------------: | :-----------------: |
| Dynamic ISL         |         ❌        |            ✅            |          ✅          |
| Live Voice Output   |         ❌        |            ✅            |          ✅          |
| On Demand           |         ✅        |            ❌            |          ✅          |
| Low Cost            |         ✅        |            ❌            |          ✅          |
| Offline Core AI     |         ❌        |            ✅            |          ✅          |
| Localized Speech    |         ❌        |            ✅            |          ✅          |
| Meeting Integration |         ✅        |            ⚠️           |          ✅          |

---

# 🌍 THE IMPACT

Project Setu isn't just about translating gestures.

It's about giving people the ability to **participate in conversations naturally**.

### 🎓 Education

Make online classrooms more accessible.

### 💼 Professional Meetings

Allow deaf professionals to communicate without depending on a human interpreter for every conversation.

### 🏥 Remote Services

Enable more accessible digital consultations and support services.

### 🌐 Everyday Communication

Bring real-time ISL communication beyond specialized accessibility applications.

---

# 🔮 THE VISION

> **Setu means Bridge.**

A bridge between:

**🤟 Sign Language**

and

**🗣️ Spoken Language**

Between:

**♿ Accessibility**

and

**🌍 Opportunity**

Between:

**People**

and

**People.**

---

# 👥 TEAM BTC



## ❤️ Built With Purpose

### **Technology should remove barriers, not create them.**

🌉 **Project Setu**

> *Connecting every voice, even when it's spoken through a sign.*
