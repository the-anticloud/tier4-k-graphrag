# Radon_Complexity_Lab_Results
**Project:** `K_GRAPHRAG` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `10`
- **average_complexity:** `{'grade': 'A', 'score': 2.875}`
- **complexity_grade:** `A`
- **complexity_score:** `2.875`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_GRAPHRAG\UPSTREAM\scripts\copy_build_assets.py - A (83.74)
E:`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_GRAPHRAG\UPSTREAM\scripts\copy_build_assets.py
    F 10:0 copy_build_assets - A (5)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_GRAPHRAG\UPSTREAM\scripts\update_workspace_dependency_versions.py
    F 26:0 update_workspace_dependency_versions - B (7)
    F 21:0 _get_package_paths - A (3)
    F 12:0 _get_version - A (2)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_GRAPHRAG\UPSTREAM\tests\conftest.py
    F 5:0 pytest_addoption - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_GRAPHRAG\UPSTREAM\packages\graphrag\graphrag\api\index.py
    F 29:0 build_index - A (4)
    F 98:0 _get_method - A (3)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_GRAPHRAG\UPSTREAM\packages\graphrag\graphrag\api\prompt_tune.py
    F 52:0 generate_indexing_prompts - A (4)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_GRAPHRAG\UPSTREAM\packages\graphrag\graphrag\api\query.py
    F 63:0 global_search - A (3)
    F 191:0 local_search - A (3)
    F 322:0 drift_search - A (3)
    F 454:0 basic_search - A (3)
    F 259:0 local_search_streaming - A (2)
    F 127:0 global_search_streaming - A (1)
    F 387:0 drift_search_streaming - A (1)
    F 505:0 basic_search_streaming - A (1)

16 blocks (classes, functions, methods) analyzed.
Average complexity: A (2.875)
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_