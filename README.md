# 🌸 VOICE4BLIND

### **Empowering Vision Through Voice**

> **A fully voice-controlled AI web application designed to help blind and visually-impaired learners access, navigate, understand, and listen to digital learning content.**

**No clicking. No typing. No visual cues required. 🎙️♿**

---

## 🌟 About Voice4Blind

**Voice4Blind** is an AI-powered accessibility platform created to make digital learning more independent and accessible for visually impaired users.

The application allows users to interact with documents completely through **voice commands**.

Users can:

* 🎤 Control the application using their voice
* 📄 Upload and open learning documents
* 📖 Read documents aloud
* 🧭 Navigate through sections using voice
* 🤖 Summarize lengthy content
* 💡 Get simplified explanations
* 📌 Listen to important points
* 🔊 Adjust reading speed and voice
* 🌐 Switch between multiple Indian languages
* 📊 Ask the system to describe visual elements such as graphs

---

# 🎯 Problem Statement

Visually impaired learners often face difficulties accessing digital educational content, especially lengthy documents, PDFs, notes, and other learning materials.

Traditional applications usually depend heavily on:

* Mouse clicks
* Keyboard input
* Visual buttons
* Screen navigation

**Voice4Blind** addresses this challenge by providing a **voice-first learning experience** where users can perform important actions through natural voice commands.

---

# 💡 Key Features

### 🎙️ Fully Voice-Controlled

The application is designed around voice interaction.

Users can navigate through the different screens and control document reading using spoken commands.

### 📚 Document Reading

Users can open learning documents and listen to their content through text-to-speech.

### 🤖 AI Summarization

Long sections can be summarized using AI, helping users understand important information quickly.

### 🧠 Simplified Explanation

Users can ask:

> **"Explain simply"**

to receive an easier-to-understand explanation of the current content.

### 📌 Important Points

Users can say:

> **"Important points"**

to extract the key information from the current section.

### 🧭 Voice Navigation

Users can navigate through documents using commands such as:

* `"Next"`
* `"Previous"`
* `"Open file 2"`
* `"Go back"`

### ⏯️ Reading Controls

Users can control speech using:

* `"Read"`
* `"Pause"`
* `"Resume"`
* `"Repeat"`
* `"Stop"`

### 🔊 Voice Controls

Users can adjust the reading experience with:

* `"Read slower"`
* `"Read faster"`
* `"Speak louder"`

### 🌐 Multilingual Support

Voice4Blind is designed to support multiple Indian languages, making the application more accessible to a wider range of learners.

### 📊 Visual Description

Users can ask:

> **"Describe the graph"**

to receive a spoken description of a visual element.

---

# 🏗️ Project Structure

```text
voice4blind/
│
├── frontend/
│   ├── index.html
│   │   └── Full multi-screen UI
│   │       ├── Welcome
│   │       ├── Login
│   │       ├── Dashboard
│   │       └── Reader
│   │
│   ├── style.css
│   │   └── Dark purple/violet theme
│   │
│   └── app.js
│       └── Complete voice pipeline
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
│       ├── intent_classifier.py
│       │   └── Pattern + Regex Intent Detection
│       │
│       ├── tts_engine.py
│       │   └── gTTS / pyttsx3 / Azure Neural TTS
│       │
│       └── document_processor.py
│           └── Text Extraction
│           ├── Text Chunking
│           └── Summarization
│
├── requirements.txt
│
└── README.md
```

---

# 🚀 Quick Start

## Option 1 — Run Frontend Standalone

The frontend can be opened directly in a supported browser.

Open:

```text
frontend/index.html
```

using **Google Chrome** or **Microsoft Edge**.

The browser's **Web Speech API** handles voice interaction.

### 🎤 Important

Allow **microphone access** when the browser asks for permission.

---

# ⚙️ Option 2 — Run with Backend

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

The FastAPI server runs at:

```text
http://localhost:8000
```

The frontend can be accessed through:

```text
http://localhost:8000/frontend/index.html
```

---

# 🔐 Environment Variables

Some advanced features can optionally use external AI and speech services.

Create a `.env` file inside the `backend/` directory:

```env
OPENAI_API_KEY=your_api_key
AZURE_SPEECH_KEY=your_key
AZURE_SPEECH_REGION=eastus
```

### Used For

| Variable              | Purpose                     |
| --------------------- | --------------------------- |
| `OPENAI_API_KEY`      | AI-powered summarization    |
| `AZURE_SPEECH_KEY`    | Azure Neural Text-to-Speech |
| `AZURE_SPEECH_REGION` | Azure Speech service region |

> API keys should never be committed to GitHub. Add `.env` to `.gitignore`.

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
| `"Open Maths Notes"` | Open a file by name  |
| `"Open file 2"`      | Open file by number  |
| `"Logout"`           | Logout               |

---

# 📖 Reader Commands

| Say                    | Action                      |
| ---------------------- | --------------------------- |
| `"Read"`               | Begin reading               |
| `"Start reading"`      | Begin reading               |
| `"Stop"`               | Pause/stop reading          |
| `"Pause"`              | Pause reading               |
| `"Wait"`               | Pause reading               |
| `"Resume"`             | Resume reading              |
| `"Continue"`           | Resume reading              |
| `"Repeat"`             | Repeat current section      |
| `"Say again"`          | Repeat current section      |
| `"Next"`               | Move to next section        |
| `"Skip"`               | Move to next section        |
| `"Previous"`           | Move to previous section    |
| `"Back"`               | Move to previous section    |
| `"Summarize"`          | Summarize current section   |
| `"Explain simply"`     | Give simplified explanation |
| `"Important points"`   | Read key points             |
| `"Read slower"`        | Decrease reading speed      |
| `"Read faster"`        | Increase reading speed      |
| `"Speak louder"`       | Adjust voice output         |
| `"Change to Kannada"`  | Switch to Kannada           |
| `"Change to Hindi"`    | Switch to Hindi             |
| `"Describe the graph"` | Describe visual content     |
| `"Logout"`             | Exit and logout             |

