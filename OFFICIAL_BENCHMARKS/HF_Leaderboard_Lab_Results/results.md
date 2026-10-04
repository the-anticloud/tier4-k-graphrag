# HF_Leaderboard_Lab_Results

**Project:** `K_GRAPHRAG`  
**Tier:** `TIER_4_INFERENCE_AGENTS`  
**Slug:** `microsoft/graphrag`  
**Commit:** `769542fbf1d8`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **53.31 ms** |
| Min latency | 45.52 ms |
| Max latency | 75.86 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **32** |
| Tokenization latency | 1.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5906 |
| Classification latency | 91.95 ms |
| Status | **PASS** |

**Input text tokenized:**
```
K_GRAPHRAG (microsoft/graphrag) — 910 files, 51964 source lines, licence MIT, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'k', '_', 'graph', '##rag', '(', 'microsoft', '/', 'graph', '##rag', ')', '—', '910', 'files', ',', '51', '##9', '##64', 'source', 'lines']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_