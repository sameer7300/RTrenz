# RTRenz – The AI-Powered Full-Stack Agency Operating System

**Production-ready · Revenue-protected · New York registered · Built by one person**

**Date:** November 2025  
**Author:** Founder & Sole Architect  
**Company:** R TRENZ LLC New York, USA  
**EIN:** 85-3019167  
**Status:** Live, Profitable, : https://rtrenz.com

## What is RTRenz?

RTRenz is the first complete replacement for the traditional digital agency stack.

Founders go from **“I have an idea”** → **AI-generated scope & pricing** → **pay & start** → **live inside a premium client portal** with real-time messaging, tickets, files, invoices, and progress tracking — all inside one legally incorporated New York company.

No email threads. No WhatsApp chaos. No unpaid invoices. Ever.

## The Four Parallel Universes

| Portal                | Route         | Users                     | Purpose                                      |
|-----------------------|---------------|---------------------------|----------------------------------------------|
| Public Marketing Site | `/`           | Anonymous visitors        | Lead generation, AI estimator, trust         |
| Client Portal         | `/dashboard`  | Paying clients            | Projects, messaging, payments, tickets       |
| Developer Portal      | `/developer`  | Internal & freelance devs | Tasks, time tracking, clean workspace        |
| Admin Fortress        | `/admin`      | Owner + future staff      | God-mode control of the entire business     |

All four apps share the same backend, auth, database, and design system — but are completely isolated.

## Tech Stack

| Layer               | Technology                                                                 |
|---------------------|----------------------------------------------------------------------------|
| Frontend            | React 18 + TypeScript + Vite + Tailwind CSS + Framer Motion                |
| Routing             | React Router v6 (nested + file-based)                                      |
| State               | React Query (TanStack) + Context API + Zustand                             |
| Backend             | Django 5 + Django REST Framework + PostgreSQL                              |
| Auth                | JWT + refresh tokens + session timeout wrapper                             |
| Payments            | Stripe (Checkout, Payment Intents, Webhooks)                               |
| Real-time (ready)   | Django Channels (WebSocket layer)                                          |
| Hosting (planned)   | hostinger (frontend) · sperate cloude hosting (backend) · Supabase/AWS RDS (DB)       |
| Analytics           | PostHog (self-hosted ready)                                                |
| Error Tracking      | Sentry                                                                     |

## Core Features (Already Built)

### Public Site
- AI Project Estimator (live cost & timeline)
- AI Scope Generator (natural language → full technical spec)
- Service catalog, portfolio, blog (fully CMS-managed)
- Meeting scheduler with calendar integration
- Complete legal pages (ToS, Privacy, Refund, Cookies)

### Client Portal (`/dashboard`)
- Project dashboard with progress, status, payment banners
- Real-time messaging (client ↔ admin only)
- Dedicated support ticket system
- File vault & document sharing
- Invoice list + one-click payment
- Proposal inbox → accept → auto project creation
- Orange “Complete Payment” enforcement everywhere

### Developer Portal (`/developer`)
- Assigned projects & tasks
- Time tracking & logs
- Messaging to admin only (no client access)
- Minimal, distraction-free UI

### Admin Fortress (`/admin`)
- Full CRM pipeline (leads → proposals → projects → delivery)
- Proposal builder (AI or manual)
- Project creation from meetings or proposals
- Payment, invoice, and refund management
- AI usage analytics
- Content management (services, portfolio, blog)
- Support ticket queue
- User & permission management

### Revenue Protection System
- HTTP 402 Payment Required on unpaid projects
- Orange payment banners on every relevant view
- Two payment models: Pay in Advance (100%) or Pay After Completion (20% down)
- Stripe webhook handling + retry logic
- Chargeback-resistant refund policy

### Legal & Compliance (New York Grade)
- Full Terms of Service
- Dual-model Refund Policy
- CCPA-ready Privacy Policy
- Cookie Policy
- All pages stamped with LLC address, EIN, governing law (NY)

## Project Structure (Frontend)

```bash
src/
├── pages/
│   ├── (public site pages)
│   ├── dashboard/          # Client portal
│   ├── developer/          # Developer portal
│   ├── admin/              # Admin fortress
│   └── legal/
├── components/
│   ├── common/
│   ├── dashboard/
│   ├── admin/
│   └── ui/
├── context/
├── hooks/
├── services/               # API wrappers
├── types/                  # Shared TS interfaces
├── utils/
└── App.tsx                 # The master route file (shown earlier)
