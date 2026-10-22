# Contributing

How to add and change knowledge in the Company Brain.

## 🚫 Hard rules

These rules are non-negotiable. A PR that breaks them doesn't get merged.

1. **All changes go through a Pull Request.** Never commit or push directly
   to `main`.
2. **No secrets.** Never add passwords, API keys, access tokens or other
   credentials to any file. Instead of the value, say where the secret is
   stored (for example, in the password manager).
3. **No customer data.** Never add customer personal or financial data.
4. **Highly sensitive internal data stays outside the repository.** Salaries
   and similar confidential information aren't stored here.
5. **Team knowledge only.** One person's private notes and reflections don't
   belong here. This is a team brain.

> If a secret or sensitive data gets into the repository by accident,
> deleting the file isn't enough: it stays in the Git history. Tell the
> repository owners right away and rotate the compromised secret.

## How to make a change

1. Create a branch from `main` named `feature/<short-description>`, e.g.
   `feature/docs-product` or `feature/runbook-staging-reset`.
2. Add or edit Markdown files (templates are in [templates/](templates/)).
3. Open a Pull Request with a description: what changed and where the
   information came from.
4. Wait for a review from at least one person, then merge.

## Where things go

| What                                   | Where             |
|----------------------------------------|-------------------|
| An explanation of "what it is and why" | `docs/<domain>/`  |
| A step-by-step procedure               | `runbooks/`       |
| A description of an AI agent           | `agents/`         |
| A new term or abbreviation             | `GLOSSARY.md`     |
| A template for a new document type     | `templates/`      |
