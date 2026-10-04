# Ledger Status

**Project:** `K_GRAPHRAG`  
**Tier:** TIER_4_INFERENCE_AGENTS  
**Identity:** Upstream `microsoft/graphrag` @ `769542fbf1d8` (MIT)

## Chain state

| Fact | Value |
| --- | --- |
| Upstream | `microsoft/graphrag` |
| Commit | `769542fbf1d8e5b4c6a8677fefc34621c87894c5` |
| Upstream licence | MIT |
| Licence class | permissive |
| Clone size | 16.89 MB |
| Ledger | 0 blocks, chain verified |
| Current TRL | NOT YET MEASURED |
| Post-optimisation TRL | NOT YET MEASURED |
| II budget cap | 1000.0 IIU |
| Verified upstream edits | 1 |

- Blocks: **0**
- Head digest: `None`
- Chain verification: **verified**

## Independent verification

The chain is verifiable without trusting this project's tooling:

```
anticloud ledger verify
anticloud ledger export > ledger.jsonl
```

Each block carries the previous block's digest, so removing or reordering an
entry invalidates every block after it. That property is the reason the
ledger can stand in for a claim of what happened.
