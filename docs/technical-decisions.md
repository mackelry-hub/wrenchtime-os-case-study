# Technical Decisions

## Next.js App Router

The private application uses the Next.js App Router to keep the product organized around modern server/client boundaries. Server actions and route handlers support privileged operations while the React UI focuses on the admin experience.

## TypeScript and Strictness

Strict TypeScript helps keep integration-heavy workflows safer as the system touches payments, scheduling, expenses, attribution, and AI-generated outputs. Type checks are part of the quality workflow through `npx tsc --noEmit`.

## Prisma and PostgreSQL

Prisma 6.x provides typed database access and migration management. The project started with local SQLite during development and moved toward PostgreSQL on Supabase for a production-oriented relational data layer.

## Environment-Based Configuration

Provider credentials, environment-specific settings, webhook secrets, and deployment configuration are handled through environment variables. This keeps secrets outside the public case study and outside source-controlled documentation.

## Auth.js With Admin Allowlist

Authentication uses Google login through Auth.js, paired with an admin email allowlist. This is appropriate for a private internal tool with a small set of trusted users.

## Provider Integrations

Third-party systems are integrated behind server-side boundaries where possible. Stripe handles Checkout and webhooks. Google Calendar supports scheduling. Resend handles email. Quo/OpenPhone supports SMS. UploadThing handles uploads. Mercury is treated as read-only. Google Ads and Meta Marketing API connectors are read-only scaffolds for analysis rather than write surfaces.

## Growth Intelligence

The Growth Intelligence area exists to connect operational outcomes with marketing signals. It focuses on attribution, tracking health, campaign/source performance, estimated gross profit, and advisory recommendations without exposing real campaign details in this public export.

## AI Design

AI is used as an advisory layer, not as an autonomous operator. Structured outputs make AI responses easier to validate and display consistently. Settings-based controls keep AI tools explicit and reviewable.

## Quality Checks

The private project uses linting, TypeScript checks, production builds, Prisma migrations, and focused growth tests. Representative commands include:

- `npx tsc --noEmit`
- `npm run build`
- `npm run test:growth`
