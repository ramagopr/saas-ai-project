# AI SaaS – Business Idea Generator

A simple AI-powered SaaS application that generates startup business ideas using an LLM.

The application uses a **Next.js frontend**, a **Python FastAPI backend**, and **OpenAI GPT models** for idea generation. Deployment is handled using **Vercel serverless infrastructure**.

---

# Architecture

```
User Browser
      ↓
Next.js (React UI)
      ↓
FastAPI API (Python)
      ↓
OpenAI API
      ↓
Response returned to UI
```

### Components

**Frontend**

* Next.js (React + TypeScript)
* Handles user interaction and UI rendering

**Backend**

* FastAPI
* Handles API requests
* Calls OpenAI API

**AI Layer**

* OpenAI GPT models
* Generates business ideas

**Deployment**

* Vercel
* Serverless deployment
* Preview environments for branches

---

# Project Structure

```
saas-ai/
│
├── app/                # Next.js frontend
├── api/
│   └── index.py        # FastAPI backend
├── projects/           # Course exercises
├── README.md
```

---

# Environment Variables

You must configure the OpenAI API key.

Create a `.env` file:

```
OPENAI_API_KEY=your_openai_key_here
```

For **Vercel deployments**, add the environment variable in the Vercel dashboard:

```
OPENAI_API_KEY
```

---

# Running Locally

Install dependencies:

```
pip install fastapi openai uvicorn
npm install
```

Run the backend:

```
uvicorn api.index:app --reload
```

Run the frontend:

```
npm run dev
```

Open:

```
http://localhost:3000
```

---

# Deployment

This project is deployed using **Vercel**.

Deploy with:

```
vercel
```

Deployment flow:

```
Git Push
    ↓
Vercel Build
    ↓
Preview Deployment
    ↓
Merge to main
    ↓
Production Deployment
```

Preview deployments automatically get their own URL.

Example:

```
https://saas-ai-git-feature.vercel.app
```

---

# Production Deployment

Production deployments occur when changes are merged to the `main` branch.

```
git push origin main
```

Vercel automatically builds and deploys.

---

# Tech Stack

* Next.js
* React
* FastAPI
* OpenAI API
* Vercel
* TypeScript
* Python

---

# Future Improvements

* Database integration
* User authentication
* Prompt templates
* Multi-agent workflows
* Usage analytics
