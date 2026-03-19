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

### Payment operations skills

- `payment-incident-responder/`
  - Incident response playbook for payment outages and state mismatches.
  - Includes severity model, comms templates, and postmortem structure.

- `catalog-sku-matcher-india/`
  - India-focused catalog matching skill for cross-store SKU normalization.
  - Includes variant guardrails, confidence scoring, and review-queue patterns.

### Growth and operations skills

- `receipt-expense-reconciler/`
  - Parses receipts/invoices, categorizes spend, detects anomalies, and prepares tax-ready summaries.

- `social-repurpose-engine/`
  - Converts long-form content into LinkedIn/X/newsletter/email variants with channel-specific structure.

- `website-change-watcher/`
  - Monitors tracked pages, detects meaningful diffs, and summarizes business impact/actions.

- `customer-support-autopilot/`
  - Classifies support tickets, drafts safe responses, and recommends SLA-aware escalation paths.

- `app-review-intelligence/`
  - Clusters app review feedback, finds pain-point trends, and maps insights to product backlog priorities.

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
3. Use `catalog-sku-matcher-india` to improve listing-match accuracy before cross-store comparisons.

### Payment reliability operations

1. Use `payment-incident-responder` during incidents for triage, containment, comms, and recovery.
2. Use `upi-go-live-checklist` and `upi-payment-integration` to prevent repeat payment failures.

### Ops and growth workflows

1. Use `receipt-expense-reconciler` for monthly/quarterly finance hygiene and anomaly checks.
2. Use `website-change-watcher` to track competitor pricing/docs/policy shifts.
3. Use `customer-support-autopilot` for faster, policy-safe response drafting and escalation.
4. Use `app-review-intelligence` to convert user feedback into prioritized roadmap inputs.
5. Use `social-repurpose-engine` to repurpose product updates into multi-channel content packs.

## Publishing notes

- Publish each skill folder separately (one skill per slug/version).
- First release should use `1.0.0`.
- Recommended initial tags: `latest,stable,v1`.
- For any post-publish edits, bump patch version (`1.0.1`, `1.0.2`, ...).

