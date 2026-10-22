# Runbook: CSV Importer Fails During Onboarding

What to do when a customer's venue or staff CSV fails to import during
onboarding.

| | |
|---|---|
| **Used by** | Lukas (Customer Success), Support (Jonas) |
| **Owner / expert** | Noor Haddad |
| **When** | Step 3 of [customer onboarding](../docs/operations/processes.md#customer-onboarding): the CSV import fails |
| **Status** | 🚧 **Draft.** The fix steps (section 3) still need to be written by Noor. |

## 1. Recognize the problem

The CSV importer has two known failure causes. See the
[known issue](../docs/engineering/architecture.md#csv-staff-importer-fails-on-some-files).

| Cause | How to check |
|---|---|
| **Non-Latin characters** | Look for names or text with characters outside the basic Latin alphabet. |
| **File exported from Apple Numbers** | Ask the customer which program they used to create or export the file. |

> 🔒 The CSV contains customer staff data. Don't forward it in Slack or
> email, and don't paste it into docs or AI tools. Customer data stays in its
> designated systems. See
> [Mission & Values](../docs/company/mission-values.md#3-customer-data-stays-in-designated-systems).

## 2. Before you start

- [ ] Note which cause applies: non-Latin characters, Apple Numbers, both, or
      neither.
- [ ] Note the customer account and venue in HubSpot or the Intercom thread,
      not here.

## 3. Fix the file

> 🚧 **TODO (Noor):** write the exact workaround steps here. Until then,
> **don't improvise. Go to step 5 and contact Noor.**
>
> Please cover:
> - How to fix a file with non-Latin characters
> - How to fix a file exported from Apple Numbers
> - What to do if the file has both problems
> - Which tools are safe to use without sending customer data outside our
>   designated systems

## 4. Re-import and verify

- [ ] Re-run the CSV import.
- [ ] Check that every venue and staff member came through.
- [ ] Check that names with non-Latin characters appear correctly.
- [ ] Continue onboarding: [configure pay rules](../docs/operations/processes.md#customer-onboarding).

## 5. Escalate if it still fails

Escalate to **Noor** if:

- the fix doesn't work,
- the failure doesn't match either known cause, or
- section 3 is still a TODO.

Follow the [support escalation path](../docs/operations/processes.md#support-escalation).
Describe the problem without attaching or pasting the customer's file.

> ⏱️ Every failed import delays T2L, which targets under a day. Escalate early
> rather than spending hours on it.

## Related

- [Known issue: CSV staff importer](../docs/engineering/architecture.md#csv-staff-importer-fails-on-some-files)
- [Customer onboarding](../docs/operations/processes.md#customer-onboarding)
