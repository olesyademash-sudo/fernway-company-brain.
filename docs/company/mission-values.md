# Mission & Values

Who Fernway is, what we build, and the values and rules that shape how we work.

> **TODO:** Add the official one-line mission statement once it's agreed.

## Company at a glance

| | |
|---|---|
| **Name** | Fernway |
| **Type** | B2B SaaS |
| **Founded** | 2024 |
| **Registered in** | Berlin, Germany |
| **Work model** | Remote-first, with the team spread across 5 countries |
| **Working language** | English |

## Product

**Fernway Shifts** handles shift planning and labor-cost forecasting for
independent café and restaurant groups.

- **Who it's for:** independent groups with **3–20 locations**.
- **What it does:** plans staff shifts and forecasts labor costs across venues.

## Positioning

**Fast onboarding is our edge.**

Enterprise competitors take weeks to configure. With Fernway, we aim for a
venue to **go live in under a day**.

### Core metric: T2L (Time To Live)

**T2L** is the time from **contract signed** to **first schedule published**
(see [Product Overview](../product/overview.md#t2l-time-to-live)). It is the
core metric we watch.

- **Target:** under a day.
- **In practice:** some onboardings take 1–3 days.

When we prioritize work, ask whether it brings T2L closer to under a day.

## Values & rules

These apply to everyone at Fernway, people and AI agents alike.

### 1. No decisions in DMs

Make decisions in **public Slack channels only**. If a decision happens in a
DM or a call, post it in the relevant public channel. Then the whole team can
see it, search for it, and question it.

### 2. Answered twice? Write it down

If you answer the same question a second time, write the answer down in this
repository. Nobody should be the only person who knows something.

### 3. Customer data stays in designated systems

Customer data lives only in its designated systems:

- **HubSpot** for CRM and customer relationships
- **Stripe** for billing and payments
- **The production database** for product data

Never export customer data into docs (including this repo) or AI tools.

### 4. Secrets stay in 1Password

Passwords, API keys, tokens and other credentials are stored **only in
1Password**. Never paste them into Slack, docs, code or AI tools. If you need
to point to a secret, name the 1Password item, never its value.

### 5. No deploys on Friday

We have a **Friday freeze**: no production deploys on Fridays, so issues don't
roll into the weekend.

### 6. English is the official working language

Write in **English** in shared channels, documentation and decisions, so
everyone across our 5 countries can take part.

## Related

- [Contributing rules](../../CONTRIBUTING.md)
- [Glossary](../../GLOSSARY.md)
