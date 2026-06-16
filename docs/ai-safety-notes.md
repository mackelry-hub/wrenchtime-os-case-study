# AI Safety Notes

WrenchTime OS uses AI as an internal advisory tool. The system is designed around human review and constrained outputs rather than autonomous action.

## Safety Principles

- AI suggestions are advisory, not automatically executed.
- AI tools are controlled through settings.
- Structured outputs are preferred over free-form responses for operational recommendations.
- AI does not autonomously contact customers.
- AI does not write to ad accounts.
- AI does not initiate payments, refunds, or financial transfers.
- AI does not modify banking records.

## Intended AI Uses

- Summarizing operational signals.
- Generating internal advisory notes.
- Highlighting tracking-health concerns.
- Suggesting areas to review in campaigns or workflows.
- Producing structured recommendations for human evaluation.

## Out-of-Scope AI Uses

- Sending customer messages without approval.
- Changing quote terms, payment amounts, or schedules.
- Mutating Google Ads or Meta ad accounts.
- Making final accounting, tax, or legal decisions.
- Accessing secrets or raw private records from public artifacts.

## Public Case-Study Boundary

This export does not include prompts, system instructions, customer records, private business rules, or real examples from the production system. The AI discussion is limited to high-level safety architecture and product intent.
