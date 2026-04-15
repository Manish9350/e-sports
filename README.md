# e-sports

A full-stack tournament registration and management app for esports events built with React, Vite, Express, and Drizzle ORM.

## Overview

This repository includes a client and server for a tournament experience with:
- registration form and player tracking
- tournament details, scoring rules, and game rules pages
- certificate generation and email sending
- contact, privacy, refund, terms, and acceptable use pages
- a players dashboard with registration validation

## Tech stack

- Frontend: React 18, TypeScript, Vite, Tailwind CSS, Radix UI, React Query, Framer Motion, Wouter
- Backend: Node.js, Express, TypeScript
- Database / ORM: Drizzle ORM, drizzle-kit
- Email / certificate utilities: Nodemailer, jsPDF, html-to-image

## Project structure

- `client/` – React application source files
- `server/` – Express API, certificate/email services, server config
- `shared/` – common schema definitions
- `data/` – seeded player data
- `drizzle.config.ts` – database configuration

## Setup

1. Install dependencies:

```bash
npm install
```

2. Add environment variables in a `.env` file at the repository root.

### Recommended environment variables

```env
DATABASE_URL=postgres://user:pass@host:port/dbname
SMTP_HOST=smtp.example.com
SMTP_PORT=587
SMTP_USER=your-smtp-user
SMTP_PASS=your-smtp-password
SMTP_FROM="Sarth Esports <admin@sarthesports.games>"
SESSION_SECRET=super-secret-value
NODE_ENV=development
```

3. Run the app in development mode:

```bash
npm run dev
```

The server listens on port `5000` by default and the Vite client runs together in development.

## Build and production

Build the client and bundle the server:

```bash
npm run build
```

Start the production build:

```bash
npm run start
```

## Database

The project uses `drizzle-kit` with `DATABASE_URL`. To push schema changes:

```bash
npm run db:push
```

## Scripts

- `npm run dev` — start the development server
- `npm run build` — build the Vite app and bundle the server
- `npm run start` — run the built server
- `npm run check` — run TypeScript checks
- `npm run db:push` — apply Drizzle schema migrations

## Notes

- Certificate emails require SMTP configuration.
- The project includes multiple informational pages, a registration flow, and a certificate generation workflow.

## License

MIT
