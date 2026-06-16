# WrenchTime OS — Private Full-Stack Business Operations Platform

WrenchTime OS is a private full-stack operations platform built to run a small service business from quote intake through scheduling, payments, customer communication, expense review, marketing attribution, and AI-assisted operational analysis. This repository is a public case study only: it describes the system architecture, engineering decisions, and product scope without exposing private source code, customer data, secrets, or proprietary workflows.

## Problem Solved

Small service businesses often run core operations across disconnected tools: spreadsheets, payment dashboards, calendars, email threads, bank exports, ad dashboards, and manual notes. WrenchTime OS brings those workflows into one admin-focused system so the operator can track work, collect deposits and balances, monitor expenses, understand attribution, and review AI-generated advisory notes without giving automation direct control over customers or ad accounts.

## Tech Stack

Frontend/App:
- Next.js App Router
- React
- TypeScript
- Tailwind CSS
- Shadcn-style component system
- PWA/mobile-friendly admin UI

Backend/Data:
- Next.js server actions and route handlers
- Prisma 6.x
- PostgreSQL
- Supabase Postgres
- Previously local SQLite during development, now Postgres/Supabase-oriented

Deployment:
- Vercel
- Supabase
- Environment-variable based configuration

Authentication:
- Auth.js
- Google login
- Admin email allowlist

Payments:
- Stripe Checkout
- Stripe webhooks
- Deposits and final balances

Email/SMS:
- Resend for email
- Quo/OpenPhone for SMS
- Twilio legacy/disabled

Scheduling:
- Google Calendar integration
- Business timezone: America/Detroit

Uploads:
- UploadThing

Accounting/Banking:
- Mercury read-only integration
- BankTransaction plus ExpenseAnnotation model pattern
- Manual expenses
- CPA/year-end exports

Ads/Growth Intelligence:
- Meta Pixel
- Google Ads conversion tracking / gtag
- Read-only Google Ads API connector scaffold
- Read-only Meta Marketing API connector scaffold
- Growth Intelligence dashboards
- Campaign/source attribution
- Estimated gross profit
- Tracking health
- Advisory AI recommendations

AI:
- OpenAI API
- Settings-based AI tools
- Structured-output advisory workflows
- No autonomous customer actions
- No ad-account writes

Code Quality:
- Strict TypeScript
- Prisma migrations
- ESLint/linting
- `npx tsc --noEmit`
- `npm run build`
- `npm run test:growth`

## Key Features

- Admin dashboard for quotes, scheduled jobs, deposits, expenses, tracking health, and advisory notes.
- Quote and schedule workflows designed for a service-business operating cadence.
- Stripe-backed deposit and final-balance payment handling.
- Calendar integration for service scheduling in the business timezone.
- Email and SMS notification support through external providers.
- Upload handling for job-related files and internal records.
- Banking and expense review with read-only bank data, manual adjustments, annotations, and CPA-ready export concepts.
- Growth Intelligence views for attribution, conversion tracking health, campaign/source performance, estimated gross profit, and advisory recommendations.
- AI-assisted analysis using structured outputs and settings-based controls.

## Architecture Summary

The platform is organized around a Next.js admin application deployed on Vercel, a PostgreSQL database hosted through Supabase, and several tightly scoped external integrations. The admin UI communicates with server-side application logic through server actions and route handlers. Data persistence is managed through Prisma migrations against PostgreSQL. External APIs are integrated behind server-side boundaries for authentication, payments, messaging, scheduling, uploads, banking, ad attribution, and AI advisory features.

See the high-level architecture diagram in [`assets/architecture.mmd`](assets/architecture.mmd) and the data-flow diagram in [`assets/data-flow.mmd`](assets/data-flow.mmd).

## Privacy Note

This repository intentionally does not include the private application source code, private database schema, customer data, transaction data, API credentials, operational secrets, internal route names, or proprietary implementation details. It is designed as a safe public case study for technical review and recruiting conversations.

## What I Personally Built

I designed and implemented the private WrenchTime OS product as a full-stack business operations system. My work covered the admin UI, typed application workflows, database modeling and migrations, payment flow integration, calendar and messaging integrations, upload handling, banking/expense concepts, marketing attribution dashboards, AI advisory workflows, deployment configuration, and production-oriented quality checks.

I also designed the system boundaries around safety: read-only financial and ad-account integrations, allowlisted admin access, environment-variable configuration, structured AI outputs, and no autonomous customer-facing or ad-account write actions.

## Why This Project Matters

This project demonstrates practical full-stack engineering in a real operating environment. It combines product thinking, backend data modeling, third-party API integration, privacy-aware architecture, payment handling, growth analytics, AI safety constraints, and production deployment discipline. The result is not a demo app; it is a working internal platform built to reduce manual overhead and improve decision-making for a real service business.

## Public Safety Checklist

- No source code included
- No secrets included
- No customer data included
- No proprietary workflows included
- No real financial data included
- Case study only
