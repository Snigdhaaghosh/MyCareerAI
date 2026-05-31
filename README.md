# MyCareerAI

MyCareerAI is an AI-powered career development, resume intelligence, and candidate management platform designed to help students, freshers, professionals, and recruiters streamline the hiring and career-building process.

The platform enables users to create professional resumes manually, upload resumes for AI analysis, identify skill gaps, optimize ATS compatibility, manage portfolios, showcase projects, and receive personalized career recommendations. Recruiters can efficiently evaluate candidate profiles, analyze skills, and identify the most suitable candidates.

MyCareerAI combines Artificial Intelligence, Natural Language Processing (NLP), resume parsing, semantic skill extraction, and career intelligence to create a complete ecosystem for career growth and talent acquisition.

---

# Table of Contents

* Overview
* Problem Statement
* Objectives
* Features
* System Architecture
* Technology Stack
* Project Workflow
* Database Design
* Installation Guide
* Environment Variables
* Running the Application
* Deployment
* Folder Structure
* Future Enhancements

---

# Problem Statement

In today's competitive job market, job seekers often struggle to create professional resumes, understand industry requirements, identify skill gaps, and effectively present their achievements.

Recruiters and hiring teams face challenges in manually screening large numbers of resumes, evaluating candidate skills, and finding the most suitable profiles.

MyCareerAI addresses these challenges by providing:

* AI-powered resume analysis
* ATS compatibility evaluation
* Resume quality assessment
* Skill gap identification
* Career recommendations
* Portfolio management
* Candidate profile standardization
* Intelligent candidate evaluation

The platform improves employability for candidates while helping recruiters make informed hiring decisions.

---

# Objectives

* Build an intelligent resume analysis platform.
* Enable manual resume creation and editing.
* Provide ATS score evaluation.
* Extract and categorize skills automatically.
* Recommend profile improvements.
* Help candidates identify skill gaps.
* Centralize education, projects, certifications, and portfolio information.
* Support recruiter-side candidate analysis.
* Create a scalable career development ecosystem.

---

# Key Features

## Candidate Features

### Resume Upload

Upload resumes in:

* PDF
* DOCX
* TXT

Supported processing:

* Resume parsing
* Information extraction
* Skill detection

### Manual Resume Builder

Create professional profiles manually by entering:

* Personal Information
* Education
* Work Experience
* Skills
* Projects
* Certifications
* Achievements
* Portfolio Links

### Profile Dashboard

Manage:

* Personal profile
* Resume details
* Projects
* Certifications
* Work history

### ATS Resume Analysis

Analyze:

* Resume quality
* ATS compatibility
* Keyword optimization
* Missing sections

### Skill Gap Analysis

Identify:

* Missing technical skills
* Industry-relevant competencies
* Suggested learning paths

### Career Recommendations

Receive AI-generated suggestions for:

* Career growth
* Resume improvement
* Professional development

### Portfolio Management

Add and showcase:

* GitHub repositories
* LinkedIn profile
* Portfolio websites
* Project demonstrations
* Work samples

---

## AI Features

### Resume Parsing

Automatically extract:

* Name
* Email
* Phone Number
* Skills
* Education
* Experience
* Certifications

### Skill Extraction

Detect:

* Technical Skills
* Soft Skills
* Tools & Technologies
* Domain Expertise

### AI Recommendations

Generate:

* Resume improvement suggestions
* Profile enhancement recommendations
* Career development guidance

### ATS Optimization

Evaluate:

* Resume structure
* Keyword relevance
* Content completeness
* Professional formatting

---

## Recruiter Features

### Candidate Search

Search candidates using:

* Skills
* Experience
* Education
* Certifications

### Candidate Evaluation

Review:

* Candidate profiles
* Resume quality
* Portfolio strength
* Skill distribution

### Candidate Ranking

Compare candidates based on:

* Skills
* Experience
* Projects
* Certifications
* ATS score

---

# System Architecture

```text
                    +-------------------+
                    |       User        |
                    +---------+---------+
                              |
          +-------------------+-------------------+
          |                                       |
          v                                       v

 +-------------------+               +----------------------+
 | Resume Upload     |               | Resume Builder       |
 | PDF / DOCX / TXT  |               | Manual Entry Forms   |
 +---------+---------+               +----------+-----------+
           |                                     |
           +----------------+--------------------+
                            |
                            v

                 +-----------------------+
                 | Data Processing Layer |
                 +-----------+-----------+
                             |
                             v

                 +-----------------------+
                 | Resume Parsing Engine |
                 +-----------+-----------+
                             |
                             v

                 +-----------------------+
                 | AI Analysis Engine    |
                 | NLP & Skill Detection |
                 +-----------+-----------+
                             |
                             v

                 +-----------------------+
                 | Firebase Database     |
                 +-----------+-----------+
                             |
                             v

                 +-----------------------+
                 | ATS Evaluation Module |
                 +-----------+-----------+
                             |
                             v

                 +-----------------------+
                 | Recommendation Engine |
                 +-----------+-----------+
                             |
                             v

                 +-----------------------+
                 | User Dashboard        |
                 +-----------------------+
```

