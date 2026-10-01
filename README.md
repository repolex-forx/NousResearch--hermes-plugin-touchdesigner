# Repolex Knowledge Graph of NousResearch/hermes-plugin-touchdesigner

RDF knowledge graph data for [NousResearch/hermes-plugin-touchdesigner](https://github.com/NousResearch/hermes-plugin-touchdesigner), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download NousResearch/hermes-plugin-touchdesigner
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 88a7a7884e5eda33cfe4b1dd5e69df7cb15d5898
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 88a7a7884e5eda33cfe4b1dd5e69df7cb15d5898.nq.gz
│   └── repolex
│       └── 88a7a7884e5eda33cfe4b1dd5e69df7cb15d5898
│           └── chunk-001.nq.gz
├── blob
│   ├── 048e49554552ee7a531ac4e95a253622b9ced1bf.nq.gz
│   ├── 0e030204d55f8b2b23fe6f2023cb869a4d0641bb.nq.gz
│   ├── 0e0f077cf86df663a1edc86e8e6d7144d8b7e4b4.nq.gz
│   ├── 23cbbd850a349fe87f12a07c26ff6b227b81cddc.nq.gz
│   ├── 2ce55dd5e8658df5991156f1eb13c4ba6fabc7ad.nq.gz
│   ├── 4bd9302327b209524ce28deb9e9c6f93b35142d8.nq.gz
│   ├── 5b9cd3da3d97559e4de5d8ceeb3dcada3d5d77d4.nq.gz
│   ├── 6aa716cb9a21e25d7c8cd5c7925dd471cbdc9ccf.nq.gz
│   ├── 6ff7b08f7552c14d7eb6df72b92df7558c043d62.nq.gz
│   ├── 74e756ccb24ddee46d0d0f73573ed766205c6f98.nq.gz
│   ├── 75410e73319c72cd3e991a501c5455eb78f38375.nq.gz
│   ├── 7d1e322a4ea52fd038fd36a4127ede05de4d974d.nq.gz
│   ├── 97c2dea80bd361522076ff3952aec5b242520b58.nq.gz
│   ├── 9b2fb5863f53815c3e7c5b9b7a9c5e7f46612509.nq.gz
│   ├── a5bfdffeb718e2e5a170283c33d40045796dec7f.nq.gz
│   ├── b9498f1fe55d881c0ad512c3b3ad6d571f1de2c6.nq.gz
│   ├── bec68e33cf902b3de41a1ce225026d7ddf661b71.nq.gz
│   ├── ca994352129ed9018fbb27689ba40e0a82b7aaed.nq.gz
│   ├── cb04fd54d57356d540c91460006b6ecf09bcff4b.nq.gz
│   ├── d4b165e7499cacf9192600371d84871350d78129.nq.gz
│   ├── e18b27749039383bd233220890be1e60bc38619f.nq.gz
│   ├── e5837de6a38397afe3e8523fb533e13b4bb997ed.nq.gz
│   ├── ec90076cb2bbe4f210359cacd69e912b3b331635.nq.gz
│   ├── f2955110b0ef4cd9b7ea0f7ecaee3c3f6c7eb29a.nq.gz
│   ├── f37a84891541579965907aed31602f41e61402d9.nq.gz
│   ├── fd5257e1e843355c1cfa1cf81785275073c2eacc.nq.gz
│   └── ff54a3fb02afcd5773f91da10d421579de389f62.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 88a7a7884e5eda33cfe4b1dd5e69df7cb15d5898.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 34 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[NousResearch/hermes-plugin-touchdesigner](https://github.com/NousResearch/hermes-plugin-touchdesigner)

---
*Parsed on 2026-10-01 by [repolex](https://repolex.ai)*
