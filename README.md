# Resume JD SkillGap

AI-powered interview preparation platform that analyzes a candidate's resume against a job description and generates a personalized interview strategy.

**Live Demo:** https://resume-jd-skillgap.vercel.app
**GitHub:** https://github.com/abhinav-saha/resume_JD_skillgap

---

## Overview

Resume JD SkillGap helps candidates prepare for technical interviews by comparing their resume and profile against a target job description.

The application uses Google Gemini to analyze the candidate's background and generate:

* Resume-to-job match score
* Challenging technical interview questions
* Behavioral interview questions
* Skill gaps with severity levels
* Personalized preparation roadmap
* Tailored resume generation

User accounts and interview reports are stored using MongoDB.

---

## Features

* Upload resume as a PDF
* Enter a target job description
* Provide additional candidate information
* AI-powered resume and JD analysis
* Resume-to-job match score
* Challenging, role-specific technical questions
* Behavioral interview questions
* Skill-gap identification with severity levels
* Day-wise interview preparation roadmap
* User authentication using JWT
* Secure HTTP-only authentication cookies
* Persistent interview reports
* Generate a tailored resume PDF
* Responsive React dashboard

---

## How It Works

```text
                    ┌──────────────────────┐
                    │    React Frontend    │
                    │       Vercel         │
                    └──────────┬───────────┘
                               │
                             Axios
                               │
                               ▼
                    ┌──────────────────────┐
                    │    Express Backend   │
                    │       Render         │
                    └──────────┬───────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
              ▼                ▼                ▼
        Resume PDF       Job Description    User Profile
        Extraction
              │                │                │
              └────────────────┼────────────────┘
                               ▼
                    ┌──────────────────────┐
                    │     Google Gemini    │
                    │     Generative AI    │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │  Structured Report   │
                    ├──────────────────────┤
                    │ Match Score          │
                    │ Technical Questions  │
                    │ Behavioral Questions │
                    │ Skill Gaps           │
                    │ Preparation Plan     │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │     MongoDB Atlas    │
                    │   Report Persistence │
                    └──────────────────────┘
```

---

## AI Interview Report

Each generated report contains:

### Match Score

A score from 0–100 representing how closely the candidate's profile matches the target role.

### Technical Questions

Six challenging, role-specific technical questions designed around the candidate's resume and job description.

Each question includes:

* Interview question
* Interviewer's intention
* Model answer and recommended approach

### Behavioral Questions

Six challenging behavioral questions focused on areas such as:

* Ownership
* Decision-making
* Conflict resolution
* Failures
* Ambiguity
* Technical disagreements

### Skill Gaps

Identifies missing or insufficient skills and categorizes their severity as:

* Low
* Medium
* High

### Preparation Roadmap

Generates a day-wise preparation plan containing:

* Focus area
* Tasks
* Recommended preparation approach

---

## Tech Stack

### Frontend

* React
* React Router
* Axios
* SCSS
* Vite

### Backend

* Node.js
* Express.js
* MongoDB
* Mongoose
* JWT
* bcryptjs
* Cookie Parser
* CORS
* Multer
* pdf-parse
* Puppeteer

### AI

* Google Gemini
* Google GenAI SDK
* Zod
* Zod-to-JSON-Schema

### Deployment

* Vercel — Frontend
* Render — Backend
* MongoDB Atlas — Database

---

## Project Structure

```text
resume_JD_skillgap/
│
├── BACKEND/
│   ├── src/
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── middlewares/
│   │   ├── models/
│   │   ├── routes/
│   │   └── services/
│   │
│   ├── .env
│   ├── package.json
│   └── server.js
│
├── FRONTEND/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── contexts/
│   │   ├── pages/
│   │   ├── services/
│   │   └── ...
│   │
│   ├── package.json
│   └── vite.config.js
│
├── .gitignore
└── README.md
```

---

## Authentication

Authentication is handled using:

* JWT
* HTTP-only cookies
* bcryptjs password hashing
* Authentication middleware
* Token blacklist for logout

The frontend communicates with protected backend routes using credentialed Axios requests.

---

## Local Setup

### 1. Clone the repository

```bash
git clone https://github.com/abhinav-saha/resume_JD_skillgap.git
cd resume_JD_skillgap
```

### 2. Backend

```bash
cd BACKEND
npm install
```

Create a `.env` file:

```env
MONGO_URI=your_mongodb_connection_string
GOOGLE_GENAI_API_KEY=your_gemini_api_key
JWT_SECRET=your_jwt_secret
```

Start the backend:

```bash
npm run dev
```

The backend runs locally on:

```text
http://localhost:3000
```

### 3. Frontend

Open another terminal:

```bash
cd FRONTEND
npm install
npm run dev
```

The frontend runs locally on:

```text
http://localhost:5173
```

---

## Deployment

The project is deployed as a monorepo:

```text
GitHub Repository
       │
       ├── BACKEND
       │      └── Render
       │
       └── FRONTEND
              └── Vercel
```

### Frontend

Hosted on Vercel:

https://resume-jd-skillgap.vercel.app

### Backend

Hosted on Render:

https://resume-jd-skillgap.onrender.com

The frontend communicates with the deployed Express API through Axios.

---

## Environment Variables

The following environment variables are required by the backend:

```env
MONGO_URI=
GOOGLE_GENAI_API_KEY=
JWT_SECRET=
```

Environment files are excluded from version control through `.gitignore`.

**Never commit API keys, database credentials, or JWT secrets to GitHub.**

---

## Future Improvements

* Multiple resume and job-description comparisons
* Interview report history improvements
* ATS keyword analysis
* Resume improvement suggestions
* More detailed interview preparation tracking
* Interview progress tracking
* Additional AI-powered career tools
* Production performance and caching improvements

---

## Author

**Abhinav Saha**

GitHub: https://github.com/abhinav-saha

---

## Project Status

**Live and actively developed.**
