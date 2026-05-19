# GameMind-AI-Agent
GameMind is an elite, full-stack autonomous AI assistant specialized in video games. Powered by **Groq** and the **LLaMA 3.3 70B** model, it uses multi-turn tool orchestration to fetch real-time game updates and compute complex metrics like hardware bottlenecks. The application also supports advanced multimodal capabilities, allowing users to upload images  and process heavy PDF documents safely via an in-memory extraction pipeline with hard truncation guards.

---

## 🚀 Features

* **Autonomous Tool Orchestration:** Dynamically switches between conversational replies and execution of specialized Python tools (`get_game_latest_news`, `calculate_pc_bottleneck`).
* **Multimodal Input Support:** * **Vision Matrix:** Seamlessly handles image uploads by dynamically switching to the `meta-llama/llama-4-scout-17b-16e-instruct` model.
  * **PDF Guardrail Reader:** Parses PDFs in-memory with a hard string-character limit (20,000 characters) to prevent token overflow.
* **Localized Multi-Lingual Architecture:** Automatically detects user language and adapts response formatting structures dynamically (English, French, Arabic).
* **Advanced UI Workspace:** A modern, customizable web interface featuring three distinct styles (Dark, Light, Neon), persistent chat histories inside `localStorage`, and real-time typewriter content streaming.

---

## 🛠️ Tech Stack

### Frontend
* Semantic HTML5 & Dynamic CSS3 (CSS Variables, Grid, Responsive Design).
* Vanilla JavaScript (ES6+) utilizing asynchronous `Fetch API`.
* Local Storage API for session persistence.
<p align="center">
  <img src="https://github.com/user-attachments/assets/e3e3d55a-d0e7-4c57-b6c7-2c28b741b80e" width="32%" alt="Dark Theme Preview" />
  <img src="https://github.com/user-attachments/assets/48590b8e-bbcb-4f54-bde5-7d98f12e5fd9" width="32%" alt="Light Theme Preview" />
  <img src="https://github.com/user-attachments/assets/71ba97b3-2892-49cb-a512-9856543defa2" width="32%" alt="Neon Theme Preview" />
</p> 

### Backend
* **Flask** (Python 3.x web server environment).
* **Flask-CORS** (Cross-Origin Resource Sharing handling).
* **Groq SDK** (High-speed LLM inference gateway).
* **PyPDF (PdfReader)** (In-memory stream reading and token guard text parsing).


---

## 💻 Installation & Setup

### Prerequisites
* Python 3.8 or higher installed on your system.
* A Groq API key (Get one from the [Groq Console](https://console.groq.com/)).

### 1. Clone the Repository
git clone [https://github.com/Oumaima-Bahloul/GameMind-Agent.git](https://github.com/your-username/GameMind-Agent.git)
cd GameMind-Agent

### 2. Configure the Backend Server
Navigate to your backend files directory and install the necessary Python dependencies:
pip install flask flask-cors groq pypdf

 
### 3. Set up your Groq API authentication key in your operating system environment variables:
Linux/macOS:  export GROQ_API_KEY="your_actual_groq_api_key_here"
Windows (Command Prompt): set GROQ_API_KEY=your_actual_groq_api_key_here
Windows (PowerShell): PowerShell $env:GROQ_API_KEY="your_actual_groq_api_key_here"

Run the Flask application:python app.py
