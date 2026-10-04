# Deploy Guide — K_GRAPHRAG
**Tier:** TIER_4_INFERENCE_AGENTS | **Stack:** Python 3.11, networkx 3.2+, FAISS, sentence-transformers, PAX 27B, K_GRAPHIFY, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, networkx 3.2+, FAISS-cpu 1.7+, sentence-transformers, PAX 27B, K_GRAPHIFY graph (must exist).

## Environment
16GB RAM. GPU for PAX synthesis. KAMELOT_SEARCH index and K_GRAPHIFY graph must be pre-built.

## AIOSS Integration
```bash
aioss init --module K_GRAPHRAG --output ./k_graphrag.aioss
aioss append --chain ./k_graphrag.aioss --payload ./output.bin --module K_GRAPHRAG
aioss verify --chain ./k_graphrag.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_GRAPHRAG",
    aioss_chain="./K_GRAPHRAG.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_GRAPHRAG.aioss --verbose
python -m K_GRAPHRAG.tests.smoke
```
