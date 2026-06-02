# Contributing to Classgrid

First off, thank you for being part of the Classgrid engineering and design team! We are building the future of educational technology, and your contributions are essential to making our platform scalable, secure, and beautiful.

As our platform is proprietary, these guidelines are designed for internal engineers, contractors, and authorized open-source collaborators.

## 🏗 Understanding Our Architecture

Before contributing, ensure you are familiar with our tech stacks:
1. **The Core Platform:** React 19, Vite, TailwindCSS (Frontend) + Node.js, Express, MongoDB, Supabase (Backend).
2. **The Marketing Engine:** Next.js 15, React 19, TailwindCSS v4, Sanity CMS, Framer Motion.

## 🌿 Branching Strategy

We follow a structured branching flow to keep our environments stable:
- `main`: Production-ready code. Always stable.
- `develop`: The active development branch. Features merge here first.
- `feature/<ticket-or-name>`: Create this branch off `develop` for new features.
- `fix/<bug-name>`: For bug fixes.
- `hotfix/<bug-name>`: For critical production fixes branching directly off `main`.

## 💻 Development Workflow

1. **Sync and Branch:** 
   Pull the latest `develop` branch and create your `feature/` branch.
2. **Run Locally:**
   Always ensure both client and server are running. 
   - Platform: `npm run dev` (Concurrently runs Vite and Express).
   - Marketing: `npm run dev` (Runs Next.js, Turbopack, and ngrok tunnels if needed).
3. **Type Safety & Linting:** 
   Our Next.js marketing repo enforces strict TypeScript rules (`npm run check:types-only`). Ensure no `.js` or `.jsx` files are introduced where TypeScript is expected. Run linting before pushing.
4. **Environment Variables:**
   Never commit `.env` files. If a new environment variable is required, add it to the `.env.example` file and notify the DevOps team.

## 📝 Commit Guidelines

We use conventional commits to auto-generate changelogs. Please format your commit messages as follows:
- `feat: [description]` for new features
- `fix: [description]` for bug fixes
- `docs: [description]` for documentation updates
- `style: [description]` for formatting, missing semi colons, etc.
- `refactor: [description]` for code refactoring
- `test: [description]` for adding tests

*Example:* `feat: integrate Supabase vector search for AI notes`

## 🚀 Pull Request Process

1. Push your branch to GitHub.
2. Open a Pull Request against the `develop` branch (never directly to `main` unless it's a hotfix).
3. Provide a clear description of the problem solved or feature added. Include UI screenshots for frontend changes.
4. Request a review from at least one senior engineer.
5. Ensure all CI/CD pipeline checks pass.

Thank you for helping us build an incredible operating system for modern education!
