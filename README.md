# Repolex Knowledge Graph of agronholm/aiohttp-apispec

RDF knowledge graph data for [agronholm/aiohttp-apispec](https://github.com/agronholm/aiohttp-apispec), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/aiohttp-apispec
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9a53408740780e9758b186742bb8898df2a25646
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9a53408740780e9758b186742bb8898df2a25646
│           └── chunk-001.nq.gz
├── blob
│   ├── 255dd067acbe7e4a2a772a6cf2e8c4aca362d49f.nq.gz
│   ├── 29e1cc402d5fc7e7836bb14cef474c7b345ee78c.nq.gz
│   ├── 4aa289c2ec8ca46ff8ddee87af8706c3e40d8dbb.nq.gz
│   ├── 517d0df1bafc14c25306133e62ede3254fea44f9.nq.gz
│   ├── 562c640dbecb4804197f5d4e814fdb09f32d2dca.nq.gz
│   ├── 63db27958d2dc46c002f6268f28e25c7ff20e3ff.nq.gz
│   ├── 74673eba18af0aa2b239d8e23c62513e2f330f9d.nq.gz
│   ├── 792dba2ca958c701357b92c04ba647fe3d7821d7.nq.gz
│   ├── 7c96277faf7679fbb00712a2f5433317c0b130f2.nq.gz
│   ├── 8e8524e93c5e696c258384465c0564788a371067.nq.gz
│   ├── 91bbd7cc325301889886fbeb5aa3f0c3ca1e18e0.nq.gz
│   ├── 95e5992ae8a148f2a3ec1a317620d5e4b91875a1.nq.gz
│   ├── a7543a349e2a91851e8c5de8792a9343370669c6.nq.gz
│   ├── a8b46164ab9ee6eef54cdacfe43b0d21aa5cbe0a.nq.gz
│   ├── aa42f797715d2e71f626208aaa477d7d71ce24d4.nq.gz
│   ├── bb2a7f4c4fa9e3db5f4a73a4f7157783f1450f62.nq.gz
│   ├── bd7ae23bccb557d442ab6d0d00e9919f68ed67d2.nq.gz
│   ├── e1373e891c6ca030ce131a95b8f2db90ec9f5779.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e757cb87f2a80e8f2cea970011f9192bcb8afc49.nq.gz
│   ├── e964255e96a27b8d529070beeb5031eea9d6e6e5.nq.gz
│   └── fbdb3fae226004d01eed8bd3ad40e75797e93798.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9a53408740780e9758b186742bb8898df2a25646.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 28 files
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

[agronholm/aiohttp-apispec](https://github.com/agronholm/aiohttp-apispec)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
