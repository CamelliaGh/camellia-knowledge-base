# 🔧 Prompt Templates for Developers

This document contains reusable **prompt templates** for tasks like refactoring code, writing tests, planning features, and generating documentation. These templates are designed to help developers get more consistent and high-quality results from AI tools like ChatGPT, Claude, or Cursor.

---

## 📌 About This Folder

There are **two versions** of the prompt template library in this repository:

| File | Purpose |
|------|---------|
| `prompt-templates.md` _(you’re reading this)_ | Human-friendly Markdown version for browsing, copying, and learning |
| `prompt-templates.mdc` | Cursor **Rule file** version, designed to load inside the AI context of tools like Cursor and Claude Code |

If you want to **use these templates directly inside Cursor**, open or move the `.mdc` file into:

```
.your-project/.cursor/rules/prompt-templates.mdc
```

Then, activate it inside Cursor via the **Command Palette → Toggle AI Rules**.

---

## 📚 Template Library

> 💡 _Tip: Use `Cmd+F` or search in the sidebar to find templates by task (feature planning, testing, debugging, etc.)._

### 🧱 General Structure Template

```
Role: [who the model should act as]
Task: [what to do]
Context: [background if needed]
Constraints: [word limits, tone, format, etc.]
Output Format: [list, table, code, etc.]
```

---

### ⚡ Refactor Code

```
Role: Senior JavaScript Engineer
Task: Refactor the following function to improve readability and performance.
Context: ES6+, no external dependencies.
Constraints: Keep functionality identical. Improve naming. Add JSDoc comments.
Output Format: Updated code only.
```

---

## 🔗 Cursor Version (for Tooling Integration)

For developers using Cursor or Claude Code, the structured rule version of this file is available at:

📄 `/.cursor/rules/prompt-templates.mdc`

This version includes metadata like `manual: true` and `alwaysApply: false`, so it doesn’t auto-inject — but it’s available any time you need these templates in your coding session.

---

## 🛠 Contributing

Want to add your own prompt templates or improve existing ones?

1. Fork the repo
2. Add or edit prompts in **both** versions (Markdown & `.mdc`)
3. Submit a pull request!

---

_Last updated: `2025-02-17`_
