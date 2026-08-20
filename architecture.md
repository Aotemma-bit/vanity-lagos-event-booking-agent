# System Architecture

## High-Level Architecture

```text
                    ┌─────────────────────┐
                    │       Guest         │
                    │      WhatsApp       │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   WhatsApp Trigger  │
                    │     WasenderAPI      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Request Processing│
                    │     & Validation    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      AI Agent       │
                    │ Guest Interaction   │
                    └──────────┬──────────┘
                               │
                ┌──────────────┼──────────────┐
                │              │              │
                ▼              ▼              ▼
          Reservation       Payment       Guest Data
           Processing       Workflow       Processing
                │              │              │
                └──────────────┼──────────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Booking Confirmation│
                    │ & Notifications     │
                    └─────────────────────┘

                               │
                               ▼
                    ┌─────────────────────┐
                    │   Error Handling    │
                    │ & Notifications     │
                    └─────────────────────┘
```

---

## Core Components

### WhatsApp Interface

Provides the guest-facing communication channel for initiating and managing booking requests.

### WasenderAPI

Handles the WhatsApp messaging layer and connects incoming guest interactions to the automation workflow.

### AI Agent

Interprets guest requests and assists with the booking conversation.

### Reservation Workflow

Processes booking information and routes the request through the appropriate reservation logic.

### Payment Workflow

Handles payment-related events within the booking lifecycle.

### Notification System

Sends confirmations and operational messages when important workflow events occur.

### Error Handling

Dedicated error workflows detect failed executions and trigger notifications for investigation.

---

## Booking Lifecycle

```text
Guest Message
      ↓
Request Understanding
      ↓
Booking Information
      ↓
Validation
      ↓
Reservation Processing
      ↓
Payment
      ↓
Confirmation
      ↓
Guest Notification
```

---

## Reliability

The workflow includes dedicated error-handling paths to prevent failed executions from silently going unnoticed.

Execution history is monitored through n8n to identify successful and failed workflow runs.

---

## Security

The following information should never be committed to the repository:

- API keys
- WhatsApp credentials
- Payment credentials
- Database credentials
- Authentication tokens
- Customer personal information
- Webhook secrets

Environment variables and credential management should be used for production deployments.
