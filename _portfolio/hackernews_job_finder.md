---
title: "HackerNews Job Finder"
excerpt: "Python, React, LLMs, Docker, WebSockets"
header:
  teaser: /assets/images/hn-logo.png
date: "2024-03-20"
---

<img src="{{ BASE_URL }}/assets/images/hn-logo.png" alt="" class="full">

## Introduction
Lately, I found myself skimming through tons of posts on "hacker news who is hiring" threads in search of a remote job. This process is not very pleasant as each thread is basically just a wall of text and searching for a job that meets specific criteria is not easy. To solve this problem, I built a tool that leverages Large Language Models (LLMs) to make the job search process more efficient and user-friendly. The source code can be found in this [repository](https://github.com/m-a-r-i-b/hackernews-job-finder).

## Solution Overview

![image-center]({{ site.url }}{{ site.baseurl }}/assets/images/hn-arch.png){: .align-center}

## Key Features

### LLM-Powered Agents
The system employs multiple specialized agents to analyze job posts:

- **ResumeParser**: Extracts work experience and skills from uploaded resumes
- **IsRemote**: Determines if positions allow remote work
- **RoleExtractor**: Identifies job roles being offered
- **KeywordExtractor**: Pulls out technical requirements (Python, JavaScript, React, etc.)
- **ContactInfoExtractor**: Finds application links and contact emails
- **CoverLetterGenerator**: Creates tailored cover letters based on resume-job matches

### Technical Architecture
- Frontend built with React for interactive job searching
- Python backend with async workers for job processing
- WebSocket integration for real-time updates
- Docker containerization for easy deployment
- JSON-based persistence layer for storing processed jobs

## Getting Started

### Prerequisites
- Docker installed on your machine
- OpenAI API key

### Installation Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/m-a-r-i-b/hackernews-job-finder.git
   cd hackernews-job-finder
   ```

2. Set up OpenAI API key:
   ```bash
   cd backend
   # Create .env file with your API key
   echo "OPENAI_API_KEY=your_openai_api_key" > .env
   ```

3. Build and run with Docker:
   ```bash
   cd ..
   docker-compose up --build
   ```

4. Access the application:
   ```
   http://localhost:3000
   ```

## How It Works
1. The system scrapes all posts from a given HN "who is hiring" thread
2. Posts are distributed to a pool of background workers
3. Each worker processes posts through the LLM agent pipeline
4. Results are pushed to the frontend in real-time via WebSockets
5. All extracted information is persisted to maintain search history

{: .notice--info}
The application is containerized for easy deployment and requires minimal setup. Just provide your OpenAI API key and you're ready to go!