# 📋 Jira Issue Templates

Ready-to-use Jira issue description templates written in **wiki markup** (Text Formatting Notation).
Copy a template → paste it into the *Description* field → fill in the placeholders. Every issue looks the same, and nothing important gets forgotten.

> The markup works in fields with the **Wiki Style Renderer** mode. In the new cloud editor, paste the text via the `{}` / Markdown-insert mode.

> 🇷🇺 Russian version: [`README.md`](README.md). The Russian templates are the files without the `-en` suffix.

---

## 🧩 Template types

| Type | File | When to use |
|------|------|-------------|
| 🚀 **Epic** | [`epic-template-en.txt`](epic-template-en.txt) | A large feature made of several stories/tasks (often cross-team) |
| ⭐ **Story** | [`story-template-en.txt`](story-template-en.txt) | User value: "*as a role, I want …, so that …*" |
| 🛠️ **Task** | [`task-template-en.txt`](task-template-en.txt) | Technical work without a direct user story |
| 🐞 **Bug** | [`bug-template-en.txt`](bug-template-en.txt) | Something is broken: steps, expected/actual, root cause |
| 🔎 **Code Review** | [`code-review-template-en.md`](code-review-template-en.md) | MR/PR review: checklist, findings with severity, verdict. **Markdown** — for GitLab/GitHub or a Jira comment |

### 📂 Structure

```
jira-templates/
├── epic-template.txt / epic-template-en.txt                    # 🚀 epic
├── story-template.txt / story-template-en.txt                  # ⭐ story
├── task-template.txt / task-template-en.txt                    # 🛠️ task
├── bug-template.txt / bug-template-en.txt                      # 🐞 bug
├── code-review-template.md / code-review-template-en.md        # 🔎 code review (markdown)
└── README.md / README-en.md
```

---

## 🎨 Markup cheat sheet

Panel colors follow Jira's standard palette:

| Panel | `bgColor` | Where we use it |
|-------|-----------|-----------------|
| 🔵 Info / Story summary | `#DCEAFF` | story intro block |
| 🟣 Epic / Task summary | `#EAE6FF` / `#E8E7FF` | epic / task intro block |
| 🟢 Acceptance Criteria / DoD | `#E3FDEE` | acceptance criteria |
| 🟠 Breaking change | `#FFF0E6` | warning about a breaking change |
| 🔴 Bug summary | `#FEEBE7` | bug intro block |

Core constructs:

```jira
{panel:title=Title|bgColor=#E3FDEE} panel body {panel}

h3. Section heading             # h3. / h4. — headings
*bold*  _italic_                # emphasis
{{monospace}}                   # inline code / field & branch names
* [ ] checklist item            # acceptance-criteria item
# numbered step                 # test cases
[Text|https://link]             # link

{code:json}
{ "example": "code block" }
{code}
```

---

## ✅ How to use

1. Open the needed `*-template-en.txt` and copy its contents.
2. Paste into the **Description** field when creating a Jira issue.
3. Replace the placeholders (`_italic hints_` and `…`) with real data.
4. Delete blocks that don't apply (e.g. the *Breaking change* panel if there's none).
5. Align on the *Acceptance Criteria* section before development starts.

> 💡 Tip: the `* [ ]` checkboxes in the criteria panel render as visible, clickable progress tracking in Jira.
