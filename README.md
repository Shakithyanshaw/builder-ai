# AI Website Generator – MERN Stack

An AI-powered SaaS web application that allows users to generate complete React websites from natural-language prompts. The application combines a modern React frontend, Node.js/Express backend, MongoDB, authentication, an AI integration through OpenRouter, an in-browser code editor, live preview, iterative AI-powered editing, and website export/publishing.

> **Project Status:** 🚧 In Development  
> **Stack:** MongoDB + Express.js + React.js + Node.js (MERN)  
> **AI Provider:** OpenRouter  
> **License:** Add your preferred license before publishing

---

## 🚀 Project Overview

This project is a full-stack AI website builder inspired by modern AI development platforms.

Instead of manually creating a React website from scratch, a user can enter a prompt such as:

> "Create a modern portfolio website for a software engineer with a dark theme, projects section, skills section, contact form, and responsive design."

The application sends the request to an AI model through OpenRouter. The AI generates the website source code and project files. The user can then:

- Monitor the generation process.
- Preview the generated website.
- Inspect and manually edit source code.
- Ask the AI to modify the project.
- Continue improving the website through additional prompts.
- Export the generated project.
- Publish the website when publishing functionality is configured.

The goal is to demonstrate how AI can be integrated into a real-world MERN SaaS application.

---

## 🎯 Main Goals

The main objectives of this project are:

- Build a complete MERN Stack SaaS application.
- Implement user registration and login.
- Create protected application routes.
- Integrate an AI model through OpenRouter.
- Generate React websites from natural-language prompts.
- Build an AI-assisted development workflow.
- Display generation progress to users.
- Provide a code editor for manual modifications.
- Provide a live website preview.
- Allow iterative AI-powered project updates.
- Export generated website projects.
- Provide a foundation for publishing generated websites.
- Follow maintainable and production-oriented project architecture.

---

## ✨ Key Features

### 👤 User Authentication

- User registration.
- User login.
- Password authentication.
- Session/token-based authentication.
- Protected routes.
- Logout functionality.
- User-specific projects.

### 🤖 AI Website Generation

Users describe the website they want using a natural-language prompt.

Example:

```text
Build a responsive restaurant website with:
- Hero section
- Menu section
- About section
- Customer reviews
- Contact section
- Modern animations
- Mobile responsive layout
```

The AI processes the prompt and generates the required React project.

### 📊 Real-Time Generation Process

The application is designed to show the user what the AI is doing during website generation.

Possible steps include:

```text
Planning website
      ↓
Creating project structure
      ↓
Generating components
      ↓
Generating styling
      ↓
Generating pages
      ↓
Installing/configuring dependencies
      ↓
Building project
      ↓
Generation completed
```

### 💬 AI Project Assistant

After the initial generation, users can continue communicating with the AI.

Examples:

```text
Make the navbar sticky.
```

```text
Change the website color scheme to blue and white.
```

```text
Add a testimonials section.
```

```text
Make the cards have rounded corners.
```

The AI can use the existing project context to modify the generated application.

### 🧑‍💻 Manual Code Editing

Users can inspect and modify generated source code using an integrated code editor.

Typical files may include:

```text
src/
├── components/
├── pages/
├── App.jsx
├── main.jsx
└── index.css
```

### 👁️ Live Preview

Users can preview the generated website without leaving the builder.

The preview should allow users to evaluate:

- Layout.
- Typography.
- Colors.
- Components.
- Responsive behavior.
- Overall design.

### 📦 Export

Generated projects can be packaged for download/export.

The exported project should contain the required source files and configuration needed to continue development locally.

### 🌐 Publishing

The project includes a foundation for publishing generated websites.

A future/production implementation can connect the application to a hosting provider or deployment service.

---

# 🏗️ How the Application Works

The high-level workflow is:

```text
                    ┌─────────────────────┐
                    │       User          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   React Frontend    │
                    └──────────┬──────────┘
                               │ REST API
                               ▼
                    ┌─────────────────────┐
                    │ Express / Node.js   │
                    │      Backend        │
                    └──────┬───────┬──────┘
                           │       │
                 ┌─────────┘       └─────────┐
                 ▼                           ▼
        ┌────────────────┐          ┌────────────────┐
        │    MongoDB     │          │   OpenRouter   │
        │   Database     │          │   AI Service   │
        └────────────────┘          └───────┬────────┘
                                            │
                                            ▼
                                   Generated React Code
                                            │
                                            ▼
                                   ┌────────────────┐
                                   │ Preview / Edit │
                                   └────────────────┘
```

---

# 👤 User Flow

## 1. Create an Account

The user opens the application and creates an account.

```text
Registration
     ↓
Account created
     ↓
Login
     ↓
Dashboard
```

## 2. Create a Project

The user enters a website description.

```text
Dashboard
   ↓
Create Project
   ↓
Enter AI Prompt
   ↓
Generate
```

## 3. AI Generates the Website

The backend sends the prompt to OpenRouter.

```text
User Prompt
    ↓
Backend API
    ↓
OpenRouter
    ↓
AI Model
    ↓
Generated Project
```