---

# 🌐 Supported Languages

Voice4Blind is designed with multilingual accessibility in mind.

| Language       | STT Code | TTS Code |
| -------------- | -------- | -------- |
| 🇺🇸 English   | `en-US`  | `en-US`  |
| 🇮🇳 Hindi     | `hi-IN`  | `hi-IN`  |
| 🇮🇳 Kannada   | `kn-IN`  | `kn-IN`  |
| 🇮🇳 Tamil     | `ta-IN`  | `ta-IN`  |
| 🇮🇳 Telugu    | `te-IN`  | `te-IN`  |
| 🇮🇳 Malayalam | `ml-IN`  | `ml-IN`  |
| 🇮🇳 Marathi   | `mr-IN`  | `mr-IN`  |
| 🇮🇳 Bengali   | `bn-IN`  | `bn-IN`  |
| 🇮🇳 Gujarati  | `gu-IN`  | `gu-IN`  |
| 🇮🇳 Punjabi   | `pa-IN`  | `pa-IN`  |
| 🇮🇳 Urdu      | `ur-PK`  | `ur-PK`  |
| 🇮🇳 Odia      | `or-IN`  | `or-IN`  |
| 🇮🇳 Assamese  | `as-IN`  | `as-IN`  |

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
                │ Detection       │
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
              │ GPT-4o-mini          │
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │ Text-to-Speech       │
              │ SpeechSynthesis      │
              │ gTTS / Azure TTS     │
              └──────────┬───────────┘
                         │
                         ▼
                    🔊 VOICE OUTPUT
                         │
                         ▼
                  🔄 LISTEN AGAIN
```

---

# 🔧 Core Backend Modules

## `main.py`

The main **FastAPI server** responsible for communication between the frontend and backend.

It provides:

* REST API endpoints
* WebSocket communication
* Document handling
* Backend request processing

---

## `intent_classifier.py`

Responsible for understanding user commands.

It uses **pattern matching and regular expressions** to identify intents such as:

```text
READ
PAUSE
RESUME
NEXT
PREVIOUS
REPEAT
SUMMARIZE
EXPLAIN
IMPORTANT_POINTS
CHANGE_LANGUAGE
LOGOUT
```

---

## `tts_engine.py`

Handles text-to-speech generation.

Supported engines include:

```text
gTTS
pyttsx3
Azure Neural TTS
```

This allows textual responses to be converted into spoken output.

---

## `document_processor.py`

Responsible for processing uploaded documents.

Main functions include:

* 📄 Text extraction
* ✂️ Text chunking
* 📚 Section processing
* 🤖 Summarization
* 📖 Content preparation for reading

---

# 🔊 Text-to-Speech Pipeline

Voice4Blind can use different speech engines depending on the deployment environment.

```text
Text
 │
 ├── Browser SpeechSynthesis
 │
 ├── gTTS
 │
 ├── pyttsx3
 │
 └── Azure Neural TTS
        │
        ▼
    🔊 Spoken Output
```

---

# 🔐 Demo Login Credentials

For demonstration purposes:

| Username | Password   |
| -------- | ---------- |
| `harini` | `1234`     |
| `demo`   | `demo`     |
| `user`   | `password` |

> These are demo credentials only and should not be used for production authentication.

---

# 🌍 Browser Compatibility

| Browser        | Support    |
| -------------- | ---------- |
| Google Chrome  | 🟢 Full    |
| Microsoft Edge | 🟢 Full    |
| Firefox        | 🟡 Partial |
| Safari         | 🟡 Partial |

### ⭐ Recommended

**Google Chrome on desktop** provides the best experience for browser-based speech recognition.

---

# ♿ Accessibility Design

Accessibility is the core principle of Voice4Blind.

The application is designed to minimize dependence on:

* 🖱️ Mouse interaction
* ⌨️ Keyboard input
* 👀 Visual navigation
* 🔘 Manual button selection

Instead, users can interact with the system using natural voice commands.

---

# 🔮 Future Enhancements

### 🤖 AI Improvements

* More advanced conversational AI
* Context-aware document questions
* Improved summarization
* Personalized learning assistance

### 🌐 Language Improvements

* Better multilingual speech recognition
* More Indian language support
* Improved regional pronunciation
* Language-aware summarization

### 📚 Document Improvements

* More document formats
* Automatic chapter detection
* Tables and image understanding
* Advanced graph and chart description

### 📱 Platform Improvements

* Android/iOS application
* Offline voice processing
* Cloud document storage
* User profiles and personalized libraries

### 🧑‍🦯 Accessibility Improvements

* Braille-device integration
* Assistive hardware integration
* Smart wearable support
* Improved screen-reader compatibility

---

# 🏆 Hackathon Project

**Voice4Blind** was developed as an accessibility-focused AI project for a hackathon, combining:

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
    VOICE4BLIND
```

#

---

# ❤️ Our Vision

We believe that **access to education should not depend on vision**.

Voice4Blind aims to use AI and voice technology to give visually impaired learners a more independent way to access and understand digital educational content.

> ### 🎙️ **"Empowering Vision Through Voice."**

---

# ⭐ Support the Project

If you find **Voice4Blind** useful or inspiring, consider giving the repository a ⭐ on GitHub.

### Made with ❤️ for accessible education.
