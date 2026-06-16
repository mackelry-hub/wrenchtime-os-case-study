# Privacy and Scope

This export is designed for a public GitHub case-study repository. It is not an open-source version of the private application.

## Included

- Project overview and problem statement.
- High-level architecture documentation.
- Safe feature descriptions.
- Technical decision notes.
- AI safety notes.
- Roadmap framing.
- High-level Mermaid diagrams.
- A mock dashboard SVG with fake aggregate data.

## Excluded

- Application source code.
- Private database schemas or full Prisma schema dumps.
- Environment files.
- API keys, tokens, webhook secrets, OAuth secrets, or provider credentials.
- Customer names, emails, phone numbers, addresses, quote details, invoices, calendar events, or uploaded files.
- Real financial details, bank transactions, revenue, expenses, tax records, or account identifiers.
- Internal admin route names.
- Proprietary pricing, scheduling, or operating workflows.
- Live screenshots from the private application.

## Redaction Approach

The case study uses high-level module names and generic examples. Diagrams are intentionally broad and use only public-facing architectural language. The dashboard mockup uses invented aggregate metrics and generic labels.

## Publishing Guidance

Before publishing, manually review the repository for accidental additions such as screenshots, copied code, package lockfiles, schema files, `.env` files, exported CSVs, uploaded documents, or terminal logs. This folder should remain a documentation-only artifact.
