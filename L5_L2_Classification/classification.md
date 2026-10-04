# L5 Narrow / L2 General Classification — K_GRAPHRAG
**Platform:** Anticloud | **Tier:** TIER_4_INFERENCE_AGENTS | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
K_GRAPHRAG combines KAMELOT_SEARCH vector retrieval with K_GRAPHIFY knowledge graph traversal for grounded, cited responses. Narrow scope: Anticloud corpus only — no web graph. Implements Microsoft GraphRAG adapted for the Anticloud domain.

## L2 General
L2 General: K_GRAPHRAG is the highest-quality retrieval backend for any tier requiring cited, multi-hop answers. Clinical staff and robotics engineers both access the same GraphRAG API with domain-appropriate citations.

## PAX 27B Integration
PAX 27B synthesizes the final response from combined vector chunks and graph-traversal nodes. Two-stage retrieval gives PAX richer grounding than vector-only RAG. Each synthesis is AIOSS-chained with full provenance.

## AIOSS Audit Chain
Every graphrag query (query hash + vector chunks hash + graph path hash + synthesis hash + citations list) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
NIST AI RMF 1.0 (grounded AI responses). ISO/IEC 42001 (transparent, cited AI outputs).
