# Operations Processes

How we onboard customers, handle support escalations, manage billing, and
which tools we use.

## Customer onboarding

**Owner:** Lukas · **Target T2L:** under a day (in practice, sometimes 1–3 days)

```
Contract signed (HubSpot)
  → 45-min setup call
  → CSV import of venues & staff
  → Configure pay rules
  → 1st schedule published      ← T2L stops here
  → 7-day check-in
  → Handover to support
```

| # | Step | Notes |
|---|---|---|
| 1 | **Contract signed** in HubSpot | T2L clock starts. |
| 2 | **Setup call** (45 min) | |
| 3 | **CSV import** of venues and staff | The importer fails on non-Latin characters and Apple Numbers files. See [known issues](../engineering/architecture.md#csv-staff-importer-fails-on-some-files). |
| 4 | **Configure pay rules** | Local break and overtime rules, per country. |
| 5 | **First schedule published** | T2L clock stops. |
| 6 | **7-day check-in** | |
| 7 | **Handover to support** | The customer moves to the support escalation path below. |

See [Product Overview](../product/overview.md) for the definitions of T2L and
pay rules.

## Support escalation

**Owner:** Jonas · **Entry point:** Intercom inbox

```
Intercom inbox
  → Jonas  (1st line)
  → Ana    (technical issues)
  → Noor   (production incidents)
  → Ivan   (anything involving customer data)
```

| Level | Who | Handles |
|---|---|---|
| Entry | Intercom inbox | All incoming customer requests |
| 1st line | **Jonas** | Triage and first response |
| Technical | **Ana** | Technical issues |
| Incidents | **Noor** | Production incidents |
| Customer data | **Ivan** | Anything involving customer data |

> Customer data stays in its designated systems (HubSpot, Stripe, the
> production DB). Never copy it into tickets, Slack, docs or AI tools while
> escalating. See [Mission & Values](../company/mission-values.md#3-customer-data-stays-in-designated-systems).

## Billing & payments

**Owner:** Hana · **System:** Stripe

- **Invoicing:** monthly, **per venue**, at **€39 / month / venue**.
- **Failed payments:** Hana checks them **manually every Monday**.

## Tooling stack

| Tool | Used for |
|---|---|
| **Slack** | Team communication. Decisions go in public channels only. |
| **Notion** | ⚠️ **Legacy docs.** This repository is now the source of truth. |
| **HubSpot** | CRM and contracts |
| **Linear** | Tickets |
| **Intercom** | Customer support inbox |
| **Stripe** | Billing and payments |
| **Google Workspace** | Email, calendar and documents |
| **Metabase** | Metrics on the production DB |
| **n8n** | Internal automations |
| **1Password** | All secrets and shared logins |

## ⚠️ Single points of failure

Each process below depends on one person, and none of them is documented as
a runbook yet:

| Process | Depends on | Should become |
|---|---|---|
| Customer onboarding | Lukas | `runbooks/customer-onboarding.md` |
| 1st-line support | Jonas | `runbooks/support-triage.md` |
| Failed-payment check | Hana | `runbooks/failed-payments-check.md` |

## Related

- [Mission & Values](../company/mission-values.md)
- [Product Overview](../product/overview.md)
- [Engineering Architecture](../engineering/architecture.md)
