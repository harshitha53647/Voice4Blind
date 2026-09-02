# 🌸 VOICE4BLIND

### **Empowering Vision Through Voice**

> **A voice-controlled AI web application designed to help blind and visually impaired learners access, navigate, understand, and listen to digital learning content.**

**No clicking. No typing. No visual cues required. 🎙️♿**

---

## 🌟 About Voice4Blind

**Voice4Blind** is an AI-powered accessibility platform designed to make digital learning more accessible and independent for visually impaired users.

The application combines **Speech-to-Text, Natural Language Processing, Intent Recognition, Document Processing, AI Summarization, and Text-to-Speech** to create a voice-first learning experience.

Users can interact with the application using natural voice commands to:

* 🎤 Navigate the application
* 📄 Access learning documents
* 📖 Read documents aloud
* 🧭 Navigate between sections
* 🤖 Summarize lengthy content
* 💡 Get simplified explanations
* 📌 Listen to important points
* 🔊 Control reading speed
* 🌐 Switch languages
* 📊 Request descriptions of visual content

---

# 🎯 Problem Statement

Visually impaired learners often face challenges when accessing digital educational resources such as PDFs, notes, and lengthy documents.

Traditional applications rely heavily on:

* Mouse interaction
* Keyboard input
* Visual buttons
* Screen-based navigation

This can make independent learning difficult.

### 💡 Our Solution

**Voice4Blind** provides a voice-first interface where users can perform important actions through spoken commands.

Instead of manually navigating a document, a learner can simply say:

> 🎤 **"Read this document"**

or

> 🎤 **"Summarize this section"**

The system understands the command and responds through speech.

---

# 💡 Key Features

## 🎙️ Voice-Based Interaction

Users can control the application through natural voice commands without depending on traditional mouse or keyboard interaction.

---

## 📖 Document Reading

Users can open learning documents and listen to their contents through Text-to-Speech.

---

## 🤖 AI Summarization

Long sections of educational content can be summarized to help users quickly understand the most important information.

---

## 🧠 Intent Recognition

Voice commands are analyzed and classified using pattern matching and regular expressions.

Examples include:

```text
READ
PAUSE
RESUME
NEXT
PREVIOUS
REPEAT
SUMMARIZE
EXPLAIN
IMPORTANT POINTS
CHANGE LANGUAGE
LOGOUT
```

---

## 💡 Simplified Explanation

Users can say:

> **"Explain simply"**

to receive an easier explanation of the current content.

---

## 📌 Important Points

Users can say:

> **"Important points"**

to hear the key information from the current section.

---

## 🧭 Voice Navigation

Users can navigate through documents using commands such as:

* `"Next"`
* `"Previous"`
* `"Repeat"`
* `"Open file 2"`

---

## ⏯️ Reading Controls

Users can control document reading using:

* `"Read"`
* `"Pause"`
* `"Resume"`
* `"Repeat"`
* `"Stop"`

---

## 🔊 Voice Controls

Users can modify the reading experience with commands such as:

* `"Read slower"`
* `"Read faster"`
* `"Speak louder"`

---

## 🌐 Multilingual Support

Voice4Blind supports multiple Indian languages through speech recognition and text-to-speech technologies.

---

## 📊 Visual Description

Users can request descriptions of visual content such as graphs using voice commands.

Example:

> **"Describe the graph"**

---

# 🏗️ Project Structure

```text
voice4blind/
│
├── frontend/
│   ├── index.html
│   │   └── Multi-screen user interface
│   │       ├── Welcome
│   │       ├── Login
│   │       ├── Dashboard
│   │       └── Reader
│   │
│   ├── style.css
│   │   └── Dark purple/violet theme
│   │
│   └── app.js
│       └── Voice interaction pipeline
│           ├── Speech-to-Text
│           ├── Text-to-Speech
│           └── Intent Detection
│
├── backend/
│   ├── main.py
│   │   └── FastAPI server
│   │       ├── REST API
│   │       └── WebSocket
│   │
│   ├── uploads/
│   │   └── Uploaded documents
│   │
│   └── modules/
│       ├── _init_.py
│       ├── document_processor.py
│       │   └── Text extraction, chunking,
│       │       and summarization
│       │
│       ├── intent_classifier.py
│       │   └── Pattern + Regex intent detection
│       │
│       └── tts_engine.py
│           └── Text-to-Speech engines
│
├── requirements.txt
├── start.sh
└── README.md
```

