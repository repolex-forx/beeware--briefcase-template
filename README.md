# Repolex Knowledge Graph of beeware/briefcase-template

RDF knowledge graph data for [beeware/briefcase-template](https://github.com/beeware/briefcase-template), parsed by [repolex](https://repolex.ai).

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
rlex download beeware/briefcase-template
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d82abb8833cb884eb7a7c5cf3baa7a85b4ccbe62
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d82abb8833cb884eb7a7c5cf3baa7a85b4ccbe62
│           └── chunk-001.nq.gz
├── blob
│   ├── 022f70359a9d5220bcb7369b5f7fa059fdd235b8.nq.gz
│   ├── 035ae8ddb213d4e9d05616bf52b8ad8f0a04d923.nq.gz
│   ├── 22c838af515b4b50d9f117d54a7c7c30a563fcb5.nq.gz
│   ├── 2c510bef080ef403b0bf1873e112f8a43721cae8.nq.gz
│   ├── 351d24577d85d03a02f921873f2a77cbbdb57acb.nq.gz
│   ├── 4cb16a76e9a9ba6923b6623674dab1f6dd770414.nq.gz
│   ├── 4ea990f6bc9aa1a46d8278665df5f46512aa24d5.nq.gz
│   ├── 5832c179275401e55cb64f80d851e19320d3031c.nq.gz
│   ├── 5b188ae8f767d88f19344c191a4a9286a2676ea4.nq.gz
│   ├── 6754db3be6499896d8c59a0e6715542cc03dba0a.nq.gz
│   ├── 691f282d48021c918ac1c3b1ff964f4a7eee0e7c.nq.gz
│   ├── 7611b0def065169879cc5defcf394c997acab1a6.nq.gz
│   ├── 77f26741ef662765e777bba149dd6560496d2534.nq.gz
│   ├── 7c0856615c6f9fe8e2aeb02f907b05dcbac1d21f.nq.gz
│   ├── 9f8d7406228b476253fb230126f35c8691ddefee.nq.gz
│   ├── b834affdddcf5014398ca9c16aafe3ea7f2d0422.nq.gz
│   ├── be2bd37eb31d4d31057de9baa0960ade7a7677d3.nq.gz
│   ├── c003e0287a80b42697012ff333e159fbe74f6c09.nq.gz
│   ├── c36804e317e197989ac7917c384bbb4a0f6c1c92.nq.gz
│   ├── c4d88e8173e484996f9c1fe716bd0fb7e4c8a73b.nq.gz
│   ├── d04c8470dbb6c7e141123c52514e5b45f3f92f87.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ec4f1c03a0413ed05a5b64a2545da5d7ebefa738.nq.gz
│   ├── f3acebe91511dfb407901c6800d723c86733c65c.nq.gz
│   └── f93f3027bc2b61c47c32e64f788fdc897fb45443.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d82abb8833cb884eb7a7c5cf3baa7a85b4ccbe62.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[beeware/briefcase-template](https://github.com/beeware/briefcase-template)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
