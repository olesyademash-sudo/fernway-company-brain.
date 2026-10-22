# Runbook: New Hire Onboarding

A standard workflow for bringing a new team member on board, from the hiring
decision to a fully set-up first week.

| | |
|---|---|
| **Process owner** | Mara Voss (CEO), until a Head of People is hired |
| **Head of People** | Role open |
| **Target** | All accounts ready on **Day 1** |
| **Status** | 🚧 **Draft.** Ownership gaps are marked **TODO**. |

> ⚠️ **Why this runbook exists:** the old Notion checklist says all accounts
> are created on Day 1. In practice it takes until **Week 2**, because nobody
> owns account provisioning. This runbook replaces the Notion checklist, and
> its main job is to give every step an owner.

## Roles

| Role | Who | Responsible for |
|---|---|---|
| **Hiring decision** | Mara | Sourcing candidates and making the hiring decision |
| **Onboarding owner** | **TODO (Mara / future Head of People):** name one person | Running this runbook end to end for each hire |
| **Account provisioning** | **TODO (Mara / future Head of People):** an owner for each tool (see the access checklist) | Creating accounts before Day 1 |
| **Buddy / manager** | **TODO:** define who assigns this | First-week support for the new hire |

## Step 1: Hire confirmed (Mara)

- [ ] Hiring decision made by Mara.
- [ ] Start date, role and team confirmed.
- [ ] Onboarding owner notified, with the start date, role and team.
      *(TODO: through which channel? A public Slack channel, per
      [no decisions in DMs](../docs/company/mission-values.md#1-no-decisions-in-dms).)*

> Keep personal data (contracts, ID documents, bank details, salary) **out of
> this repository**, Slack and tickets.

## Step 2: Before Day 1 (account provisioning)

**Deadline:** every account must be ready **before** the start date.
*(TODO: set a lead time, for example 3 working days before Day 1.)*

### Access checklist

| ✓ | Tool | Who needs it | Who provisions it |
|---|---|---|---|
| [ ] | **1Password** | Everyone. Set this up first, because all other shared logins live here. | **TODO** |
| [ ] | **Slack** | Everyone | **TODO** |
| [ ] | **Google Workspace** | Everyone (email, calendar, docs) | **TODO** |
| [ ] | **HubSpot** | **TODO:** define roles (likely GTM and CS) | **TODO** |
| [ ] | **Linear** | **TODO:** define roles (likely engineering and product) | **TODO** |
| [ ] | **Intercom** | **TODO:** define roles (likely support and CS) | **TODO** |
| [ ] | **Stripe** | **TODO:** define roles (likely Ops and billing) | **TODO** |
| [ ] | **Metabase** | **TODO:** define roles | Uses the shared read-only login in **1Password**, so grant access to the right vault. *TODO: which vault?* |

> **TODO (Mara / future Head of People):** confirm the "who needs it" column
> as a per-role access matrix. Grant only the access each role needs,
> especially for HubSpot, Intercom and Stripe, which hold customer data.

### Also before Day 1

- [ ] **GitHub access** to this repository (the Company Brain). *(TODO: who
      grants it?)*
- [ ] Buddy or manager assigned and told the start date.
- [ ] First-week calendar invites sent. *(TODO: define the standard
      first-week meetings.)*

## Step 3: Day 1

- [ ] New hire signs in to **1Password** first, then to every other tool.
- [ ] Every tool in the access checklist works. Report any gap to the
      onboarding owner **the same day**.
- [ ] Reads the Company Brain:
  - [ ] [README](../README.md)
  - [ ] [Mission & Values](../docs/company/mission-values.md), especially the
        rules on secrets, customer data and Friday deploys
  - [ ] [Team & Roles](../docs/people/team-roles.md)
  - [ ] [Contributing rules](../CONTRIBUTING.md)
- [ ] Joins the relevant Slack channels. *(TODO: list the standard channels.)*

## Step 4: First week

- [ ] Reads the docs for their own area:
  - Engineering → [Architecture](../docs/engineering/architecture.md)
  - Product → [Product Overview](../docs/product/overview.md)
  - Sales / marketing → [Sales & Pricing](../docs/go-to-market/sales-pricing.md)
  - CS / support / ops → [Operations Processes](../docs/operations/processes.md)
- [ ] Opens a first Pull Request to the Company Brain that fixes or adds
      something they had to ask about. This is the
      ["answered twice? write it down"](../docs/company/mission-values.md#2-answered-twice-write-it-down)
      rule in practice.
- [ ] End-of-week check-in with the buddy or manager.
      *(TODO: who runs it, and what's covered?)*

## Step 5: Close out

- [ ] Onboarding owner confirms all steps are done.
- [ ] Any problem with this runbook is fixed in this runbook, through a
      Pull Request.

## Open TODOs (Mara / future Head of People)

1. **Name one onboarding owner.** This is the root cause of the Week 2 delay.
2. **Name an owner for each tool** in the access checklist.
3. **Define the per-role access matrix** (who needs HubSpot, Linear, Intercom,
   Stripe, Metabase).
4. **Set a provisioning lead time** before Day 1.
5. **Define the standard first-week meetings and Slack channels.**
6. **Retire the Notion onboarding checklist** once this runbook is approved.
7. **Write an offboarding runbook** that revokes the same access.