---

# 🧠 System Architecture

```text
                    🎤 USER VOICE
                         │
                         ▼
                ┌─────────────────┐
                │  Speech-to-Text │
                │   Web Speech API│
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ Language        │
                │ Processing      │
                └────────┬────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │ Intent Recognition   │
              │ Pattern + Regex      │
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │ Action Handler       │
              │ app.js / main.py     │
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │ Document Processor   │
              │ Extraction + Chunking│
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │ AI Summarization     │
              │      AI Model        │
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │ Text-to-Speech       │
              │ Browser / gTTS /     │
              │ pyttsx3 / Azure      │
              └──────────┬───────────┘
                         │
                         ▼
                    🔊 VOICE OUTPUT
                         │
                         ▼
                  🔄 LISTEN AGAIN
```

---

# 🛠️ Technologies Used

| Technology          | Purpose                                         |
| ------------------- | ----------------------------------------------- |
| HTML5               | Frontend structure                              |
| CSS3                | User interface and accessibility-focused design |
| JavaScript          | Frontend logic and voice pipeline               |
| Web Speech API      | Speech recognition and browser TTS              |
| Python              | Backend development                             |
| FastAPI             | REST API and WebSocket server                   |
| NLP                 | Text and command processing                     |
| Regular Expressions | Intent classification                           |
| gTTS                | Text-to-Speech                                  |
| pyttsx3             | Offline Text-to-Speech option                   |
| Azure Neural TTS    | Advanced speech output                          |
| Document Processing | Text extraction and chunking                    |
| AI Summarization    | Summarizing educational content                 |

---

# 🔧 Backend Modules

## `main.py`

The main FastAPI backend responsible for communication between the frontend and backend.

It handles:

* REST API requests
* WebSocket communication
* Document processing requests
* Backend application logic

---

## `intent_classifier.py`

Responsible for identifying the user's intention from spoken commands.

It uses:

* Pattern matching
* Regular expressions
* Command classification

Examples:

```text
"Read"
"Next"
"Previous"
"Summarize"
"Repeat"
"Pause"
"Resume"
"Logout"
```

---

## `document_processor.py`

Responsible for processing uploaded learning documents.

Its responsibilities include:

* Text extraction
* Text cleaning
* Text chunking
* Section processing
* Summarization preparation

---

## `tts_engine.py`

Provides Text-to-Speech functionality.

Possible speech engines include:

```text
gTTS
pyttsx3
Azure Neural TTS
```

---

# 🚀 Quick Start

## Option 1 — Frontend Only

The frontend can be opened directly using a supported browser.

Open:

```text
frontend/index.html
```

using **Google Chrome** or **Microsoft Edge**.

Allow microphone access when prompted.

---

# ⚙️ Option 2 — Full Backend Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/voice4blind.git
```

### 2. Navigate to the Project

```bash
cd voice4blind
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

### 4. Activate the Environment

### Windows

```bash
venv\Scripts\activate
```

### Linux / macOS

