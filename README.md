# MeetMate: Your AI-Powered Meeting Assistant

MeetMate is an intelligent, end-to-end meeting automation system that helps professionals and teams stay organized and productive. MeetMate automates the tedious process of managing meeting information by processing meeting transcripts to generate clear, concise summaries and personalized to-do lists for each participant. Integrating directly with Google Calendar, Google Tasks, and Notion ensures that action items and important deadlines are seamlessly added as reminders or events, helping users stay organized and focused. In addition, the agent connects with **Gmail** to send each participant an email containing their assigned tasks and the overall meeting summary, making follow-ups effortless and keeping everyone in sync.

Ideal for busy professionals, teams, and project managers, this agent transforms raw meeting data into actionable insights—saving time, reducing manual note-taking, and boosting productivity by keeping everyone aligned and accountable.

---

## 🌐 Live Links

- **🔗 Demo Video:** [Watch here](https://drive.google.com/file/d/1TzbKXGIOua0ETbrMKlPqCACZD3IM9EVK/view?usp=sharing)
- **🧪 Live Preview:** [Ngrok Display Endpoint](https://21f5-49-207-210-189.ngrok-free.app/display)

---

## 🚀 Features

- 📋 Paste your meeting transcript
- 🧠 Get intelligent summaries and task extraction using GPT-4
- 📅 Auto-create Google Calendar events and Google Tasks for action items
- 📧 Receive personalized emails with summaries and tasks
- 📝 Notion integration to log meeting notes and tasks

---

## 🛠️ Tech Stack

| Layer         | Technology                     |
| ------------- | ------------------------------ |
| Frontend      | HTML, CSS, JavaScript          |
| Backend       | Python, Flask                  |
| AI Agents     | OpenAI GPT-4o                  |
| Orchestration | n8n (Workflows, Integrations)  |
| Hosting       | n8n Cloud, Ngrok, GitHub Pages |

---

## 📁 Folder Structure

```
MeetMate/
├── backend/
│   ├── app.py                 # Flask app to render HTML output
│   ├── templates/
│   │   └── result.html       # HTML template for output preview
├── frontend/
│   ├── index.html            # Main UI for uploading transcript
│   └── script.js             # Client-side JS for API calls
│   └── styles.css            # Stylesheet for frontend
├── venv/                     # Virtual environment
└── requirements.txt          # Python dependencies
```

---

## 🤖 Agents&#x20;

| Agent         | Description                                    | Input            | Output                  |
| ------------- | ---------------------------------------------- | ---------------- | ----------------------- |
| Summarizer    | GPT-4-based summarization of the transcript    | Transcript text  | Summary (string[])      |
| Extractor     | GPT-4-based task extraction from transcript    | Transcript text  | Tasks (name, task, due) |
| Notifier      | Sends summary & tasks via email                | Summary + Tasks  | Emails sent             |
| Scheduler     | Adds tasks to Google Calendar and Google Tasks | Task list        | Calendar events         |
| Notion Logger | Writes meeting summary into Notion database    | Summary (string) | Notion page             |

---

## 📌 Example Workflow

1. User uploads a transcript
2. n8n workflow triggers
3. Transcript is processed by GPT-4 (summary + task extraction)
4. Tasks sent to Google Calendar and Google Tasks
5. Summary and tasks emailed to users
6. Notes saved to Notion database
7. Final result preview rendered via Flask server

---

## ⚙️ Setup Instructions

### 1. Clone the Repo

```bash
git clone https://github.com/your-username/MeetMate.git
cd MeetMate
```

### 2. Create and Activate Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Start Flask Server

```bash
cd backend
python app.py
```

### 5. Serve Frontend

```bash
cd frontend
python3 -m http.server 3002
```

---

## 🧠 To Do / Improvements

•🎙️ **Live Meeting Participation**: Enable the agent to join virtual meetings (via platforms like Zoom, Google Meet, or Microsoft Teams) and transcribe conversations in real time using speech-to-text APIs.

•🔊 **Audio Input Support**: Extend input formats to include audio files (e.g., MP3, WAV), allowing users to upload recordings directly without needing pre-generated transcripts.

---

## 👩‍💻 Made By

**Sreekar**

- GitHub: [@electroNBS](https://github.com/electroNBS)
- LinkedIn: [Sreekar](https://www.linkedin.com/in/your-profile)

---

> MeetMate: Never miss a meeting detail again.

