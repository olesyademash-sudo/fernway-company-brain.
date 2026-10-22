# Engineering Architecture

Fernway's engineering tools and infrastructure, how code gets to production,
and the technical issues we know about.

## Tech stack & infrastructure

| Tool | Purpose | Access / owner |
|---|---|---|
| **Linear** | Ticket tracking | — |
| **Metabase** | Metrics and reporting on top of the production DB | Shared **read-only** login, stored in **1Password** |
| **n8n** | Internal automations | Self-hosted instance, run by **Ivan** |

> The Metabase login is shared and read-only. Get it from 1Password, and never
> copy it into docs, Slack or code.

## Deployment & release process

```
Linear ticket  →  Pull Request  →  QA on staging (Ana)  →  Deploy
```

1. **Linear ticket.** Every change starts as a ticket in Linear.
2. **Pull Request.** The work is opened as a PR that links to the ticket.
3. **Staging QA.** **Ana** tests the change on staging.
4. **Deploy.** Approved changes go out on a deploy day.

### Deploy schedule

| Day | Deploys |
|---|---|
| Monday | — |
| **Tuesday** | ✅ Deploy day |
| Wednesday | — |
| **Thursday** | ✅ Deploy day |
| **Friday** | ⛔ **Friday freeze: no deploys** |

The Friday freeze is a strict rule. See
[Mission & Values](../company/mission-values.md).

## Staging environment

Staging is where every change is tested before release.

- **Reset process:** currently known **only by Ana**. See the runbook [Staging reset](../../runbooks/staging-reset.md) (draft; Ana still needs to write the steps).

## Known tech issues

### n8n workflows contain hardcoded API keys

- **Problem:** some n8n workflows have API keys written directly into them
  instead of pulling them from a credential store.
- **Risk:** anyone with access to the n8n instance or its exports can see
  those keys. This breaks our rule that secrets live only in 1Password.
- **Status:** open.

### CSV staff importer fails on some files

- **Problem:** the staff CSV importer fails when:
  - the file contains **non-Latin characters**, or
  - the file was created in **Apple Numbers**.
- **Workaround:** see the runbook [CSV importer fails during onboarding](../../runbooks/csv-importer-fix.md). The fix steps are still to be written by **Noor**.
- **Status:** open.

## ⚠️ Knowledge gaps (single points of failure)

The following knowledge lives in one person's head. That is exactly what the
Company Brain exists to prevent. Each item should become a runbook in
[`runbooks/`](../../runbooks/).

| Knowledge | Only known by | Should become |
|---|---|---|
| How to reset staging | Ana | [`runbooks/staging-reset.md`](../../runbooks/staging-reset.md) (draft) |
| CSV importer workaround | Noor | [`runbooks/csv-importer-fix.md`](../../runbooks/csv-importer-fix.md) (draft) |
| How the n8n instance is hosted and run | Ivan | `runbooks/n8n-operations.md` |
