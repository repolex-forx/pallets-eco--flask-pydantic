# Repolex Knowledge Graph of pallets-eco/flask-pydantic

RDF knowledge graph data for [pallets-eco/flask-pydantic](https://github.com/pallets-eco/flask-pydantic), parsed by [repolex](https://repolex.ai).

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
rlex download pallets-eco/flask-pydantic
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── bc3fee46e680ce51bc8c32c71b3844dcd18bfd88
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── bc3fee46e680ce51bc8c32c71b3844dcd18bfd88
│           └── chunk-001.nq.gz
├── blob
│   ├── 04b385d486be73f456822b912eb7aed2f48e5af7.nq.gz
│   ├── 04c6322520d244c9467033835a4fdbd7a0579c29.nq.gz
│   ├── 052bf9b7878314f32202a559a8db08c6e0188156.nq.gz
│   ├── 0598a8d01f2519ff612f39a2b9c8b3b4a407bf33.nq.gz
│   ├── 076b6c1d9b15c48dbcdd55956fccb0338cab2ca9.nq.gz
│   ├── 124aac84e319f3d7721c2fea30ad5f6c59253a27.nq.gz
│   ├── 378eac25d311703f3f2cd456d8036da525cd0366.nq.gz
│   ├── 4cdc656c8291987ce54bcbfc11b447ba7da03103.nq.gz
│   ├── 60c92407f7869b6c76b385a440d5dc3de3907929.nq.gz
│   ├── 73b55bf95099cf9a74ffbd94e501a02806e9d4b5.nq.gz
│   ├── 743a6143f3d239696a2a7334d315e378527a985a.nq.gz
│   ├── 7c1b54f03a364989ce86d54218319589e275ce3f.nq.gz
│   ├── 83729a5bda2378db7d4c68f4de3ad41d3181b8ba.nq.gz
│   ├── 8a1cecd8db61b2f2dce9a6c118f0dfb1833bfc49.nq.gz
│   ├── 9c2f1b059d03b11c22d4ca67a532b1ddba63e621.nq.gz
│   ├── 9e78220f947c8f017375c34063d51d053a404e69.nq.gz
│   ├── b3ff80bc95f45090bab4329203ec437548e143f7.nq.gz
│   ├── b52eda4a98b8246c2ef4fb43d202339217b4ff0e.nq.gz
│   ├── c49de5f93620cc69c0031245d98a322a4fc68906.nq.gz
│   ├── c6ed3940b142754ef76a30cf7cc27f0afca321f2.nq.gz
│   ├── d0775291694d968dec0b0a4d28f03223b304047d.nq.gz
│   ├── d346a29a9683317f7de87e8f1ab93910bc10180a.nq.gz
│   ├── d421fdea7f65b204e67bd064ab65b5304ed484d9.nq.gz
│   ├── e214cc1da65b8ba859aaa3309fb74562c9cbfa0e.nq.gz
│   ├── e5b283cb264edbbf45d6489f52b1194fb960917e.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── bc3fee46e680ce51bc8c32c71b3844dcd18bfd88.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 34 files
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

[pallets-eco/flask-pydantic](https://github.com/pallets-eco/flask-pydantic)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
