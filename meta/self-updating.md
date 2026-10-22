# Keeping the Company Brain Up to Date

How this knowledge base stays current: who reviews, when we check, and how we
flag stale content.

## PR reviewers (document owners)

Every PR needs a review from the owner of the domain it touches:

| Domain | Owner |
|---|---|
| `docs/engineering/`, `docs/product/` | Ivan |
| Customer success (onboarding, CS runbooks) | Lukas |
| `docs/operations/` | Hana |
| `docs/company/`, `docs/go-to-market/`, `docs/people/` | **TODO:** assign owners |

## Rules

- [ ] **Answered twice? Update the doc.** If you answer the same question a
      second time in Slack or a conversation, open a PR to add the answer to
      the right doc ([mission & values, rule 2](../docs/company/mission-values.md#2-answered-twice-write-it-down)).
- [ ] **Spotted something stale? Flag it.** Add this banner at the top of the
      file, right under the `#` heading: `⚠️ Needs update: [Reason / Date]`.
      Example: `⚠️ Needs update: deploy days changed / 2026-11-03`
- [ ] **Fixed it? Remove the banner** in the same PR.

## Quarterly review

Once per quarter, each owner reviews their part of `docs/`:

- [ ] Read every doc in your domain. Is it still true?
- [ ] Fix small things directly in a PR.
- [ ] Add the `⚠️ Needs update` banner to anything you can't fix right away.
- [ ] Look for open `TODO`s and existing banners: `grep -rn "TODO\|Needs update" docs runbooks`.
- [ ] Assign each open item an owner, or close it.
