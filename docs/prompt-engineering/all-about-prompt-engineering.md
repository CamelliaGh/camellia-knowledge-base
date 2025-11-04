# 🧠 All About Prompt Engineering

Prompt engineering is the practice of designing clear, structured, and efficient inputs (or *prompts*) to guide AI models like ChatGPT, Claude, or Gemini to produce the best possible outputs. While generating content with AI might seem simple—just type and wait—the quality of the response often depends heavily on *how* you ask.

---

## ✨ Why Prompt Engineering Matters

Good prompt design:
- Ensures reliable and accurate answers.
- Helps the model stay consistent with instructions (e.g., tone, format).
- Maximizes the model's reasoning abilities.
- Reduces hallucinations or irrelevant replies.

There’s a lot more to prompting than asking questions; we can use tailored prompts, frameworks, examples, and constraints to enhance outputs.

---

## 🔧 Core Components of a Prompt

Most effective prompts include:
- **Role**: Who should the model act as? (e.g. "Act as an expert UI/UX designer…")
- **Task**: What should it do? ("Write…", "Analyze…", "Debug…")
- **Context**: Important background for accuracy.
- **Format**: Specify structure like tables, bullets, code blocks.
- **Examples**: (Optional) Few-shot examples to demonstrate ideal outputs.
- **Constraints**: Word limits, tone, etc.

---

## 🧩 Advanced Prompting Frameworks (Catalog + Examples)

Below are popular reusable **frameworks** you can copy‑paste and adapt. Each includes a one‑liner and a minimal example.

### 1) **RACE** — *Role, Action, Context, Expectation*
- **Use when:** You need a crisp, complete instruction.
- **Template:** `Role: … | Action: … | Context: … | Expectation: …`
- **Example:**  
  - Role: Senior UX writer  
  - Action: Rewrite hero copy for parenting app  
  - Context: Audience = busy moms, tone = warm, 8–10 words max headline  
  - Expectation: Headline + subheadline + 3 bullets + CTA

### 2) **CARE** — *Context, Action, Result, Example*
- **Use when:** You want to anchor with an example.
- **Template:** Provide brief context → request action → define desired result → include 1 example.
- **Example:** Context: Library shelf‑reading explainer. Action: Write a parent‑friendly blurb. Result: ~90 words. Example: *“Think tidy shelves = faster finds.”*

### 3) **RTF** — *Role, Task, Format*
- **Use when:** You need speed and consistency.
- **Template:** Role = … | Task = … | Format = …
- **Example:** Role: Data analyst | Task: Summarize survey insights | Format: 5 bullets + 1 chart idea

### 4) **CRISP** — *Constraints, Role, Input, Steps, Product*
- **Use when:** You want explicit constraints and a step plan.
- **Template:** State constraints → assign role → give input → ask for step plan → define final product.
- **Example:** Constraints: ≤150 words, no jargon. Role: Career coach. Input: Candidate profile. Steps: Diagnose → Advise → Plan. Product: 30‑day plan.

### 5) **FABRIC** — *Facts, Ask, Boundaries, Results, Illustration, Checklist*
- **Use when:** You must avoid hallucinations and ensure sources.
- **Example:** Facts: (paste data). Ask: Draft press note. Boundaries: Only use provided facts. Results: 120–150 words. Illustration: 1 headline. Checklist: factual/concise/citable.

### 6) **ROSES** — *Role, Objective, Steps, Examples, Style*
- **Use when:** You need tone‑controlled outputs with sample patterns.
- **Example:** Role: PM. Objective: Draft RICE backlog. Steps: Identify → Score → Rank. Examples: (2 rows). Style: concise, table.

### 7) **TAG** — *Task, Action, Goal*
- **Use when:** You want a single‑sentence brief.
- **Example:** Task: Summarize a 10‑page PDF. Action: Extract key decisions. Goal: 7 bullets for execs.

### 8) **IDEA** — *Intent, Data, Examples, Ask*
- **Use when:** You’re doing retrieval/RAG.
- **Example:** Intent: Compare 3 courses. Data: pasted syllabi. Examples: preferred output sample. Ask: 6‑row table + recommendation.

> **Tip:** Start with RTF for quick tasks. Use RACE/CRISP/FABRIC when accuracy, constraints, or auditability matter.

---

## 🔵 Reasoning & Tool‑Use Techniques

- **Chain‑of‑Thought (CoT):** “Think step by step.” Great for math/logic/planning.
- **Self‑Ask / Step‑back:** Ask the model to list questions it needs to answer before the final output.
- **Tree‑of‑Thought (ToT):** Explore multiple solution paths → select best.
- **ReAct:** Alternate *reasoning* and *actions* (e.g., tool calls) in agent workflows.
- **RAG (Retrieval‑Augmented Generation):** Inject external docs/snippets to ground answers.

**Mini‑prompt:**  
“Before answering, list the 3 most uncertain assumptions and how you’ll validate each.”

---

## 🧭 Best Practices

1. Be clear & concise.  
2. Use delimiters to separate instruction sections.  
3. Define constraints explicitly—tone, format, length, exclusions.  
4. Iterate & revise; keep a prompt log.  
5. Test across different models (e.g. GPT‑4 vs Claude) for consistency.  
6. Mind the context window; include only relevant material.  
7. Ask for sources or set ‘facts‑only’ rules when accuracy matters.

---

## ✅ Prompt Engineering Checklist

- [ ] Defined objective of your prompt?  
- [ ] Included role and background context?  
- [ ] Specified format and constraints?  
- [ ] Added examples if useful?  
- [ ] Asked for reasoning if needed?  
- [ ] Verified token length?

---

## 💡 Example Prompt (Combining Frameworks)

```
RACE+CoT
Role: Senior Technical PM
Action: Create a prioritized feature backlog for a “Wix Events Importer” MVP.
Context: One developer, one QA, 4-week sprint, 1,000-event import, Wix Velo + REST only.
Expectation: Output a Markdown table (Feature, RICE, Reason, Effort, Dependencies). Think step by step.
```

---

## 📚 Further Resources

- Anthropic: Prompting & best practices
- OpenAI: Prompting guidelines & structured outputs
- PromptingGuide.ai: Technique catalog
- “Material for MkDocs” (for publishing docs sites)

---

## 🧱 Anti‑Patterns (What to Avoid)

- Over‑stuffed prompts without structure.  
- Vague requests (“make it better”) without criteria.  
- Asking for everything at once; split into steps.  
- Relying on unstated facts; paste the source data.  
- No format constraints → messy outputs.

---

## 🧪 Quick Reference — Copy‑Paste Starters

**RTF (starter):**  
`Role: … | Task: … | Format: …`

**RACE (audit‑friendly):**  
```
Role: …
Action: …
Context: …
Expectation: …
```

**CRISP (strict):**  
```
Constraints: …
Role: …
Input: …
Steps: …
Product: …
```

**FABRIC (fact‑safe):**  
```
Facts: …
Ask: …
Boundaries: (no external info, cite all)
Results: (length/format)
Illustration: (headline/table/example)
Checklist: (accuracy, tone, structure)
```

---

## 🏁 Summary

Prompt engineering is a toolbox: **frameworks** (RACE/RTF/CRISP/FABRIC…), **reasoning techniques** (CoT/ToT/ReAct), and **sound practices** (constraints, examples, iteration). Use simple frameworks for speed, and stricter ones when accuracy and reproducibility matter.
