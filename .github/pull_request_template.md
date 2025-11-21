## Summary

Describe what changed in 1–2 sentences.

## Motivation

Explain why this change is needed. “See linked issue.” is fine if applicable.

## Related Issues / Tickets

List linked issues (e.g., “Closes #123”) or write “None”.

## Type of Change

- [ ] Feature
- [ ] Bug fix
- [ ] Refactor
- [ ] Chore / maintenance
- [ ] Documentation
- [ ] Breaking change (requires release note or migration guide)

## Testing

Template smoke-test (main verification):

- [ ] `copier copy --vcs-ref dev gh:stfukuda/python-package destination`
- [ ] `cd destination && just setup`
- [ ] `just sync`
- [ ] `just format && just lint && just check && just test`
- [ ] `just docs` / `just docs-serve`
- [ ] `just build`

Additional targeted tests (if any):

- Mention other focused checks (e.g., `markdownlint README.md`).

## Checklist

- [ ] Documentation updated (if needed)
- [ ] Tests added/updated or confirmed not needed
- [ ] `pre-commit` / linters / formatters pass locally
- [ ] Linked related issue(s) and added release note if breaking
- [ ] Security/privacy impact considered (if applicable)
