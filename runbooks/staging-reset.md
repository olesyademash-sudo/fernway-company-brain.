# Runbook: Staging Reset

How to safely reset the staging environment before the Tuesday and Thursday
testing and release cycle.

| | |
|---|---|
| **Owner / expert** | Ana Silva (QA & Tech Support) |
| **Backup** | **TODO:** name a second person who has done a reset with Ana |
| **When** | Before testing for a Tuesday or Thursday deploy |
| **Never** | ⛔ On a **Friday** |
| **Status** | 🚧 **Draft.** The exact commands and steps are a **TODO for Ana**. |

> ⚠️ **Single point of failure:** Ana is currently the **only** person who
> knows how to reset staging. If Ana is unavailable, staging can't be reset,
> which blocks QA and the [release process](../docs/engineering/architecture.md#deployment--release-process).
>
> **Ana: please fill in every TODO below before your upcoming vacation,** and
> walk the backup through one real reset using only this runbook.

## Safety rules

1. ⛔ **Never reset staging on a Friday.** This follows the
   [Friday freeze](../docs/company/mission-values.md#5-no-deploys-on-friday).
2. **Never point any step at production.** Check which environment you're on
   before running anything. *(TODO, Ana: how do you tell staging and
   production apart: URL, context, profile?)*
3. **Credentials stay in 1Password.** Never paste staging credentials into
   this runbook, Slack, a terminal history you share, or AI tools. Reference
   the 1Password item by name only. *(TODO, Ana: which item?)*
4. **Announce before you reset.** A reset can wipe in-progress testing. Post
   in a public Slack channel first. *(TODO: which channel?)*

## When to reset

| Deploy day | Reset by |
|---|---|
| **Tuesday** | **TODO (Ana):** e.g. Monday afternoon or Tuesday morning? |
| **Thursday** | **TODO (Ana):** e.g. Wednesday afternoon or Thursday morning? |
| **Friday** | ⛔ Never |

Other triggers: **TODO (Ana):** are there other situations that need a
reset, such as broken test data or a failed migration?

## Step 1: Pre-checks

- [ ] Today is **not Friday**.
- [ ] Announced in Slack (see safety rule 4), and nobody is mid-test.
- [ ] You have the access you need. *(TODO, Ana: list the tools, access and
      1Password items.)*
- [ ] You've confirmed you're targeting **staging**, not production.

## Step 2: Reset

> 🚧 **TODO (Ana):** replace this block with the exact steps and commands, in
> order. Use placeholders for secrets, e.g. `<from 1Password: item name>`.

```bash
# TODO (Ana): step-by-step commands
# 1. ...
# 2. ...
```

Please also document:

- [ ] **What a reset actually does:** wipe the DB? Restore a snapshot? Re-seed
      data? Redeploy a branch?
- [ ] **Where the test or seed data comes from.** Does staging ever contain
      copies of **production or customer data**? If so, say how it's
      anonymized. Customer data must stay in
      [designated systems](../docs/company/mission-values.md#3-customer-data-stays-in-designated-systems).
- [ ] **How long a reset takes.**

## Step 3: Verify

> 🚧 **TODO (Ana):** how do we confirm the reset worked?

- [ ] Staging is reachable. *(TODO: URL or health check)*
- [ ] Test data is in the expected state. *(TODO: what to check)*
- [ ] A basic smoke test passes. *(TODO: which flows: sign-in, build a
      schedule, publish?)*
- [ ] Posted "staging reset done" in Slack.

## Step 4: If something goes wrong

> 🚧 **TODO (Ana):** list the common failures and fixes, and how to roll back.

- **Who to escalate to if Ana is unavailable:** **TODO.** Likely Noor
  (Backend Lead, on-call). Please confirm.

## Related

- [Engineering Architecture: staging environment](../docs/engineering/architecture.md#staging-environment)
- [Release process & deploy schedule](../docs/engineering/architecture.md#deployment--release-process)
- [Mission & Values: Friday freeze](../docs/company/mission-values.md#5-no-deploys-on-friday)
