# Todo Summary Assistant

A full-stack application to manage your to-do items, summarize pending tasks using OpenAI, and send the summary to a Slack channel.

## 🔧 Tech Stack

- **Frontend:** React
- **Backend:** Node.js + Express
- **Database:** Supabase (PostgreSQL)
- **LLM Integration:** OpenAI GPT-3.5
- **Slack Integration:** Incoming Webhook

---

## 🚀 Features

- Add, view, and delete personal to-dos
- Summarize all pending to-dos via OpenAI
- Send summary directly to a Slack channel
- Success/failure message on Slack operation

---

## 📦 Project Structure

```
project-root/
├── client/              # React frontend
│   └── src/App.jsx
├── server/              # Node.js backend
│   └── index.js
├── .env.example         # Environment variables sample
├── .env                 # Actual env file (not committed)
└── README.md
```

---

## 🔑 Environment Variables

Create a `.env` file in the `server` directory with the following variables:

```
SUPABASE_URL=https://your-project.supabase.co
SUPABASE_KEY=your-supabase-service-role-key
OPENAI_API_KEY=your-openai-api-key
SLACK_WEBHOOK_URL=https://hooks.slack.com/services/your/webhook/url
PORT=5000
```

> 📁 Example `.env.example` file:
```env
SUPABASE_URL=
SUPABASE_KEY=
OPENAI_API_KEY=
SLACK_WEBHOOK_URL=
PORT=5000
```

---

## 🛠️ Setup Instructions

### Backend
```bash
cd server
npm install
node index.js
```

### Frontend
```bash
cd client
npm install
npm run dev  # Or npm start depending on your setup
```

Make sure to proxy `/api` calls to your backend server in development.

---

## 🧠 OpenAI Setup
- Go to https://platform.openai.com/account/api-keys
- Create a free-tier account and get your API key.
- Add it to `.env` as `OPENAI_API_KEY`

---

## 💬 Slack Setup
- Go to https://api.slack.com/messaging/webhooks
- Create an incoming webhook for your Slack channel
- Copy the webhook URL
- Add it to `.env` as `SLACK_WEBHOOK_URL`

---

## 🗃️ Supabase Setup
1. Go to https://supabase.com/ and create a free project
2. Create a `todos` table with the following schema:

```sql
CREATE TABLE todos (
  id uuid DEFAULT uuid_generate_v4() PRIMARY KEY,
  text TEXT NOT NULL,
  created_at TIMESTAMP DEFAULT now()
);
```

3. Copy the project URL and service role API key into your `.env`

---

## 🌐 Deployment (Optional)
- Deploy frontend using Vercel, Netlify, or Firebase Hosting
- Host backend using Supabase Edge Functions or Render

---

## 📬 Contact
For queries, feel free to reach out.

---

Happy coding! 🚀

# .env.example
Anvesh chary - Vaagdevi College of Engineering - FULLSTACK