## 4. Review the Website

The user sees:

- Generation status.
- Generated files.
- Code editor.
- Website preview.

## 5. Improve the Website

The user can send additional instructions.

```text
Existing Project
       +
New User Prompt
       ↓
AI Agent
       ↓
Updated Project
```

## 6. Export or Publish

Once satisfied:

```text
Project
  ├── Export
  └── Publish
```

---

# 🛠️ Technology Stack

## Frontend

| Technology         | Purpose                 |
| ------------------ | ----------------------- |
| React.js           | Frontend framework      |
| React Router       | Application routing     |
| JavaScript / JSX   | Application development |
| CSS / Tailwind CSS | Styling                 |
| Axios / Fetch      | API communication       |
| Code Editor        | Manual source editing   |

## Backend

| Technology           | Purpose             |
| -------------------- | ------------------- |
| Node.js              | JavaScript runtime  |
| Express.js           | REST API framework  |
| MongoDB              | Database            |
| Mongoose             | MongoDB ODM         |
| JWT / Authentication | User authentication |
| OpenRouter           | AI API integration  |

## Development Tools

| Tool       | Purpose                 |
| ---------- | ----------------------- |
| Git        | Version control         |
| GitHub     | Repository hosting      |
| CodeRabbit | AI-assisted code review |
| VS Code    | Development environment |
| npm        | Package management      |

---

# 🧩 System Architecture

The application follows a client-server architecture.

```text
Frontend
React Application
       │
       │ HTTP Requests
       ▼
Backend
Express REST API
       │
       ├──────────────► MongoDB
       │
       └──────────────► OpenRouter
                              │
                              ▼
                          AI Model
```

## Frontend Responsibilities

The frontend handles:

- UI rendering.
- User interaction.
- Routing.
- Authentication state.
- Project management UI.
- Prompt submission.
- Generation progress.
- Code editing.
- Preview.
- Export controls.

## Backend Responsibilities

The backend handles:

- Authentication.
- Authorization.
- User management.
- Project management.
- AI requests.
- AI response processing.
- Database operations.
- Validation.
- Error handling.
- Security.

## Database Responsibilities

MongoDB stores:

- Users.
- Projects.
- Generated files.
- Project metadata.
- AI conversation history, if implemented.
- Generation status.

---

# 📁 Project Structure

A recommended repository structure is:

```text
ai-website-generator/
│
├── client/
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── layouts/
│   │   ├── context/
│   │   ├── hooks/
│   │   ├── services/
│   │   ├── utils/
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   │
│   ├── package.json
│   └── vite.config.js
│
├── server/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── services/
│   ├── utils/
│   ├── app.js
│   ├── server.js
│   └── package.json
│
├── .gitignore
├── README.md
└── package.json
```

# ⚙️ Installation and Setup

## Prerequisites

Install the following:

- Node.js.
- npm.
- MongoDB or MongoDB Atlas.
- Git.
- A code editor such as VS Code.
- OpenRouter API access.

Verify Node.js:

```bash
node -v
```

Verify npm:

```bash
npm -v
```

Verify Git:

```bash
git --version
```

---

# 📥 Clone the Repository

```bash
git clone <YOUR_REPOSITORY_URL>
```

Enter the project:

```bash
cd ai-website-generator
```

---

# 📦 Install Dependencies

## Frontend

```bash
cd client
npm install
```

## Backend

Open another terminal:

```bash
cd server
npm install
```

---

# 🔧 Configure Environment Variables

Create:

```text
server/.env
```

Add:

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_secret
OPENROUTER_API_KEY=your_openrouter_api_key
CLIENT_URL=http://localhost:5173
```

Create:

```text
client/.env
```

Add:

```env
VITE_API_URL=http://localhost:5000/api
```

---

# ▶️ Running the Project

## Start Backend

```bash
cd server
npm run dev
```

Expected result:

```text
Server running on port 5000
Database connected
```

## Start Frontend

Open another terminal:

```bash
cd client
npm run dev
```

Vite will normally provide a local URL similar to:

```text
http://localhost:5173
```

Open that URL in your browser.

---

# 📈 Future Improvements

Potential improvements include:

## AI Features

- Multiple AI model selection.
- Streaming AI responses.
- Better project context management.
- Automatic bug fixing.
- AI code explanation.
- AI code refactoring.
- AI-generated tests.
- Image generation.
- AI-generated content.
- Design-to-code from screenshots.

## Editor Features

- File explorer.
- Multi-file editing.
- Syntax highlighting.
- Search across files.
- Undo/redo.
- Git integration.
- Terminal.
- Dependency management.

## SaaS Features

- User profiles.
- Project history.
- Project duplication.
- Team collaboration.
- Shared projects.
- Usage limits.
- Subscription plans.
- Billing.
- Usage analytics.

## Deployment

- One-click deployment.
- Custom domains.
- Deployment history.
- Rollbacks.
- Build logs.
- Automatic HTTPS.

## Security

- Sandboxed preview environments.
- Containerized builds.
- Network isolation.
- Resource quotas.
- Malware/security scanning.
- Prompt abuse protection.

---
