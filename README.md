<h1 align="center">HealthTrack</h1>

<p align="center"><em><strong>Daily health, ready for care.</strong></em></p>

<div align="center">
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/shadcn%2Fui-000000?style=for-the-badge&logo=shadcnui&logoColor=white" alt="shadcn/ui" />
  <img src="https://img.shields.io/badge/GSAP-88CE02?style=for-the-badge&logo=gsap&logoColor=white" alt="GSAP" />
  <img src="https://img.shields.io/badge/React_Query-FF4154?style=for-the-badge&logo=reactquery&logoColor=white" alt="React Query" />
  <img src="https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white" alt="Axios" />
  <img src="https://img.shields.io/badge/React_Hook_Form-EC5990?style=for-the-badge&logo=reacthookform&logoColor=white" alt="React Hook Form" />
  <img src="https://img.shields.io/badge/Zod-3E67B1?style=for-the-badge&logo=zod&logoColor=white" alt="Zod" />
  <img src="https://img.shields.io/badge/i18next-26A69A?style=for-the-badge&logo=i18next&logoColor=white" alt="i18next" />
  <img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express" />
  <img src="https://img.shields.io/badge/Sequelize-52B0E7?style=for-the-badge&logo=sequelize&logoColor=white" alt="Sequelize" />
  <img src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black" alt="Swagger" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=redis&logoColor=white" alt="Redis" />
  <img src="https://img.shields.io/badge/Turborepo-EF4444?style=for-the-badge&logo=turborepo&logoColor=white" alt="Turborepo" />
</div>

<p align="center">
HealthTrack is a full-stack, bilingual (English / Arabic) health-tracking platform. Patients record their day — mood, sleep, symptoms, medications, and doctor visits — in one calm place, spot trends over time, and turn any date range into a physician-ready AI summary they can bring to an appointment. An admin side keeps the medical catalogs (symptoms, conditions, medications, clinics, doctors) clean and up to date.
</p>

<p align="center">
Built as a TypeScript monorepo with a React frontend, an Express + Sequelize REST API, and BullMQ background workers.
</p>

---

## Table of Contents

