# Car Rental Management System with AI Customer Service — Case Study

> Management system for car rental companies with a built-in customer service inbox on the **official WhatsApp API** and an **AI agent that handles customer conversations**.
> **Source code is private.** This repository documents the project; a live demo is available on request.

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000?logo=nextdotjs)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Drizzle](https://img.shields.io/badge/Drizzle_ORM-C5F74F?logo=drizzle&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)

## The problem

Small and mid-sized rental companies juggle bookings, fleet and customers across spreadsheets and phones, and lose rentals because WhatsApp messages go unanswered outside business hours.

## What I built

- **Rental management** — fleet, bookings and customers in one system.
- **Customer service inbox** integrated with the **official WhatsApp Business API**, so the team works every conversation from one screen.
- **AI agent** that answers customers on WhatsApp end to end — availability, prices and booking questions — with the conversation visible to the team, who can step in at any time.
- **Public booking website** (WordPress + Elementor) that reads fleet, prices and rules from the system, so nothing is registered twice and the site never diverges from the back office.
- **Pricing engine** — rates per category, seasons, weekends, taxes and fees, add-ons and packages, pickup locations with their own fees.

## Architecture

```mermaid
flowchart LR
  C[Customer on WhatsApp] --> WA[Official WhatsApp API]
  WA --> S[Rental management system]
  S --> AI[AI agent<br/>answers and qualifies]
  AI --> S
  S --> T[Team inbox<br/>human takeover]
  WEB[Booking website] --> S
  S --> DB[(Database)]
```

## Stack

Next.js (App Router) + React · TypeScript · PostgreSQL with Drizzle ORM · Better Auth · Zod · Tailwind + Radix UI · Docker on a VPS. Quality gates: Vitest, ESLint, dependency-cruiser, Knip and jscpd.

## My role

Product design, architecture, full stack development, WhatsApp API and AI integration, and deployment.

---
Built by **Victor Sestrem** · [LinkedIn](https://www.linkedin.com/in/victor-sestrem/) · victor-sestrem@hotmail.com
