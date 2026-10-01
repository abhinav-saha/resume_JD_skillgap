# Resume JD SkillGap

An AI-powered interview preparation platform that analyzes a candidate's resume against a job description and generates a personalized interview strategy.

The application uses Generative AI to identify skill gaps, generate challenging technical and behavioral interview questions, calculate a profile-to-job match score, and create a day-wise preparation roadmap.

---

## Features

- Upload your resume as a PDF
- Enter a job description
- Provide additional information about yourself
- AI-powered resume and job description analysis
- Match score between candidate profile and job
- Challenging, role-specific technical interview questions
- Behavioral interview questions
- Skill-gap identification with severity levels
- Personalized day-wise preparation roadmap
- User authentication
- Generate a tailored resume PDF
- Store interview reports using MongoDB

---

## Tech Stack

### Frontend

- React
- React Router
- Axios
- SCSS
- Vite

### Backend

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT
- bcryptjs
- Multer
- pdf-parse
- Puppeteer

### AI

- Google Gemini
- Google GenAI SDK
- Zod
- Zod-to-JSON-Schema

---

## How It Works


Resume PDF
     |
     v
React Frontend
     |
     | Axios
     v
Express Backend
     |
     +-- Resume Text Extraction
     |
     +-- Job Description
     |
     +-- Self Description
     |
     v
Google Gemini
     |
     v
Structured Interview Report
     |
     +-- Match Score
     +-- Technical Questions
     +-- Behavioral Questions
     +-- Skill Gaps
     +-- Preparation Roadmap
     |
     v
MongoDB
     |
     v
React Dashboard
