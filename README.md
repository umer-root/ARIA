# ARIA — AI Email & Outreach Automation Agent

A full-stack AI agent for email automation, cold outreach, and lead management. Built with Python (Flask) + Claude AI.

---

## Features

- 📧 Cold email drafting
- 🔁 Multi-step outreach sequences
- ✉️ Subject line generation (A/B variants)
- 🔍 Email analysis & improvement
- 🌐 Prospect research & personalization
- 📋 Lead data extraction (JSON output)

---

## Project Structure

```
aria-agent/
├── app.py              # Flask backend
├── requirements.txt    # Python dependencies
├── static/
│   └── index.html      # Frontend UI
└── README.md
```

---

## Run Locally (Free)

### 1. Install dependencies
```bash
pip install -r requirements.txt
```

### 2. Set your Anthropic API key
```bash
# Mac/Linux
export ANTHROPIC_API_KEY=your-api-key-here

# Windows
set ANTHROPIC_API_KEY=your-api-key-here
```

Get a free API key at: https://console.anthropic.com

### 3. Start the server
```bash
python app.py
```

Open http://localhost:5000 in your browser.

---

## Deploy FREE on Render.com

1. Push this project to GitHub
2. Go to https://render.com → New Web Service
3. Connect your GitHub repo
4. Set:
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `python app.py`
   - **Environment Variable**: `ANTHROPIC_API_KEY` = your key
5. Click Deploy → Get a free public URL!

---

## Deploy FREE on Railway.app

1. Push to GitHub
2. Go to https://railway.app → New Project → Deploy from GitHub
3. Add environment variable: `ANTHROPIC_API_KEY`
4. Deploy → Get public URL

---

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/chat` | Send message to ARIA |
| POST | `/api/clear` | Clear session history |
| GET | `/api/health` | Health check |

### Chat Request Body
```json
{
  "message": "Write a cold email to a SaaS founder",
  "session_id": "unique-session-id",
  "task_type": "cold_email"
}
```

### Task Types
- `general` — Open chat
- `cold_email` — Draft cold emails
- `sequence` — Build email sequences
- `subject_lines` — Generate subject lines
- `analyze` — Improve existing emails
- `research` — Prospect research
- `extract` — Extract lead data as JSON

---

## Cost Estimate

- **Anthropic API**: ~$0.003 per 1K tokens (Claude Sonnet)
- **Hosting**: $0 on Render/Railway free tier
- **Typical usage**: ~$5–15/month for active use

---

Built with Claude AI by Anthropic.
