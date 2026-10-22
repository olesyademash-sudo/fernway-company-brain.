# Agent: Support Draft Assistant

A Claude-based assistant that drafts replies to support tickets in Intercom.

| | |
|---|---|
| **Status** | 🧪 **Experimental** (trial) |
| **Model / tool** | Claude |
| **Used in** | Intercom: draft replies for support tickets |
| **Owner** | **TODO:** name an owner (likely support, Jonas, or Ivan for automations) |
| **Users** | **TODO:** who uses it day to day? |
| **Started** | **TODO:** trial start date |

## What it does

- Helps with **support ticket triage** by drafting a reply for each ticket.
- Produces **drafts only**. A person reviews, edits and sends every reply.
  *(TODO: confirm that it never sends anything on its own.)*

## Hard rule

> ⛔ **No raw customer PII or payment data goes to AI tools.**

That means:

- No customer names, emails, phone numbers, addresses or staff lists
  (including CSV files) in prompts.
- No payment or billing data (Stripe details, invoices, card information).
- If a ticket needs that data to answer, **write the reply manually.**

This follows the company-wide rule that
[customer data stays in designated systems](../docs/company/mission-values.md#3-customer-data-stays-in-designated-systems).

## ⚠️ Open questions

Answer these before the trial goes beyond experimental:

1. **How does ticket content reach Claude?** Through a built-in Intercom
   integration, copy-paste, or an automation (for example n8n)? Ticket text
   often contains customer names and emails, so whoever owns the trial needs
   to show how the hard rule is enforced in practice: stripping or masking
   PII before the text is sent, not just relying on a policy.
2. **Data handling:** is this Claude account or setup configured so that
   inputs aren't retained or used for training? Who confirmed it?
3. **Access:** what can the agent see in Intercom: all tickets, or only the
   ones it's asked about? Which credentials does it use (stored in 1Password)?
4. **Success criteria:** what metric decides whether the trial is adopted or
   stopped (time to first reply, edit rate, CSAT)?
5. **Kill switch:** who can turn it off, and how?

## Related

- [Support escalation](../docs/operations/processes.md#support-escalation)
- [Mission & Values](../docs/company/mission-values.md)