---

# Technology Stack

## Frontend

* React.js
* Vite
* Tailwind CSS
* JavaScript

## Backend

* Node.js
* Express.js

## Database

* Firebase Firestore

## Authentication

* Firebase Authentication

## AI Integration

* Google Gemini API
* NLP-based Resume Analysis

## Cloud Storage

* Firebase Storage

## Deployment

* Vercel

---

# Project Workflow

### Step 1: User Registration

Users create an account using:

* Email Authentication
* Firebase Authentication

### Step 2: Resume Creation

Users can:

* Upload existing resume
  OR
* Create resume manually

### Step 3: Data Processing

System extracts:

* Candidate information
* Skills
* Education
* Experience

### Step 4: AI Analysis

AI evaluates:

* Resume quality
* Skill distribution
* ATS compatibility

### Step 5: Recommendations

Generate:

* Resume suggestions
* Career advice
* Missing skill recommendations

### Step 6: Dashboard

Display:

* Analysis results
* ATS score
* Career insights

---

# Database Design

## Users Collection

```json
{
  "uid": "",
  "name": "",
  "email": "",
  "phone": "",
  "linkedin": "",
  "github": "",
  "portfolio": ""
}
```

## Education Collection

```json
{
  "institution": "",
  "degree": "",
  "field": "",
  "startYear": "",
  "endYear": ""
}
```

## Experience Collection

```json
{
  "company": "",
  "position": "",
  "duration": "",
  "description": ""
}
```

## Projects Collection

```json
{
  "title": "",
  "description": "",
  "technologies": [],
  "githubLink": "",
  "liveLink": ""
}
```

## Skills Collection

```json
{
  "skillName": "",
  "category": ""
}
```

---

# Project Structure

```bash
MyCareerAI/
│
├── public/
│
├── src/
│   ├── assets/
│   ├── components/
│   ├── pages/
│   ├── hooks/
│   ├── services/
│   ├── context/
│   ├── firebase/
│   ├── utils/
│   └── App.jsx
│
├── server/
│
├── .env
├── package.json
├── vite.config.js
└── README.md
```

---

# Installation Guide

## Prerequisites

Install:

* Node.js (v18 or above)
* npm
* Git

Verify installation:

```bash
node -v
npm -v
git --version
```

---

## Clone Repository

```bash
git clone https://github.com/Snigdhaaghosh/MyCareerAI.git

cd MyCareerAI
```

---

## Install Dependencies

```bash
npm install
```

If dependency issues occur:

```bash
npm install --legacy-peer-deps
```

---

# Environment Variables

Create a `.env` file in the root directory.

```env
VITE_FIREBASE_API_KEY=YOUR_FIREBASE_API_KEY

VITE_FIREBASE_AUTH_DOMAIN=YOUR_AUTH_DOMAIN

VITE_FIREBASE_PROJECT_ID=YOUR_PROJECT_ID

VITE_FIREBASE_STORAGE_BUCKET=YOUR_STORAGE_BUCKET

VITE_FIREBASE_MESSAGING_SENDER_ID=YOUR_SENDER_ID

VITE_FIREBASE_APP_ID=YOUR_APP_ID

VITE_GEMINI_API_KEY=YOUR_GEMINI_API_KEY
```

---

# Firebase Setup

### Create Firebase Project

Visit:

https://console.firebase.google.com

### Enable Services

* Authentication
* Firestore Database
* Storage

### Copy Firebase Configuration

Add configuration values to `.env`.

---

# Gemini API Setup

Visit:

https://ai.google.dev

Generate API key and add:

```env
VITE_GEMINI_API_KEY=YOUR_API_KEY
```

---

# Run Development Server

```bash
npm run dev
```

Open:

```text
http://localhost:8080
```

---

# Production Build

```bash
npm run build
```

---

# Preview Production Build

```bash
npm run preview
```

---

#  Deployment

## Deploy using Vercel

Install CLI:

```bash
npm install -g vercel
```

Login:

```bash
vercel login
```

Deploy:

```bash
vercel
```

Production deployment:

```bash
vercel --prod
```

---

#  Future Enhancements

* AI Candidate Matching
* Recruiter Dashboard
* Job Recommendation Engine
* Resume Ranking System
* GitHub Profile Analysis
* LinkedIn Integration
* AI Interview Assistant
* Cover Letter Generator
* Semantic Search
* OCR Support for Scanned Resumes
* Multi-language Resume Analysis
* Career Roadmap Generator
* Learning Recommendation System

---

# Developer

**Snigdha Ghosh**

GitHub: https://github.com/Snigdhaaghosh

---
##  Vision

MyCareerAI aims to become a complete AI-powered career ecosystem where candidates can build, improve, and showcase their professional profiles while recruiters can discover and evaluate top talent efficiently.

**Build Better Careers with AI.**
