---
alwaysApply: true
scene: git_message
---

Use Conventional Commits with Gitmoji. All commit messages must be in English.

## Format

```
<emoji> <type>(<scope>): <subject>

[body]

[footer]
```

- **emoji**: required, Gitmoji matching the type (see table below)
- **type**: required, see type table below
- **scope**: optional, module or area affected, e.g. `auth`, `api`, `ui`
- **subject**: required, ≤50 chars, imperative mood, lowercase, no trailing period
- **body**: optional, ≤72 chars per line, explain *why* not *what*; omit if it would only restate the subject
- **footer**: optional, for Issue references or Breaking Changes

## Type & Gitmoji

| Emoji | Type       | When to use                              |
|-------|------------|------------------------------------------|
| ✨    | `feat`     | Introduce a new feature                  |
| 🐛    | `fix`      | Fix a bug                                |
| 📝    | `docs`     | Documentation changes only               |
| 🎨    | `style`    | Code style/formatting, no logic change   |
| ♻️    | `refactor` | Refactor code, not a fix or feature      |
| ✅    | `test`     | Add or update tests                      |
| 🔧    | `chore`    | Build process, dependency updates, tools |
| ⚡️    | `perf`     | Improve performance                      |
| 👷    | `ci`       | CI/CD configuration changes              |
| ⏪️    | `revert`   | Revert a previous commit                 |
| 🔒️    | `security` | Fix a security issue                     |
| 💄    | `ui`       | Update UI or styles                      |
| 🚀    | `deploy`   | Deploy or release related changes        |
| 🗑️    | `remove`   | Remove code or files                     |

## Rules

1. **All parts of the commit message — subject, body, and footer — must be written in English. Never use any other language.**
2. Use imperative mood: `add`, `fix`, `update` — not `added`, `fixed`
3. Breaking changes: append `!` after type, add `BREAKING CHANGE: <desc>` in footer
4. Reference issues in footer: `Closes #123` or `Fixes #456`

## Examples

```
✨ feat(auth): add OAuth2 login support

🐛 fix(api): handle null response from payment gateway

📝 docs: update README with setup instructions

♻️ refactor(cart): extract price calculation to separate service

✨ feat(api)!: change response format to JSON:API spec

BREAKING CHANGE: response envelope changed from { data } to { data, meta }

🐛 fix(checkout): prevent duplicate order submission

User could click submit multiple times before the request completed.
Added debounce and disabled state after first click.

Closes #234
```