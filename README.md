# Repolex Knowledge Graph of florimondmanca/aiometer

RDF knowledge graph data for [florimondmanca/aiometer](https://github.com/florimondmanca/aiometer), parsed by [repolex](https://repolex.ai).

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
rlex download florimondmanca/aiometer
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 73db261bccb60aceff48677ea9b72a44110c4c11
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 73db261bccb60aceff48677ea9b72a44110c4c11
│           └── chunk-001.nq.gz
├── blob
│   ├── 09301e40be6db26c5e073ad67b38466afe8248d3.nq.gz
│   ├── 09b8f65f82fcc9977aebb5ec4469c76726fcdcd6.nq.gz
│   ├── 0aaa2f1509ab4657b8f638a77cb63c6e1f23e786.nq.gz
│   ├── 18818fd2c628c64460e40adcceb2067cafdbca7e.nq.gz
│   ├── 2fe2ac2e2db2dceb05a5db9fc7ffc8f70cbc2c76.nq.gz
│   ├── 3fb8d7a6d70ef37582e99f06afe60803cb83d7ac.nq.gz
│   ├── 405f33e98e0e5cfd13d7acd8a88dd467687779a5.nq.gz
│   ├── 41ed33bf71f7e1ec48d44cb40ed3919a9fd70947.nq.gz
│   ├── 422af5259a056d8b3460460d7bdea438e29dad87.nq.gz
│   ├── 5518f7f2159b2715263a19c6e533505bf8d59ec0.nq.gz
│   ├── 5580482f3fefe5620609489b3e1682dddde5cdbc.nq.gz
│   ├── 630b754d283373e71cd11e4e7a9d12fd8247b412.nq.gz
│   ├── 6ec15eb55b295584a2640d20766cc10da0fab3ed.nq.gz
│   ├── 707275f0fe486c8b9fbe3575fa1e4a62288b7a18.nq.gz
│   ├── 709e41b9823ba816714b6ce455cf527e4b1fdfc8.nq.gz
│   ├── 75506988293cbdc21ac13f864cf78695947b6040.nq.gz
│   ├── 8474f89cf80d6758ec144126215cae827def0b39.nq.gz
│   ├── af861a4d76f9475c8fab6fed88c77638e81da871.nq.gz
│   ├── b678428b265dc639f2ed9f57ef38b8bd5600fde0.nq.gz
│   ├── d93c67ca5266d5c79bd79b05b0514532c22ea955.nq.gz
│   ├── da6ae9dbdbde92e854dd9e23f944607ca094ecf6.nq.gz
│   ├── db2cd0c97a3bdf566ab82a4335a6ff030fe9d839.nq.gz
│   ├── e397b3afc9632b52e078463b69cbcbb250f862ad.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eb94e43e790da99f07dc0ee06a5acf99af9dcc0d.nq.gz
│   └── fa9b28487919960423042e75a71ce310fd4d5549.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 73db261bccb60aceff48677ea9b72a44110c4c11.nq.gz
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

[florimondmanca/aiometer](https://github.com/florimondmanca/aiometer)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
