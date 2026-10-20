# Repolex Knowledge Graph of jaraco/jaraco.crypto

RDF knowledge graph data for [jaraco/jaraco.crypto](https://github.com/jaraco/jaraco.crypto), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/jaraco.crypto
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0b2e3fde123b2a5f4933d9f6d65c8af9b176f657
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0b2e3fde123b2a5f4933d9f6d65c8af9b176f657
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c6369130e47f84304352693a06adc4a428086ee.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 2e3f4dd791a6372b427d618eb0baa8c4dc58e5f0.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 5c05f9e27d57a4b7a3c3a9fdfecf8cddb8be499f.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 789506c387ba9e5c2932849f33d33f7b63c98baf.nq.gz
│   ├── 8c1f39880810c90809d6133ba6a9a0b76db927e0.nq.gz
│   ├── 913b2a2482454c27b538e9f4ebe2fc4e3b95defb.nq.gz
│   ├── 97966586fe2bc79f468ac9bf972c6350b8c0faed.nq.gz
│   ├── 9ad34ea16b5ed4155be5b64502bc12fc4e3d499d.nq.gz
│   ├── b3a106c788b85417c2d393d118cbe3b328dcc39c.nq.gz
│   ├── c09ea24876931bce0eb52294be0b58a7e14ec439.nq.gz
│   ├── c2996736278d8581208710230f7fd8f07bcc4d81.nq.gz
│   ├── c7d4dcc196eb158a624b8a0897390d56ab81d433.nq.gz
│   ├── cb09af2ac7c07c89b6e8b7142e6388a65e4edea1.nq.gz
│   ├── cc297998c6f2678befb49f3b92fa265a63b7e4a7.nq.gz
│   ├── cfb0768d48e6de1abd396125ea9c237404c5f244.nq.gz
│   ├── d8bec19d6b751bac9cb4239b9184e708b6fee506.nq.gz
│   ├── df46b5d886e03e37471a5266ccc04aaf66f78f60.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ed16a82aca3ce8209eaa5bb74a9a28e959a83d8f.nq.gz
│   ├── efcb8cbc2043faa7caf4f92fc7488bd6914c934c.nq.gz
│   └── f8c4f73dce6bf205631b701ed09eabf28fda64c7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0b2e3fde123b2a5f4933d9f6d65c8af9b176f657.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 38 files
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

[jaraco/jaraco.crypto](https://github.com/jaraco/jaraco.crypto)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
