# Cursor Model List (Nov 7, 2025)

> This file summarizes models typically available in Cursor and what they’re best at. Availability, names, and context limits can vary by region/plan and change over time. Check the official page for the latest list: https://cursor.com/docs/models

## Model → Ideal Task Matrix

| Model Name | Provider | Approx. Context | Highlights | Best For |
|---|---|---|---|---|
| **Composer 1 (Agent)** | Cursor | Large | Cursor’s agent model; trained for software engineering with tool-use (file ops, terminal) | End‑to‑end agent workflows, multi‑file edits, running tests & fixing iteratively |
| **Cursor Small** | Cursor | ~60k | Lightweight, fast, inline | Autocomplete, tiny diffs, quick Q&A on code |
| **Claude 4 Sonnet** | Anthropic | 120k–200k | Strong reasoning, long context | Repo‑wide refactors, design docs, complex bug hunts |
| **Claude 4 Opus** | Anthropic | ~200k | Higher‑capacity reasoning | Architecture, system design, tricky multi‑step changes |
| **Claude 3.7 Sonnet** | Anthropic | 120k–200k | Reliable all‑rounder | Feature scaffolding + explanation, PR reviews |
| **Claude 3.5 Sonnet** | Anthropic | ~75k | Cost–quality balance | Everyday coding tasks |
| **Claude 3.5 Haiku** | Anthropic | ~60k | Lower cost, quick | Fast iterations, drafts, smaller changes |
| **GPT‑4.1** | OpenAI | 128k–1M | Strong balance of code + rationale | Feature scaffolding, integrations, API glue code |
| **GPT‑4o** | OpenAI | 60k–128k | Multimodal, responsive | Code + quick reasoning, UI/text tasks |
| **GPT‑4o mini** | OpenAI | ~60k | Lightweight | Boilerplate, utility snippets, docstrings |
| **o3 / o3‑mini** | OpenAI | 128k–200k | “Thinking” variants | Multi‑step reasoning, planning, test strategy |
| **o1 / o1‑mini** | OpenAI | ~60k | Cost‑efficient | Unit tests, small refactors, JSON/YAML configs |
| **Gemini 2.5 Pro** | Google | ~120k | Fast, structured outputs | Test generation, doc generation, medium tasks |
| **Gemini 2.5 Flash** | Google | up to ~1M | Very large context option | Long files, logs, bulk doc or test creation |
| **DeepSeek V3** | DeepSeek | ~60k | Cost‑effective | Bulk boilerplate, broad stubs, low‑cost sweeps |
| **DeepSeek R1** | DeepSeek | ~60k | “Thinking” variant | Reasoned fixes, analysis passes, explanations |
| **Grok 3 Beta** | xAI | ~60k–132k | Code‑centric, snappy | One‑function rewrites, utilities, fast edits |
| **Grok 3 Mini** | xAI | ~60k | Lightweight | Small helpers, quick diffs |

### Notes
- **Context**: The max tokens a model can consider at once (input + output). Values are approximate and may change.
- **Agent vs. non‑agent**: Agent models can plan & act (e.g., read/write files, run commands) when permitted in Cursor.
- **Pick per task**: Prefer heavier models for deep reasoning/large context; lighter models for speed/cost.

## Quick Picks by Task
- **Big refactor / repo‑wide reasoning** → Claude 4 Sonnet/Opus, GPT‑4.1, Composer 1  
- **Feature scaffolding + explanation** → GPT‑4.1, GPT‑4o, Claude 3.7 Sonnet  
- **Tests & docs quickly** → Gemini 2.5 Pro/Flash, GPT‑4o mini  
- **Low‑cost bulk generation** → DeepSeek V3  
- **Tight one‑file changes** → Grok 3 Beta / Mini, Cursor Small  
- **Agent workflows (multi‑file, run tests)** → Composer 1 (and agent‑enabled Claude/GPT variants when available)

---

_Last updated: 2025‑11‑07_
