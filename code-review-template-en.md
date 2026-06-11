# 🔎 Code Review: _MR / feature name_

> **Change summary:** one or two sentences — what this MR changes and why. _E.g.: "adds PATCH /folders/{fid}/rooms/{rid} with the pinned field"._

| | |
|---|---|
| **MR / PR** | _link_ |
| **Branch** | `feature/...` → `develop` |
| **Author** | @… |
| **Reviewer** | @… |
| **Ticket** | _Jira link_ |
| **Size** | _e.g. +320 / −40, 12 files_ |
| **Review date** | _DD.MM.YYYY_ |

---

## ✅ Reviewer checklist

_Based on [Google Engineering Practices](https://google.github.io/eng-practices/review/reviewer/looking-for): look beyond style — review design and behavior too._

### 🏗️ Design & architecture
- [ ] The change belongs here (not in a library / another module) and integrates well with the rest of the system
- [ ] No accidental complexity — the code is no more complex than the task requires
- [ ] No speculative generality (YAGNI): nothing implemented "just in case"
- [ ] API contracts / data schemas agreed (migrations, backward compatibility, account_data, etc.)

### ⚙️ Functionality
- [ ] The code does what the ticket says, and that behavior is right for the users
- [ ] Errors and edge cases handled (invalid input, empty data, concurrent access)
- [ ] Correct response codes / error messages (4xx vs 5xx, clear error body)
- [ ] No regressions in adjacent functionality

### 🔐 Security
- [ ] Access control checked (resource owner, token scope) — no access to other users' data
- [ ] Input is validated; no injections / sensitive data leaks into logs or responses
- [ ] No hardcoded secrets

### 🧪 Tests
- [ ] Unit/integration tests cover the new behavior, including negative scenarios
- [ ] Tests are meaningful: they fail if the code breaks (not "tests for the sake of tests")
- [ ] Test cases from the ticket are covered

### 📖 Readability
- [ ] Clear names for variables, functions, classes
- [ ] Comments explain **why**, not "what" — and there are no more than needed
- [ ] Code follows the project style guide (linter/formatter green)
- [ ] Documentation updated (OpenAPI/Swagger, README, migration notes)

### 🚀 Operations
- [ ] Logging/metrics are sufficient to diagnose issues in production
- [ ] DB migrations are reversible / safe to roll out
- [ ] Performance: no N+1, redundant queries, or locks

---

## 🗒️ Findings

_Severity: 🟥 **blocker** — must not merge; 🟧 **major** — fix in this MR; 🟨 **minor** — separate MR is fine; 💬 **nit** — taste, author's call._

| # | Severity | Where (file:line) | Finding | Status |
|---|----------|-------------------|---------|--------|
| 1 | 🟥 blocker | `path/file.py:123` | … | ⏳ open / ✅ fixed / 🤝 won't fix |
| 2 | 💬 nit | … | … | ⏳ |

## ❓ Questions for the author
- …

## 👍 What went well
_Call out the good parts too — e.g. neat tests, a nice refactoring._
- …

---

## 🏁 Verdict

- [ ] ✅ **Approve** — good to merge
- [ ] 🟡 **Approve with comments** — merge after fixing minor/nit, no re-review needed
- [ ] 🔴 **Request changes** — needs fixes and another review round

**Verdict comment:** …

## 🔗 Links & notes
Ticket, discussion thread, related MRs, follow-up tasks.
