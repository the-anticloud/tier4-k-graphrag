# How to Operate — K_GRAPHRAG
**Platform:** Anticloud | **IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg

## Module Overview
K_GRAPHRAG — GraphRAG: graph-enhanced retrieval-augmented generation for Anticloud knowledge queries
Stack: Python 3.11, networkx 3.2+, FAISS, sentence-transformers, PAX 27B, K_GRAPHIFY, AIOSS_FORMAT

## Daily Operations
1. `aioss verify --chain ./k_graphrag.aioss`
2. Check service health via api-oss-monitor
3. Review api-oss-logging for error-level events
4. Confirm PAX 27B is loaded and responding

## Incident Response
- Chain tamper: halt, notify compliance, restore from backup
- GPU OOM: reduce batch size, check memory leak
- High latency >2s P99: check queue depth, scale workers
- Compliance gap: run api-oss-compliance report

## Backup (nightly)
```bash
python -m api_oss_backup backup --sources ./k_graphrag.aioss --output ./backups/
```
