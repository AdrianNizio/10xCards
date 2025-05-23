# 10x Cards

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js Version](https://img.shields.io/badge/node-22.14.0-brightgreen.svg)](https://nodejs.org/)
[![Astro Version](https://img.shields.io/badge/astro-5.5.5-orange.svg)](https://astro.build/)

A modern web application built with Astro and React for creating and managing flashcards to enhance learning efficiency.

## Table of Contents
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Available Scripts](#available-scripts)
- [Project Scope](#project-scope)
- [Project Status](#project-status)
- [License](#license)

## Tech Stack

- **Framework:** [Astro](https://astro.build/) v5.5.5
- **UI Library:** [React](https://reactjs.org/) v19.0.0
- **Styling:** 
  - [Tailwind CSS](https://tailwindcss.com/) v4.0.17
  - [Shadcn/ui](https://ui.shadcn.com/) components
- **Language:** [TypeScript](https://www.typescriptlang.org/)
- **Development Tools:**
  - ESLint v9.23.0
  - Prettier
  - Husky for Git hooks
  - Lint-staged for pre-commit linting

## Getting Started

### Prerequisites

- Node.js v22.14.0
- npm (comes with Node.js)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/10x-cards.git
cd 10x-cards
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

The application will be available at `http://localhost:4321`

## Available Scripts

- `npm run dev` - Start the development server
- `npm run build` - Build the production application
- `npm run preview` - Preview the production build locally
- `npm run lint` - Run ESLint to check code quality
- `npm run lint:fix` - Fix ESLint issues automatically
- `npm run format` - Format code using Prettier

## Project Structure

```
./src/
├── layouts/     # Astro layouts
├── pages/       # Astro pages
│   └── api/     # API endpoints
├── middleware/  # Astro middleware
├── db/         # Supabase clients and types
├── types.ts    # Shared types
├── components/ # UI components
│   └── ui/     # Shadcn/ui components
├── lib/        # Services and helpers
└── assets/     # Static internal assets
```

## Project Scope

The project aims to provide a modern flashcard application with the following features:

- Create and manage flashcard decks
- Study sessions with spaced repetition
- Progress tracking and analytics
- Responsive design for all devices
- Offline support
- User authentication and data persistence

## Project Status

🚧 **Under Development** 

The project is currently in active development. Features are being added and refined continuously.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
