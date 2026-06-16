# Feature Overview

This document summarizes the product areas at a safe level for a public case study. It avoids private workflows, real customer records, private route names, and implementation-specific business rules.

## Admin Operations

The admin UI is designed for a service-business operator who needs a quick view of current quotes, scheduled jobs, deposits, balances, expenses, tracking health, and advisory notes. The interface is mobile-friendly and PWA-oriented so the system can be used while away from a desk.

## Quote and Schedule Workflows

The private system supports the operational path from customer interest to scheduled work. The public case study does not include exact workflow rules, pricing logic, quote fields, or private job details.

## Payments

Stripe Checkout is used for payment collection, with webhook handling for payment state updates. The system supports deposit and final-balance concepts. Public materials use only generic terms and mock values.

## Communications

Email communication is handled through Resend. SMS support is oriented around Quo/OpenPhone, while Twilio is treated as legacy/disabled. This case study does not include message templates, real phone numbers, customer contact details, or private communication logs.

## Calendar and Scheduling

Google Calendar integration supports scheduling around the business timezone, America/Detroit. The case study does not expose calendar IDs, real appointments, or operational scheduling rules.

## Uploads

UploadThing supports file upload workflows in the private application. The public case study does not include stored files, upload URLs, customer attachments, or media from real jobs.

## Accounting and Banking

The accounting area includes read-only banking concepts, manual expenses, annotation patterns, and CPA/year-end export support. The case study intentionally avoids bank account details, transaction exports, vendor lists, real expenses, tax details, and exact database structures.

## Growth Intelligence

Growth Intelligence brings together tracking health, campaign/source attribution, estimated gross profit, and advisory notes. The private implementation includes read-only connector scaffolds for Google Ads and Meta Marketing APIs, plus browser-side conversion tracking concepts for Meta Pixel and Google Ads gtag.

## AI Advisory

AI workflows use the OpenAI API for structured advisory outputs. These tools are settings-controlled and designed for human review. They do not autonomously contact customers, modify ad accounts, or execute business actions.
