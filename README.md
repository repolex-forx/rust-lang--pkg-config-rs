# Repolex Knowledge Graph of rust-lang/pkg-config-rs

RDF knowledge graph data for [rust-lang/pkg-config-rs](https://github.com/rust-lang/pkg-config-rs), parsed by [repolex](https://repolex.ai).

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
rlex download rust-lang/pkg-config-rs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a8852cc148f8f7d504bf3a62444c298dcd3637f0
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── a8852cc148f8f7d504bf3a62444c298dcd3637f0.nq.gz
│   └── repolex
│       └── a8852cc148f8f7d504bf3a62444c298dcd3637f0
│           └── chunk-001.nq.gz
├── blob
│   ├── 16fe87b06e802f094b3fbb0894b137bca2b16ef1.nq.gz
│   ├── 28db4390834921668a40eba93316c410b58d770d.nq.gz
│   ├── 39e0ed6602151f235148e6c08413aa7eda5b9038.nq.gz
│   ├── 45a16068da54832f9638fae701db467fc7ba9b55.nq.gz
│   ├── 567c37c28e95a1a30f602460da17e95dd212493f.nq.gz
│   ├── 5c96ba95dfec84950afee738d78a53b003b9a310.nq.gz
│   ├── 701c4bf73f1ee0fae32709ed75aebc9c7f90237a.nq.gz
│   ├── 7c36c5cb71a8908ce276871b383e296efccf80f9.nq.gz
│   ├── afe3d392d8553ecf28d4a3033e5ac8789aeb437c.nq.gz
│   ├── b990e26893d610c4c5d4034c27a6cc9be2d79274.nq.gz
│   ├── ce63ceb558f85713adba2d481553c333ef7cd9ac.nq.gz
│   ├── d6904d26d07f290d2b0f78f5a46a76ccf5c0ba19.nq.gz
│   └── fec17f47a646b2cfaad2e5d1bafb95f998b82ab6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a8852cc148f8f7d504bf3a62444c298dcd3637f0.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 22 files
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

[rust-lang/pkg-config-rs](https://github.com/rust-lang/pkg-config-rs)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
