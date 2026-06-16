# Architecture

WrenchTime OS is a private full-stack operations platform built around a server-rendered Next.js application, a PostgreSQL data layer, and a controlled set of external integrations. The public diagram intentionally stays at a module level and does not expose private routes, exact table definitions, internal filenames, or proprietary workflow steps.

## System Shape

The admin experience is delivered through a mobile-friendly Next.js App Router interface. Authenticated admin users access quote, scheduling, payment, expense, growth, and advisory views from a unified UI. Server-side application logic handles sensitive operations such as payment events, provider calls, AI requests, and database writes.

The database layer uses Prisma 6.x with PostgreSQL. The private system moved from local SQLite during development toward a production-oriented Supabase Postgres setup. The public case study describes data areas only at a high level.

## High-Level Modules

- Admin UI: mobile-friendly operator interface for daily business management.
- Auth: Google login through Auth.js with an admin email allowlist.
- Quote/Schedule Workflows: quote tracking, job scheduling, and calendar coordination.
- Payments: Stripe Checkout and webhook-backed payment state updates for deposits and final balances.
- Expense/Banking: read-only banking import concepts, manual expenses, annotations, and CPA/year-end export support.
- Growth Intelligence: attribution, tracking health, estimated gross profit, and campaign/source analysis.
- AI Advisory: settings-based structured recommendations using the OpenAI API.
- External APIs: Stripe, Google Calendar, Resend, Quo/OpenPhone, UploadThing, Mercury, Google Ads, Meta Marketing, and OpenAI.
- PostgreSQL: central relational persistence layer.

## Deployment Model

The private application is deployed with Vercel for the web runtime and Supabase for PostgreSQL. Runtime configuration is handled through environment variables. Secrets are not committed to source control and are not included in this public export.

## Boundary Decisions

Sensitive integrations are kept server-side. The admin UI does not directly hold provider secrets or write directly to external systems from the browser. AI features are constrained to advisory outputs and internal review, and growth connectors are designed as read-only scaffolds rather than tools that mutate ad accounts.

## Diagram

See [`../assets/architecture.mmd`](../assets/architecture.mmd).
