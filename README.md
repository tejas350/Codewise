<div align="center">⚡ CodeWise – AI-Powered Automated Code Review Tool</div>
<div align="center">

A GitHub-integrated automated code review system that uses OpenAI to generate intelligent, context-aware suggestions on Pull Requests and Issues.

</div>
✨ Overview

CodeWise is an automated code-review and issue-triage tool designed to enhance software development workflows.
It integrates with GitHub to analyze Pull Requests, triage Issues, and provide AI-driven feedback using the OpenAI API.

CodeWise acts as a lightweight GitHub bot that improves code quality, reduces review workload, and helps teams ship cleaner code.

🚀 Key Features
✅ AI-Powered Code Review

Uses OpenAI to generate smart suggestions, refactor hints, and quality insights on Pull Requests.

✅ Automated Issue Triage

Classifies, summarizes, or prioritizes incoming GitHub Issues.

✅ Pull Request & Review Handlers

Specialized logic for PR creation, updates, and reviews.

✅ Modular Architecture

Handlers, services, and utilities are organized under src/ for easy maintenance.

✅ Node.js + GitHub API Integration

Uses libraries like:

superagent — HTTP requests

uuid — unique identifiers

validator — input validation

yargs, yargs-parser — CLI argument parsing

📦 Project Structure
.
├── dist/                          # Compiled/bundled files
├── lib/                           # Library/build output (from dependencies like superagent)
├── node_modules/                  # Project dependencies
├── src/
│   ├── handlers/                  # GitHub webhook event handlers
│   │   ├── issues.js              # Logic for Issue events
│   │   ├── pullRequest.js         # Logic for Pull Request events
│   │   └── pullRequestReview.js   # Logic for Pull Request Review events
│   ├── services/
│   │   └── openaiService.js       # Integration with OpenAI API
│   └── index.js                   # Main entry point
├── test/
│   └── fixtures/                  # Sample payloads for testing
├── HISTORY.md                     # Project changelog
├── LICENSE                        # License information
├── README.md                      # Project documentation
└── package.json                   # Dependencies & scripts

🛠️ Prerequisites

Before running CodeWise, ensure you have:

Node.js (LTS recommended)

GitHub App or Personal Access Token (PAT)

OpenAI API Key

Internet access for API communication

📥 Installation
1️⃣ Clone the Repository
git clone <repository-url>
cd CodeWise

2️⃣ Install Dependencies
npm install

▶️ Running the Application
1. Set Required Environment Variables

You will need:

OPENAI_API_KEY=
GITHUB_TOKEN=


(And any other config used in your handlers/services.)

2. Start the Service
node src/index.js


If using PM2:

pm2 start src/index.js

🧪 Testing

The project includes mock fixtures for event simulation.

Run tests (if configured in package.json):

npm test

🛠️ Development Guide
Modify AI Analysis

Edit the prompts/models in:

src/services/openaiService.js

Add/Modify GitHub Handlers

Extend logic inside:

src/handlers/

Add More Webhook Events

You can add custom handlers for:

push events

comments

labels

merge events

📌 Future Enhancements

Multi-language code review support

GitHub App UI dashboard

AI-generated auto-fix PRs

Fine-tuned models for better PR feedback

📄 License

This project is licensed under the MIT License.
