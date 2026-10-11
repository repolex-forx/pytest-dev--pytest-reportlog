# Repolex Knowledge Graph of pytest-dev/pytest-reportlog

RDF knowledge graph data for [pytest-dev/pytest-reportlog](https://github.com/pytest-dev/pytest-reportlog), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-reportlog
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cd0788f2c81d8f235ce4b2be2df8afa844a2bcf8
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── cd0788f2c81d8f235ce4b2be2df8afa844a2bcf8
│           └── chunk-001.nq.gz
├── blob
│   ├── 032df8b12e6ae4546372c1991280a8c6d87aca5f.nq.gz
│   ├── 06c03be323491281e4d368c0eca8e11cfb91a5bb.nq.gz
│   ├── 1fa5dcf53f98a4c1bfdf93c2c007527ecc2e567b.nq.gz
│   ├── 4962913eb3a9096f9a6132369348e5cdaf111a74.nq.gz
│   ├── 549f0d323fa2c46f1b822b564e7184b964824686.nq.gz
│   ├── 576b44eb0cdf4b4a5b4294b6a919df10ca630d74.nq.gz
│   ├── 89de80ed51a2dd6a855d603a6fa09ddcd133d615.nq.gz
│   ├── b58ae04cd55066806768f6e1452215facadec0b2.nq.gz
│   ├── b94fa5c431bb4d6b6304a943700d19144bf17001.nq.gz
│   ├── be006de9a1ae3b9628e796c74277cd6d61e0a34a.nq.gz
│   ├── c1067e6140ee5b9a326453748e6262c6738aab93.nq.gz
│   ├── c1d5c03c2d42885453aaeb9dd8dcb227de76d927.nq.gz
│   ├── d44d56f1050d6069cfae85b6d1d3ef481d3b081b.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── cd0788f2c81d8f235ce4b2be2df8afa844a2bcf8.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 22 files
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

[pytest-dev/pytest-reportlog](https://github.com/pytest-dev/pytest-reportlog)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
