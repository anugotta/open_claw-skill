# OpenClaw Skills Workspace

This repository contains multiple publish-ready skills across writing style, payments, shopping intelligence, and ordering workflows.

## Skills overview

### Writing-style skills

- `harvey-specter-writing-style/`
  - Rewrites text in a confident, concise, negotiation-first style inspired by Harvey Specter.
  - Includes anti-AI-writing guardrails for more human-sounding output.

- `don-corleone-writing-style/`
  - Rewrites text in a calm, formal, patriarchal dealmaker style inspired by Don Corleone.
  - Includes safety guardrails (no copied quotes, no violent instructions).

### UPI skills pack

- `upi-payment-integration/`
  - Engineering implementation playbook for collect/intent/QR/mandate flows.
  - Webhook reliability, idempotency, reconciliation, and failure handling.

- `upi-payment-ux-ops/`
  - User-facing copy and support operations playbook.
  - Pending/failure/refund/dispute messaging, support macros, and SLA/escalation patterns.

- `upi-go-live-checklist/`
  - Program orchestration from zero setup to go-live decision.
  - Provider matrix, launch gates, memory template, and incident rollback runbook.

### Commerce intelligence skill

- `india-price-tracker/`
  - India-focused multi-store price comparison and monitoring toolkit.
  - Includes effective-price modeling, arbitrage alerts, bulk monitoring, and history trends.
  - Store coverage includes Amazon India, Flipkart, Reliance Digital, Croma, Vijay Sales, Tata CLiQ, JioMart, Myntra, AJIO, Nykaa, and Snapdeal.

### Ordering workflow skill

- `india-food-ordering/`
  - Unified Swiggy + Zomato ordering workflow (with optional additional vendor routing).
  - Strict safety flow: cart preview, address validation, explicit confirmation before order.

## Recommended usage flows

### UPI launches

1. Start with `upi-go-live-checklist/setup.md`.
2. Implement technical flow with `upi-payment-integration`.
3. Prepare customer/support flows with `upi-payment-ux-ops`.
4. Close launch gates in `upi-go-live-checklist/go-live-gates.md`.

### Writing transformations

1. Use `harvey-specter-writing-style` for sharp assertive tone.
2. Use `don-corleone-writing-style` for formal calm authority tone.

### Commerce automation

1. Use `india-price-tracker` for market tracking and pricing opportunities.
2. Use `india-food-ordering` for vendor-comparison ordering workflows with confirmation safeguards.

## Publishing notes

- Publish each skill folder separately (one skill per slug/version).
- First release should use `1.0.0`.
- Recommended initial tags: `latest,stable,v1`.
- For any post-publish edits, bump patch version (`1.0.1`, `1.0.2`, ...).

