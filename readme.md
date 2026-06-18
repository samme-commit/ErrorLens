# ErrorLens

ErrorLens is an AI-powered developer tool that explains programming error messages in a simple and understandable way.

Instead of searching through confusing Stack Overflow threads or documentation, users can paste an error message, select a programming language, and get a clear explanation of what went wrong, why it happened, and how to fix it.

## Features

* AI-powered error explanation
* Support for multiple programming languages

  * JavaScript
  * HTML
  * CSS
  * Python
* Language-based UI accents
* Markdown rendering
* Syntax-highlighted code blocks
* Copy button for generated code snippets
* Chat-style interface
* Typewriter-style AI responses
* Prompt-injection protection
* Clean and responsive dark UI

## Tech Stack

### Frontend

* HTML
* CSS
* JavaScript
* Font Awesome
* Highlight.js

### Backend

* Node.js
* Express.js
* Groq API
* OpenAI-compatible SDK

## How It Works

1. The user enters an error message.
2. The selected programming language is sent to the backend.
3. The backend sends the error to an AI model through the Groq API.
4. The AI returns a structured explanation.
5. The frontend renders the answer with markdown formatting and syntax-highlighted code blocks.

## Installation

Clone the repository:

```bash
git clone https://github.com/samme-commit/ErrorLens.git
cd ErrorLens
```

Install dependencies:

```bash
npm install
```

Start the server:

```bash
node server.js
```

Open the app in your browser:

```text
http://localhost:3000
```

## Environment Variables

This project requires a Groq API key.

| Variable | Description |
|---|---|
| `GROQ_API_KEY` | API key used to access the Groq API |

### Setting up the API key on Windows PowerShell

You need to make the API key available as an environment variable.

In PowerShell, run:

```powershell
setx GROQ_API_KEY "your_groq_api_key_here"

## Project Structure

```text
ErrorLens/
├── server.js
├── index.html
├── app.css
├── package.json
├── package-lock.json
├── .env
├── .gitignore
└── README.md
```

## Roadmap

Planned improvements:

* Add real-time streaming responses
* Add support for more programming languages
* Add chat history
* Add better mobile responsiveness
* Add deployment version
* Add error examples for users to test

## Security Notes

ErrorLens treats user input as untrusted text. The backend prompt is designed to prevent prompt injection by telling the AI that pasted errors should be analyzed as data, not followed as instructions.

However, no AI safety method is perfect, so additional validation and filtering may be added in the future.

## Why I Built This

I built ErrorLens because error messages can often be confusing, especially when learning programming. The goal is to make debugging less frustrating by translating technical errors into clear explanations and practical fixes.

## Author

Built by [samme-commit](https://github.com/samme-commit)
