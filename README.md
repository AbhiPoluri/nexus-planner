# Nexus Planner

> A modern, intelligent project planning and task management platform designed to help teams organize, prioritize, and execute work efficiently.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

---

## Table of Contents

- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

---

## About

Nexus Planner is a full-stack project management application that combines intuitive task boards with smart scheduling, dependency mapping, and real-time collaboration. Whether you're running a solo side project or coordinating a cross-functional team, Nexus Planner adapts to your workflow.

---

## Features

- 📋 **Kanban & List Views** — Switch between board, list, and timeline layouts
- 🔗 **Dependency Mapping** — Visualize task dependencies with an interactive graph
- 🤖 **Smart Scheduling** — AI-assisted prioritization and deadline suggestions
- 👥 **Real-Time Collaboration** — Live updates, comments, and @mentions
- 📊 **Progress Analytics** — Burndown charts, velocity tracking, and custom reports
- 🔔 **Notifications** — In-app, email, and webhook-based alerts
- 🔒 **Role-Based Access Control** — Granular permissions per project and workspace
- 🌐 **API-First Design** — Full REST & GraphQL API for integrations

---

## Tech Stack

| Layer       | Technology                          |
|-------------|-------------------------------------|
| Frontend    | React 18, TypeScript, Tailwind CSS  |
| State       | Zustand, React Query                |
| Backend     | Node.js, Express, GraphQL           |
| Database    | PostgreSQL, Redis (caching)         |
| Auth        | JWT, OAuth 2.0                      |
| Testing     | Jest, Playwright, React Testing Lib |
| CI/CD       | GitHub Actions                      |
| Deployment  | Docker, AWS / Vercel                |

---

## Getting Started

### Prerequisites

- Node.js v18+
- npm v9+ or yarn
- PostgreSQL 14+
- Redis 7+

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/your-username/nexus-planner.git
cd nexus-planner

# 2. Install dependencies
npm install

# 3. Copy environment variables
cp .env.example .env
# Edit .env with your database credentials and secrets

# 4. Run database migrations
npm run db:migrate

# 5. Seed the database (optional)
npm run db:seed

# 6. Start the development server
npm run dev
```

The app will be available at `http://localhost:3000`.

### Environment Variables

| Variable           | Description                      | Required |
|--------------------|----------------------------------|----------|
| `DATABASE_URL`     | PostgreSQL connection string     | ✅       |
| `REDIS_URL`        | Redis connection string          | ✅       |
| `JWT_SECRET`       | Secret key for JWT signing       | ✅       |
| `PORT`             | Server port (default: 3000)      | ❌       |

---

## Project Structure

```
nexus-planner/
├── src/
│   ├── components/    # Reusable UI components
│   ├── hooks/         # Custom React hooks
│   ├── services/      # API service layer
│   ├── store/         # Global state management
│   └── utils/         # Helper functions & constants
├── docs/              # Architecture docs and API reference
├── tests/
│   ├── unit/          # Unit tests
│   ├── integration/   # Integration tests
│   └── e2e/           # End-to-end tests
├── scripts/           # Build and deployment scripts
└── public/            # Static assets
```

---

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a pull request.

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m 'feat: add your feature'`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

Please follow the [Conventional Commits](https://www.conventionalcommits.org/) specification.

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
