# Multi-Model Agent Evaluation Matrix

Use this sheet to fill placeholders in `placeholders.tex` and result tables.

## Model Backends
- Closed: gpt-5.1-codex, claude-sonnet-4-5, o3, gpt-4.1
- Open: DeepSeek-V3.1, Llama-3.3-70B-Instruct

## Fixed Agent Policy
- Prompt policy version: v1-copilot-agent-fixed
- Tool set: search, edit, run, test, diagnostics
- Retry budget: 3 attempts per task
- Action budget: 30 tool calls per task

## Primary Metrics (per model)
| Model | Easy SR | Medium SR | Hard SR | Overall SR | Quality Score | Safety Violations | Avg Latency | Avg Cost |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| gpt-5.1-codex |  |  |  |  |  |  |  |  |
| claude-sonnet-4-5 |  |  |  |  |  |  |  |  |
| o3 |  |  |  |  |  |  |  |  |
| gpt-4.1 |  |  |  |  |  |  |  |  |
| DeepSeek-V3.1 |  |  |  |  |  |  |  |  |
| Llama-3.3-70B-Instruct |  |  |  |  |  |  |  |  |

## Slice Analysis
| Slice | % of dataset | Best model | SR | Notes |
|---|---:|---|---:|---|
| Large repositories |  |  |  |  |
| External-doc dependent tasks |  |  |  |  |
| Bug-fix tasks |  |  |  |  |
| Feature implementation tasks |  |  |  |  |
| Refactoring tasks |  |  |  |  |

## Error Taxonomy
| Error Category | Frequency | Representative case |
|---|---:|---|
| Repository grounding failure |  |  |
| Planning/decomposition failure |  |  |
| Test-repair loop failure |  |  |
| Unsafe/invalid tool usage |  |  |
| API hallucination |  |  |