```bash
source venv/bin/activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

### 6. Start the Backend

```bash
cd backend
python main.py
```

The backend runs on:

```text
http://localhost:8000
```

---

# 🎤 Voice Commands

## 🌸 Welcome Screen

| Say       | Action      |
| --------- | ----------- |
| `"Hi"`    | Start login |
| `"Hello"` | Start login |
| `"Ready"` | Start login |

---

## 🔐 Login

| Say                 | Action            |
| ------------------- | ----------------- |
| `"Username Harini"` | Set username      |
| `"Yes"`             | Confirm username  |
| `"Correct"`         | Confirm username  |
| `"Repeat"`          | Re-enter username |
| `"No"`              | Re-enter username |
| `"Password 1234"`   | Set password      |

---

## 🏠 Dashboard

| Say                  | Action               |
| -------------------- | -------------------- |
| `"Scan documents"`   | List available files |
| `"Open Maths Notes"` | Open file by name    |
| `"Open file 2"`      | Open file by number  |
| `"Logout"`           | Logout               |

---

## 📖 Reader

| Say                    | Action                    |
| ---------------------- | ------------------------- |
| `"Read"`               | Begin reading             |
| `"Start reading"`      | Begin reading             |
| `"Stop"`               | Stop reading              |
| `"Pause"`              | Pause reading             |
| `"Resume"`             | Resume reading            |
| `"Continue"`           | Continue reading          |
| `"Repeat"`             | Repeat current section    |
| `"Say again"`          | Repeat current section    |
| `"Next"`               | Next section              |
| `"Previous"`           | Previous section          |
| `"Summarize"`          | Summarize current section |
| `"Explain simply"`     | Simplify current section  |
| `"Important points"`   | Read key points           |
| `"Read slower"`        | Decrease reading speed    |
| `"Read faster"`        | Increase reading speed    |
| `"Speak louder"`       | Adjust voice output       |
| `"Change to Kannada"`  | Switch to Kannada         |
| `"Change to Hindi"`    | Switch to Hindi           |
| `"Describe the graph"` | Describe visual content   |
| `"Logout"`             | Exit and logout           |

---

# 🌐 Supported Languages

| Language  | STT Code | TTS Code |
| --------- | -------- | -------- |
| English   | `en-US`  | `en-US`  |
| Hindi     | `hi-IN`  | `hi-IN`  |
| Kannada   | `kn-IN`  | `kn-IN`  |
| Tamil     | `ta-IN`  | `ta-IN`  |
| Telugu    | `te-IN`  | `te-IN`  |
| Malayalam | `ml-IN`  | `ml-IN`  |
| Marathi   | `mr-IN`  | `mr-IN`  |
| Bengali   | `bn-IN`  | `bn-IN`  |
| Gujarati  | `gu-IN`  | `gu-IN`  |
| Punjabi   | `pa-IN`  | `pa-IN`  |
| Urdu      | `ur-PK`  | `ur-PK`  |
| Odia      | `or-IN`  | `or-IN`  |
| Assamese  | `as-IN`  | `as-IN`  |

---

# 🔐 Demo Credentials

| Username | Password   |
| -------- | ---------- |
| `harini` | `1234`     |
| `demo`   | `demo`     |
| `user`   | `password` |

> These credentials are for demonstration purposes only.

---

# 🌍 Browser Compatibility

| Browser        | Support    |
| -------------- | ---------- |
| Google Chrome  | 🟢 Full    |
| Microsoft Edge | 🟢 Full    |
| Firefox        | 🟡 Partial |
| Safari         | 🟡 Partial |

### ⭐ Recommended

**Google Chrome on desktop** is recommended for the best browser-based speech recognition experience.

---

# ♿ Accessibility

Accessibility is the primary goal of Voice4Blind.

The application aims to reduce dependency on:

* 🖱️ Mouse interaction
* ⌨️ Keyboard input
* 👀 Visual navigation
* 🔘 Manual button selection

Instead, users can interact with learning content using voice commands.

---

# 🔮 Future Enhancements

* 🌍 Improved multilingual support
* 🤖 Advanced conversational AI
* 📚 Question answering over documents
* 📊 Improved graph and image understanding
* 📱 Android and iOS applications
* ☁️ Cloud document storage
* 🎧 Offline voice processing
* 📖 Automatic chapter detection
* 🧑‍🦯 Assistive device integration
* ⠿ Braille device integration
* 👤 Personalized user profiles

---

# 🏆 Hackathon Project

Voice4Blind combines:

```text
Artificial Intelligence
        +
Natural Language Processing
        +
Speech Recognition
        +
Text-to-Speech
        +
Document Processing
        +
Accessibility
        ↓
    🌸 VOICE4BLIND
```

---

# 👥 Team

### Voice4Blind Team

* **Harshitha**
* **Mrudula**
* **Manasa**
* **Aishwarya**

---

# ❤️ Our Vision

We believe that **access to education should not depend on vision**.

Voice4Blind aims to use AI and voice technology to provide visually impaired learners with a more independent and accessible way to learn.

> ### 🎙️ **"Empowering Vision Through Voice."**

---

# ⭐ Support the Project

If you find **Voice4Blind** useful or inspiring, consider giving the repository a ⭐ on GitHub.

### Made with ❤️ for accessible education.
