# Repolex Knowledge Graph of marshmallow-code/.github

RDF knowledge graph data for [marshmallow-code/.github](https://github.com/marshmallow-code/.github), parsed by [repolex](https://repolex.ai).

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
rlex download marshmallow-code/.github
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c95e0c1a38c521a4fd3819f6156b41a52fc32ec6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c95e0c1a38c521a4fd3819f6156b41a52fc32ec6
│           └── chunk-001.nq.gz
├── blob
│   ├── 617d74754972938e5438d42fc07feb1e8676cd68.nq.gz
│   ├── 7e79ca9304254230a298355da27d9ff1ba51fc67.nq.gz
│   ├── d5509f6ad6f376ebf338d38b273728cb375950ad.nq.gz
│   └── ec52d2bf7b68189db794a92a0f7286cdba5d7cfc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c95e0c1a38c521a4fd3819f6156b41a52fc32ec6.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 11 files
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

[marshmallow-code/.github](https://github.com/marshmallow-code/.github)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
