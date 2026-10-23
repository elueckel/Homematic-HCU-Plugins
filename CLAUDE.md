## graphify

This project has a knowledge graph at graphify-out/ with god nodes, community structure, and cross-file relationships (this repo's own release readmes only).

**A merged cross-repo graph for the whole Homematic plugin family** (homematic-tools, Advanced Rules, Advanced Reports, Advanced Climate, Advanced Shelly, Sigenergy, Advanced Ready, `_Homematic-HCU-Plugins` — 3735 nodes / 6609 edges / 256 communities, built 2026-09-14) lives at `/Users/enno/Documents/ClaudeCode/homematic-tools/graphify-out/graph.json`. For a question that spans plugins (e.g. "how does Rules consume Reports' external values"), query that graph instead: `graphify query "<question>" --graph "/Users/enno/Documents/ClaudeCode/homematic-tools/graphify-out/graph.json"`.

Rules:
- For codebase questions, first run `graphify query "<question>"` when graphify-out/graph.json exists. Use `graphify path "<A>" "<B>"` for relationships and `graphify explain "<concept>"` for focused concepts. These return a scoped subgraph, usually much smaller than GRAPH_REPORT.md or raw grep output.
- If graphify-out/wiki/index.md exists, use it for broad navigation instead of raw source browsing.
- Read graphify-out/GRAPH_REPORT.md only for broad architecture review or when query/path/explain do not surface enough context.
- After modifying code, run `graphify update .` to keep the graph current (AST-only, no API cost).
