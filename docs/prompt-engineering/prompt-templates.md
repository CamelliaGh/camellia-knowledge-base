
# 📋 Reusable Prompt Templates for Developers

This file contains reusable prompt templates for use with coding AI tools like Cursor, Claude Code, and GitHub Copilot. Replace placeholders in brackets (e.g., `[LANGUAGE]`, `[FEATURE_NAME]`) before sending to the AI.

---

## 1) Feature Implementation Prompt

```
Role: You are a senior software engineer at a SaaS company, working in the [PROJECT_NAME] codebase.
Task: Implement the new feature "[FEATURE_NAME]" in [LANGUAGE]. The feature should [DESCRIPTION_OF_FUNCTIONALITY].
Context: Codebase uses [ARCHITECTURE, e.g., monorepo, CI/CD with GitHub Actions], and coding standards: [STYLE_GUIDE, e.g., ESLint, Prettier]. Tests use [TEST_FRAMEWORK]. Coverage target ≥ 80%.
Output: Provide updated/added source files + unit tests. Include comments for major changes.
Constraints: Do not modify unrelated files. Do not change public API signatures without approval. Include docstrings for public functions. File size < 200 lines.
```

---

## 2) Code Review Prompt

```
Role: You are a senior code reviewer.
Task: Review the following code and provide:
1) A brief summary of what it does.
2) Issues found (performance, security, readability, maintainability).
3) Recommended refactor actions (with example code blocks).
4) Suggested tests to cover missing edge cases.
Code:
```[PASTE CODE HERE]```
Constraints: Output with numbered sections. Do not add external dependencies.
```

---

## 3) Bug Fix Prompt

```
Role: You are a debugging specialist.
Task: Diagnose and fix the issue based on this error stack. Then write the updated code and tests to confirm the fix.
Error: "[PASTE ERROR MESSAGE]"
Context: Codebase runs on [ENVIRONMENT], using [LANGUAGE], [TECH STACK].
Steps:
1) Explain probable root cause.
2) Provide updated code (minimal changes).
3) Write regression test.
Constraints: Maintain existing code style. Avoid magic values. Do not change unrelated files.
```

---

## 4) Documentation Prompt

```
Role: You are a technical writer experienced in [LANGUAGE] codebases.
Task: Create or update the documentation for the module “[MODULE_NAME]”.
Context: Module handles [FUNCTIONALITY]. Current README is outdated.
Deliverables:
- Overview of module
- Sample usage code snippet
- Config/setup instructions
- Troubleshooting tips
- API reference (function params, return values)
Constraints: Markdown only. No more than 120 words per section.
```

---

## 🔄 Usage Tip

Store this file in your project as `prompt-templates.md` and reuse prompts for features, debug sessions, and code reviews. Or convert them into `.mdc` rule format for use in Cursor under `.cursor/rules/`.
