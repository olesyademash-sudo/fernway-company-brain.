# CLAUDE.md

Instructions for Claude and other AI agents working with this repository.

## What this repository is

This is the **Company Brain**, the company's single source of truth.
Everything the team knows is written down here as docs-as-code: plain
Markdown, versioned in Git, with changes made through Pull Requests.

This is **not a codebase**. There is no application to build or test. The
main work is reading, searching, writing and refining documentation.

Other tools (Slack, Notion, Google Drive, Gmail) are sources that feed this
repository. If information in them contradicts what's written here, this
repository is the source of truth. Still, report the discrepancy.

## Structure

```
docs/                 Reference knowledge, grouped by domain
  company/            Mission, values, strategy, ways of working
  engineering/        Architecture, technical decisions, engineering standards
  product/            Product vision, roadmap, specifications
  operations/         Internal operational processes, tools, admin
  go-to-market/       Marketing, sales, positioning, customers
  people/             Onboarding, roles, team processes and policies
runbooks/             Step-by-step procedures ("how to do X")
agents/               Registry of AI agents: purpose, owner, access
templates/            Templates for new documents
meta/                 Documentation about the Company Brain itself
scripts/              Helper scripts for maintaining the repository
tools/                Configurations for integrations with external tools
GLOSSARY.md           Company terms and abbreviations
CONTRIBUTING.md       Rules for making changes (mandatory)
```

Where things go:

- **An explanation of "what it is and why"** → `docs/<domain>/`
- **Step-by-step instructions for "how to do it"** → `runbooks/`
- **A description of an AI agent** → `agents/`
- **A new term or abbreviation** → `GLOSSARY.md`
- **A new document type** → first create a template in `templates/`

## Rules

### 1. Search docs/ first, don't make things up

Before answering any question about the company (processes, decisions,
people, product, customers, tools):

1. Search for the answer in `docs/`, `runbooks/`, `agents/` and `GLOSSARY.md`.
2. Base your answer on what you find, and cite the specific file.
3. If there's no answer, say so. **Don't make things up**, and don't fill
   gaps with assumptions presented as facts.
4. If what you find looks outdated or contradictory, point that out.

A missing answer is a signal that the knowledge needs to be documented.
Suggest creating the relevant document through a Pull Request.

### 2. New information only through Pull Requests

- Never commit or push directly to `main`.
- For any change: create a branch → commit → open a Pull Request.
- Branch names: `docs/<short-description>`, `runbook/<...>`, `agent/<...>`,
  and so on.
- The PR description should explain what changed and where the information
  came from (the source).

### 3. No secrets or sensitive data

No file in this repository may contain:

- passwords, API keys, access tokens, private keys or connection strings;
- customer personal data (names, contacts, addresses, documents and so on);
- financial details (bank details, contract amounts, salaries, financial
  reports).

Instead of a secret, link to where it's stored (for example, "in the password
manager, vault X"), without the value itself.

If you notice such data in the repository, don't copy or quote it. Tell the
user, so it can be removed (and rotated, if it's a secret).

See [CONTRIBUTING.md](CONTRIBUTING.md) for the detailed rules.

## Document style

- Language: English, the company's official working language.
- One document, one topic. Several short files are better than one huge one.
- File names: `kebab-case.md`.
- Start each document with a `#` heading and 1–2 sentences on what it covers.
- Link to other documents with relative paths instead of duplicating them.
- Write so a new colleague can understand without asking follow-up questions.
- Use the templates in `templates/` for new documents, when they exist.
