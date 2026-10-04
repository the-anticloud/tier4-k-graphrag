# Developer Cookbook — K_GRAPHRAG
**Stack:** Python 3.11, networkx 3.2+, FAISS, sentence-transformers, PAX 27B, K_GRAPHIFY, AIOSS_FORMAT
**Domain:** GraphRAG: graph-enhanced retrieval-augmented generation for Anticloud knowledge queries

## GraphRAG query with citations
```python
from k_graphrag import GraphRAG

rag = GraphRAG(
    pax_model="./pax-27b-q4.gguf",
    kamelot_index="./kamelot_index/",
    graph_path="./anticloud_graph.ttl",
    aioss_chain="./graphrag.aioss"
)

result = rag.query(
    "Which TIER_7 biosignal projects are HIPAA compliant and what evidence supports this?",
    retrieval_depth=2, top_k_chunks=10
)
print(result.answer)
for cite in result.citations:
    print(f"  [{cite.type}] {cite.source}: {cite.excerpt[:60]}...")
print(f"Chain: {result.chain_hash}")
```

## Build global context summaries
```python
communities = rag.build_community_summaries(
    graph_path="./anticloud_graph.ttl",
    pax_model="./pax-27b-q4.gguf"
)
# Enables high-level queries: "What is the overall state of TIER_7?"
```

## Benchmark GraphRAG vs plain RAG
```python
comp = rag.benchmark_vs_plain_rag(
    test_queries="./anticloud_rag_bench.jsonl",
    pax_model="./pax-27b-q4.gguf"
)
print(f"GraphRAG: {comp.graphrag_accuracy:.2f} | Plain RAG: {comp.plain_rag_accuracy:.2f}")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