- [Features](#features)
- [Screenshots](#screenshots)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Available Scripts](#available-scripts)
- [Testing](#testing)
- [API Documentation](#api-documentation)
- [Environment Variables](#environment-variables)
- [Background Jobs](#background-jobs)
- [Docker](#docker)

---

## Features

### For patients

- 🔐 **Authentication** — JWT access/refresh tokens, session cookies, role-based routing (`user` / `admin`) and an onboarding flow
- 📝 **Guided daily check-in** — a 5-step wizard capturing mood, sleep, journal notes, symptoms, medications, conditions, and doctor visits
- 📒 **Daily log history** — browse past check-ins with date-range filtering
- 🏥 **Clinical profile** — track your conditions, symptoms, medications, clinics, and doctors in one place
- 📊 **Health analytics** — mood, sleep, and entry trends over the last 30 days
- 🤖 **AI clinical summaries** — generate physician-ready reports for any date range, with bilingual EN/AR output
- ⏰ **Daily reminders** — scheduled check-in reminder emails, localized to the user's language
- 🌍 **Full Arabic (RTL) support** alongside English via i18next

### For admins

- 🗂️ **Catalog management** — CRUD for conditions, symptoms (SNOMED/BioPortal-referenced), medications, clinics, and doctors
- 📈 **Admin dashboard** — overview plus filtering on every catalog list

---

## Screenshots

<table border="1" cellpadding="10" cellspacing="0" style="border-collapse: collapse; border: 1px solid #888888;">
  <tr>
    <td align="center" width="50%" style="border: 1px solid #888888;">
      <img src="screen_shots/Screenshot%202026-09-08%20083058.png" alt="Landing Page" width="100%" />
      <p align="center"><strong>Landing Page</strong></p>
    </td>
    <td align="center" width="50%" style="border: 1px solid #888888;">
      <img src="screen_shots/Screenshot%202026-09-08%20083342.png" alt="Patient Dashboard" width="100%" />
      <p align="center"><strong>Patient Dashboard</strong></p>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%" style="border: 1px solid #888888;">
      <img src="screen_shots/Screenshot%202026-09-08%20083411.png" alt="Daily Log History" width="100%" />
      <p align="center"><strong>Daily Log &mdash; Check-in History</strong></p>
    </td>
    <td align="center" width="50%" style="border: 1px solid #888888;">
      <img src="screen_shots/Screenshot%202026-09-08%20083449.png" alt="Daily Check-in Wizard" width="100%" />
      <p align="center"><strong>Daily Check-in Wizard</strong> <em>(Step 1 of 5 &mdash; How you feel)</em></p>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%" style="border: 1px solid #888888;">
      <img src="screen_shots/Screenshot%202026-09-08%20083512.png" alt="Health Profile Conditions" width="100%" />
      <p align="center"><strong>Health Profile &mdash; Conditions</strong></p>
    </td>
    <td align="center" width="50%" style="border: 1px solid #888888;">
      <img src="screen_shots/Screenshot%202026-09-08%20083600.png" alt="Health Profile Symptoms" width="100%" />
      <p align="center"><strong>Health Profile &mdash; Symptoms</strong></p>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%" style="border: 1px solid #888888;">
      <img src="screen_shots/Screenshot%202026-09-08%20083800.png" alt="Medications" width="100%" />
      <p align="center"><strong>Medications</strong></p>
    </td>
    <td align="center" width="50%" style="border: 1px solid #888888;">
      <img src="screen_shots/Screenshot%202026-09-08%20083820.png" alt="Providers Clinics" width="100%" />
      <p align="center"><strong>Providers &mdash; Clinics</strong></p>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%" style="border: 1px solid #888888;">
      <img src="screen_shots/Screenshot%202026-09-08%20083840.png" alt="Providers Doctors" width="100%" />
      <p align="center"><strong>Providers &mdash; Doctors</strong></p>
    </td>
    <td align="center" width="50%" style="border: 1px solid #888888;">
      <img src="screen_shots/Screenshot%202026-09-08%20083902.png" alt="Doctor Visits" width="100%" />
      <p align="center"><strong>Doctor Visits Timeline</strong></p>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%" style="border: 1px solid #888888;">
      <img src="screen_shots/Screenshot%202026-09-08%20083925.png" alt="Health Analytics" width="100%" />
      <p align="center"><strong>Health Analytics</strong> <em>(Mood &amp; sleep trends)</em></p>
    </td>
    <td align="center" width="50%" style="border: 1px solid #888888;">
      <img src="screen_shots/Screenshot%202026-09-08%20083945.png" alt="AI Reports" width="100%" />
      <p align="center"><strong>AI Reports &mdash; Clinical Summaries</strong></p>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%" style="border: 1px solid #888888;">
      <img src="screen_shots/Screenshot%202026-09-08%20084015.png" alt="Settings Account" width="100%" />
      <p align="center"><strong>Settings &mdash; Account &amp; Security</strong></p>
    </td>
    <td align="center" width="50%" style="border: 1px solid #888888;">
      <img src="screen_shots/Screenshot%202026-09-08%20084047.png" alt="Dashboard Arabic RTL" width="100%" />
      <p align="center"><strong>Dashboard &mdash; Arabic (RTL)</strong></p>
    </td>
  </tr>
</table>

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 18, Vite, TypeScript, Tailwind CSS, shadcn/ui, GSAP |
| Data fetching | TanStack Query, Axios |
| Forms / Validation | React Hook Form, Zod |
| Charts | Recharts |
| i18n | i18next / react-i18next (English + Arabic RTL) |
| Backend | Express, Sequelize, Zod, OpenAPI (Swagger) |
| Auth | JWT (access + refresh), bcrypt, role-based access control |
| AI | OpenAI (clinical summaries), embeddings, Google Cloud Translation (optional) |
| Background Jobs | BullMQ, Redis |
| Database | PostgreSQL |
| Monorepo | Turborepo + npm workspaces |
| Language | TypeScript (everywhere) |

---

## Project Structure

Turborepo monorepo with npm workspaces. All packages share a TypeScript codebase.

```
packages/
  web/       → React + Vite frontend (port 5173) — pages, layouts, providers, UI kit
  api/       → Express REST API (port 3000) — controllers, services, Sequelize models,
               migrations, seeders, OpenAPI spec
  workers/   → BullMQ background job processors (reminders, email, embeddings)
  shared/    → Shared code: auth (JWT/password), Sequelize models, queue client,
               AI client, config
```

---

## Getting Started

### Prerequisites

- **Node.js >= 20**
- **Docker** (for PostgreSQL + Redis)

### 1. Install dependencies

```bash
npm install
```

### 2. Start infrastructure

```bash
docker-compose up -d
```

### 3. Configure environment

```bash
cp .env.example .env
# Edit .env with your values
```

> ⚠️ The provided `.env.example` and `docker-compose.yml` default to a database named `starter_kit` — that's just the template leftover. Change `POSTGRES_DB` and `DATABASE_URL` to whatever you prefer.

### 4. Run database migrations & seed

```bash
cd packages/api
npm run db:migrate
npm run db:seed   # optional: catalogs (conditions, symptoms, meds, clinics, doctors) + admin user
```

The seeder creates an admin account:

```
email:    admin@example.com
password: Admin1234!
```

### 5. Start development servers

```bash
# Start all packages in parallel (from repo root)
npm run dev

# Or start individually
cd packages/api && npm run dev      # API on :3000
cd packages/web && npm run dev      # Web on :5173
cd packages/workers && npm run dev  # Workers
```

---

## Available Scripts

Run these from the repo root (Turbo delegates to each package):

| Command | Description |
|---------|-------------|
| `npm run dev` | Start all packages in watch mode |
| `npm run build` | Build all packages |
| `npm run test` | Run all test suites |
| `npm run lint` | Lint all packages |
| `npm run clean` | Clean build output across all packages |

---

## Testing

```bash
npm run test                  # All packages (Turbo)
cd packages/api && npm test   # API unit + integration tests (Jest + Supertest)
cd packages/web && npm test   # Web component/hook tests (Vitest + Testing Library)
```

---

## API Documentation

The API is described by an OpenAPI 3 spec (`packages/api/openapi.yaml`). At runtime:

- **Swagger UI:** `http://localhost:3000/api/docs`
- **Raw spec:** `http://localhost:3000/api/openapi.yaml`
- **Health check:** `http://localhost:3000/health`

Typed API clients for the frontend can be regenerated with:

```bash
cd packages/web
npm run gen:api-types
```

---

## Environment Variables

See `.env.example` for all required variables. Notable ones:

| Variable | Purpose |
|----------|---------|
| `DATABASE_URL`, `POSTGRES_*` | PostgreSQL connection |
| `REDIS_URL` | Redis connection (BullMQ) |
| `JWT_SECRET`, `JWT_REFRESH_SECRET` | Access / refresh token signing |
| `OPENAI_API_KEY` | AI clinical summaries (optional) |
| `GOOGLE_TRANSLATE_API_KEY` | Arabic catalog labels (optional) |
| `S3_*` | Object storage for attachments (optional) |
| `SMTP_*`, `EMAIL_FROM_NAME` | Daily reminder emails (optional) |

---

## Background Jobs

Workers consume BullMQ queues from Redis (scheduled every minute):

| Worker | Queue | What it does |
|--------|-------|--------------|
| `reminder` | `reminders` | Checks for daily check-in reminders due per user settings |
| `email` | `emails` | Sends reminder emails via SMTP (localized EN/AR) |
| `embeddings` | `embeddings` | Builds/updates embeddings via the AI client |

---

## Docker

The `docker-compose.yml` starts:

- **PostgreSQL 16** on port `5432`
- **Redis 7** on port `6379`
