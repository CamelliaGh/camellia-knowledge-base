
# 💻 Prompt Engineering in Coding Workflows

AI-powered tools such as Cursor, Github Copilot, and Claude Code are changing how developers write, review, and debug code. To get the best results, you need strong prompt engineering skills tailored for *coding tasks*.

---

## 🤖 Why Use Prompts in Coding?

- Automate boilerplate or repetitive code.
- Generate tests, docs, or architecture instantly.
- Debug or refactor code with step-by-step help.
- Speed up onboarding with codebase-aware contextual answers.

---

## 🔧 Coding Prompt Structure

When building prompts for coding assistants, include:

1. **Role** – e.g., “You are a senior full-stack developer…”
2. **Task** – “Refactor this class”, “Create tests for this method.”
3. **Context** – Existing code, file paths, architecture.
4. **Constraints** – Language, style guide, test coverage.
5. **Expected output** – Code only? With comments? In separate blocks?

---

## 🧠 Techniques for Developers

| Technique | Description |
|-----------|-------------|
| **Explain before coding** | Ask the AI to think step-by-step before outputting code. |
| **Ask for file-based changes** | Tools like Cursor let you reference specific files. |
| **Request test coverage** | Automatic generation of unit/integration tests. |
| **Walkthrough debugging** | Ask the model to hypothesize, fix, and verify. |

---

## ✅ Sample Prompt for Coding

```
Role: You are a senior TypeScript engineer.
Task: Refactor the function below to improve readability and performance. Then write Jest tests for edge cases.
Code:
```ts
function validate(data) {
  if (!data.email) return false;
  if (!data.name) return false;
  if (data.age < 18) return false;
  return true;
}
```
Constraints: ESNext syntax. No external libraries. 100% branch coverage in tests.
```

---

## 🔥 Best Use Cases for AI Code Prompts

- Feature scaffolding
- Code review
- Unit test generation
- Documentation updates
- Debug trace analysis

---

## 📎 Cursor / Claude Code Example Rule

You can add reusable templates as `.mdc` rule files inside:
```
.cursor/rules/prompt-templates.mdc
```

This ensures consistency and helps others in your team reuse effective prompts quickly.

---

## 🧩 Final Tip

Always review the AI output—AI-generated code *can* introduce bugs or style inconsistencies. Use prompts to guide structure, but stay in the loop.
