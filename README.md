# Repolex Knowledge Graph of pydata/parallel-tutorial

RDF knowledge graph data for [pydata/parallel-tutorial](https://github.com/pydata/parallel-tutorial), parsed by [repolex](https://repolex.ai).

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
rlex download pydata/parallel-tutorial
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0e7f564deba35343d25f893f3a79343442c11f4b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0e7f564deba35343d25f893f3a79343442c11f4b
│           └── chunk-001.nq.gz
├── blob
│   ├── 02c52ba7871db7df7d9a5bc348e4350ca1bafc99.nq.gz
│   ├── 06e89d614ec18e0d57da6c79efb5f6cc845fff8c.nq.gz
│   ├── 09069fea2749dab1f69acc3829dde971a37eced5.nq.gz
│   ├── 0e23f10acfc769996aef0ab7d51a8d4076633649.nq.gz
│   ├── 175e9414236a5aba97a3b556e1288f71433ef744.nq.gz
│   ├── 1db27659ce07d14002608ebdb8693728a9db1aef.nq.gz
│   ├── 34d6dd3082fa8b43685da82cc6233ea5444a4875.nq.gz
│   ├── 3e0313319893ca372a8b279d6e2d6872036eb28b.nq.gz
│   ├── 416645b50edb70c4b84d376c129d8bc9a5fc0cfd.nq.gz
│   ├── 45ed4ab44036fc1f2ab9bff5de16b53cada96115.nq.gz
│   ├── 464c718c0599563d7d9a6d5b17ed3c00718519cb.nq.gz
│   ├── 488bfe4f61530c07dbdb09d90942398ca8e87d9b.nq.gz
│   ├── 5277fb24c4deacd891569f3260bb13444336c762.nq.gz
│   ├── 58e83280679d8b91d82eca1791ab1229cc132f98.nq.gz
│   ├── 5f300f948e7c529d911bdbf66bccf2ed0e5c7b5e.nq.gz
│   ├── 62d5db0b036972dbedb1975268faf2ead6b2834f.nq.gz
│   ├── 80f27716f0c5022e6c35b04e8bc7cb9c02b93d6c.nq.gz
│   ├── 8314fa1ebc44f9dfaf378cc5d287aab89ad318da.nq.gz
│   ├── 86192aca06460c5d7bbb6db9f8d1543b8139d073.nq.gz
│   ├── 8afb1ae1df10c4c0148dadff9b4cfd48011721a0.nq.gz
│   ├── 91faaba46243f00a81dc3d0d8250f52c34d42952.nq.gz
│   ├── a068942fb626d98851fd1d8aeba0efc013e1718c.nq.gz
│   ├── a4bb2475b98382e7c8fac3863b69c608df52f041.nq.gz
│   ├── a6bc739d20ae61e17eab86345a4058672e34f886.nq.gz
│   ├── a6e21ba5621d78a1071af74417e900b689f31cc3.nq.gz
│   ├── a8759af5e861eaf28fd399af7cf8438849b4e185.nq.gz
│   ├── b231b592e33108d8591f2080afe249c3c32b7b7c.nq.gz
│   ├── c2933e5110bcb54b7a2c54c65da5f84982193374.nq.gz
│   ├── d28d5f1d0179902fa12c54d4fc981c9936047d5d.nq.gz
│   ├── d3d9ea064533b287b9a42429bc81a39131d80687.nq.gz
│   ├── d68dab0c6b9fbc28bdd38e5ad5a08ed3a219beb2.nq.gz
│   ├── db0c999ade222db7a848b58a451725d9d6b8a30f.nq.gz
│   └── fc3a426bf6bac228ad866cb2f7298f83caa37c84.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0e7f564deba35343d25f893f3a79343442c11f4b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
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

[pydata/parallel-tutorial](https://github.com/pydata/parallel-tutorial)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
