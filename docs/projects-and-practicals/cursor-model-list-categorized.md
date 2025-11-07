# Cursor Model List (Categorized by Usage) – Updated Nov 2025

> This file categorizes Cursor-supported AI models by their **best usage area** to help you quickly pick the right model for the task.  
> Source: https://cursor.com/docs/models

---

## 🧠 1. Planning, Architecture, and Multi-Step Reasoning
| Model Name | Provider | Context | Notes |
|---|---|---|---|
| **Claude 4 Opus** | Anthropic | ~200k | Deep system-level reasoning, tool-enabled agent |
| **Claude 4 Sonnet** | Anthropic | 120k–200k | High-context, reliable for architecture + multi-step tasks |
| **GPT-4.1 / o3** | OpenAI | 128k–200k | Balanced explanation + code; strong “thinking” variants |
| **DeepSeek R1** | DeepSeek | ~60k | “Thinking” variant; strong multi-step analysis |
| **Claude 3.7 Sonnet** | Anthropic | 120k–200k | Reliable explanations and trade-off analysis |

---

## 🛠 2. Repo-Wide Refactors & Complex Bug Hunts
| Model Name | Provider | Context | Notes |
|---|---|---|---|
| **Claude 4 Sonnet / Opus** | Anthropic | 120k–200k | Handles large edits and context-aware refactors |
| **Composer 1 (Agent)** | Cursor | Large | Agent model for multi-file actions and terminal use |
| **GPT-4.1** | OpenAI | 128k–1M | Clear corrections and targeted multi-file suggestions |

---

## 🔧 3. Feature Scaffolding (Implementation + Explanation)
| Model Name | Provider | Context | Notes |
|---|---|---|---|
| **GPT-4.1 / GPT-4o** | OpenAI | 60k–128k | Balanced scaffolding, writing, and explanation |
| **Claude 3.7 Sonnet** | Anthropic | 120k–200k | Great for feature estimates and reviews |
| **o3 (OpenAI)** | OpenAI | 128k–200k | Good for planning complex or unfamiliar flows |

---

## ✅ 4. Unit Tests, Docstrings, and README Generation
| Model Name | Provider | Context | Notes |
|---|---|---|---|
| **Gemini 2.5 Pro** | Google | ~120k | Structured outputs, quick validation |
| **Gemini 2.5 Flash** | Google | up to 1M | Massive context for doc and test creation |
| **GPT-4o mini** | OpenAI | ~60k | Fast and affordable for small-scale tasks |
| **DeepSeek V3** | DeepSeek | ~60k | Good for mass‑generation of predictable content |

---

## 🤖 5. Agent Workflows (Run Tests, Fix, Repeat)
| Model Name | Provider | Context | Notes |
|---|---|---|---|
| **Composer 1 (Agent)** | Cursor | Large | Trained for engineering tasks with tool and terminal actions |
| **Claude 4 Sonnet/Opus (Agent Mode)** | Anthropic | 120k–200k | High-reliability file edit and test iterators |
| **GPT-4.1 (Agent Enabled)** | OpenAI | 128k–1M | Can combine code + tool call sequences |

---

## 💸 6. Low-Cost Bulk Generation (Boilerplate, Sweeps)
| Model Name | Provider | Context | Notes |
|---|---|---|---|
| **DeepSeek V3** | DeepSeek | ~60k | Great cost-performance tradeoff |
| **o1 / o1-mini** | OpenAI | ~60k | Good for JSON/YAML, configs, low-risk refactors |
| **GPT-4o mini** | OpenAI | ~60k | Small docs, templates, stubs |

---

## ⚡ 7. One-Function Edits & Quick Diffs
| Model Name | Provider | Context | Notes |
|---|---|---|---|
| **Grok 3 Beta / Mini** | xAI | ~60k–132k | Snappy, code-first short hops |
| **Cursor Small** | Cursor | ~60k | Inline diff suggestions and queries |
| **Claude 3.5 Haiku** | Anthropic | ~60k | Low cost and fast small changes |

---

## 📑 8. Very Large Context Processing (Logs, Long Docs)
| Model Name | Provider | Context | Notes |
|---|---|---|---|
| **Gemini 2.5 Flash** | Google | up to 1M | Handles huge logs, long tests, multi-file docs |
| **GPT-4.1 (Max)** | OpenAI | up to 1M | Best for long input + thinking combo |
| **Claude 4 Sonnet (Max)** | Anthropic | ~200k | Large context + deep reasoning |

---

_Last updated: 2025-11-07 • Source: Cursor Model Documentation_
