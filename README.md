# 🎟️ Vanity Lagos Club — Automated Event Booking Agent

An AI-powered event booking automation system designed for Vanity Lagos Club.

The system automates the guest booking journey through WhatsApp, allowing customers to make booking requests while the workflow processes reservation data, handles payment-related events, and triggers confirmations and operational notifications.

---

## Workflow Architecture

![Workflow Architecture](images/workflow.png)

---

## Overview

The system combines AI agents, WhatsApp automation, API integrations, database operations, payment processing, and error handling into a single automated booking workflow.

The goal is to reduce manual booking operations while providing guests with a faster and more consistent booking experience.

---

## Key Features

- WhatsApp-based event booking
- AI-powered guest interaction
- Automated reservation processing
- Guest information management
- Event and booking data processing
- Payment workflow integration
- Automated booking confirmations
- Operational notifications
- Error handling and recovery workflows
- API-based integrations
- Workflow execution monitoring

---

## Workflow Process

### 1. Guest Interaction

A guest initiates a booking conversation through WhatsApp.

### 2. Request Processing

The incoming request is processed and routed through the booking workflow.

### 3. AI Agent

The AI agent interprets the guest's request and assists with the booking process.

### 4. Reservation Processing

Booking information is validated and processed through the connected backend systems.

### 5. Payment

Payment-related events are processed as part of the booking lifecycle.

### 6. Confirmation

Once the booking workflow reaches the appropriate state, confirmation messages and operational notifications are triggered.

### 7. Error Handling

Dedicated error-handling workflows monitor failures and provide notifications when an execution encounters an issue.

---

## Technology Stack

- n8n
- AI Agents
- WhatsApp
- WasenderAPI
- REST APIs
- JavaScript
- Payment Integration
- Database / Data Storage
- Workflow Automation

---

## Architecture

See [architecture.md](architecture.md) for a detailed overview of the system design.

---

## Workflow Execution

![Workflow Executions](images/executions.png)

The workflow has been tested through multiple executions, including successful runs and error-handling scenarios.

---

## Business Impact

This automation is designed to help an entertainment venue:

- Reduce manual booking operations
- Respond to guests faster
- Standardize the reservation process
- Reduce booking errors
- Automate payment-related workflows
- Improve operational visibility
- Scale guest handling without proportionally increasing administrative workload

---

## Project Type

**AI Automation • Hospitality & Entertainment • Event Booking • WhatsApp Automation • Workflow Engineering**

---

## Disclaimer

This repository contains documentation and architecture information for a production-style automation project.

Credentials, API keys, private customer information, payment secrets, and other sensitive configuration values are intentionally excluded.
