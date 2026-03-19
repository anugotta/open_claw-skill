# UPI Skills Pack

This workspace contains a 3-skill UPI playbook set.

## Skills overview

- `upi-payment-integration/`
  - Engineering implementation for collect/intent/QR/mandate flows
  - Webhook reliability, idempotency, reconciliation, and technical failure handling

- `upi-payment-ux-ops/`
  - User messaging, support macros, refund/dispute communication, and incident copy

- `upi-go-live-checklist/`
  - Program orchestration from onboarding to go/no-go decision
  - Provider matrix, launch gates, and incident runbook

## When to use what

- Building backend flow or fixing payment correctness:
  - use `upi-payment-integration`

- Designing customer states or support process:
  - use `upi-payment-ux-ops`

- Planning release milestones, blockers, and approvals:
  - use `upi-go-live-checklist`

## Recommended end-to-end sequence

1. Start with `upi-go-live-checklist/setup.md`.
2. Execute technical work using `upi-payment-integration`.
3. Execute UX/ops work using `upi-payment-ux-ops`.
4. Return to `upi-go-live-checklist/go-live-gates.md` for final gate review.
5. Keep incident procedures from `upi-go-live-checklist/incident-runbook.md` ready for launch day.

## Publishing

Example publish commands:

```bash
clawhub publish ./upi-payment-integration --slug upi-payment-integration --name "UPI Payment Integration" --version 1.0.0 --tags latest,stable,v1 --changelog "Initial release"
clawhub publish ./upi-payment-ux-ops --slug upi-payment-ux-ops --name "UPI Payment UX and Ops" --version 1.0.0 --tags latest,stable,v1 --changelog "Initial release"
clawhub publish ./upi-go-live-checklist --slug upi-go-live-checklist --name "UPI Go Live Checklist" --version 1.0.0 --tags latest,stable,v1 --changelog "Initial release"
```

