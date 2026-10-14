# ProjectSync — AI-Powered Project & Task Management

ProjectSync is a full-stack web application designed to simplify project organization and task management. It combines project and task tracking with an AI-powered Copilot that helps users interact with their workspace through natural-language commands.

## Features

- **Project Management:** Organize and manage projects in one place.
- **Task Management:** Create, view, track, and manage tasks.
- **AI Copilot:** Interact with project and task management functionality using natural-language prompts.
- **Authentication:** User registration, login, and protected application routes.
- **Dashboard:** Access project and task information through a centralized interface.
- **Database Integration:** Store and retrieve application data using Supabase and PostgreSQL.
- **Responsive Interface:** React-based interface with theme support.

## Tech Stack

| Category | Technologies |
|---|---|
| Frontend | React, TypeScript, Vite |
| Backend | Node.js, Express.js |
| Database | Supabase, PostgreSQL |
| AI Integration | Groq API |
| API Communication | REST APIs |
| Testing | Project validation tests |
| Version Control | Git, GitHub |

## How the AI Copilot Works

The AI Copilot connects natural-language requests to backend functionality.

1. The user enters a request through the Copilot interface.
2. The backend processes the request using the configured AI integration.
3. The AI can select available tools for supported project and task operations.
4. The backend executes the selected operation and retrieves the relevant data.
5. The application returns a response to the user.

The Copilot's available actions depend on the tools implemented and configured in the application.

## Architecture

```text
User
  |
  v
React + TypeScript Frontend
  |
  v
Node.js + Express Backend
  |
  +------> Groq AI Copilot
  |              |
  |              v
  |        Tool Selection
  |              |
  v              v
Supabase / PostgreSQL
  |
  v
Application Data
```

## Getting Started

### Prerequisites

Install the following before running the project:

- Node.js
- npm
- A Supabase account and project
- A Groq API key for AI functionality

### 1. Clone the repository

```bash
git clone https://github.com/Harshada0408/ProjectSync.git
cd ProjectSync
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env` file in the project root using `.env.example` as a reference.

Configure the variables required by the application:

```dotenv
SUPABASE_URL=your_supabase_project_url
SUPABASE_PUBLISHABLE_KEY=your_supabase_publishable_key
SUPABASE_SECRET_KEY=your_supabase_secret_key
GROQ_API_KEY=your_groq_api_key
PORT=3000
```

Use the exact variable names expected by the application. Never commit your actual `.env` file or expose secret keys in source code.

### 4. Set up the database

1. Create a Supabase project.
2. Open the SQL Editor in your Supabase dashboard.
3. Review and execute `supabase-schema.sql`.
4. Apply `supabase-fix.sql` only if required by your database setup.

### 5. Start the development server

```bash
npm run dev
```

Open the local URL displayed in your terminal. In the current development setup, the application runs at:

http://localhost:3000

## Environment and Security

- Store credentials in environment variables.
- Keep `.env` excluded from version control.
- Use appropriate database access policies and authentication checks.
- Never expose privileged Supabase keys in client-side code.
- Keep third-party API keys private.

## Future Improvements

- Improve AI-generated responses and error handling.
- Add advanced task filtering, search, and sorting.
- Introduce project analytics and productivity reports.
- Add task activity history and collaboration features.
- Expand automated testing and deployment workflows.

## License

This repository includes the license and notices applicable to the original project. See the `LICENSE` file for details.

