# Repolex Knowledge Graph of jupyterhub/autodoc-traits

RDF knowledge graph data for [jupyterhub/autodoc-traits](https://github.com/jupyterhub/autodoc-traits), parsed by [repolex](https://repolex.ai).

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
rlex download jupyterhub/autodoc-traits
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 339425f57a35c47a1435b0b3330749f3f1d7f1b8
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 339425f57a35c47a1435b0b3330749f3f1d7f1b8
│           └── chunk-001.nq.gz
├── blob
│   ├── 063d6f5d64eff36738beab349c3d3a62199c630a.nq.gz
│   ├── 0f43843ed27455a061be31fcda8542fbd16fef09.nq.gz
│   ├── 1010cca555b341b90f5cdb61e59463950ab5b614.nq.gz
│   ├── 1172187b7a43cfa15c6637f53254c210f065cd2e.nq.gz
│   ├── 166af91e07437f80b5e5a45183d0d9cf807349f8.nq.gz
│   ├── 2205c5d2efe66fb3b99846623163208b7937e62e.nq.gz
│   ├── 2e6378a5e5adeae13f974adcd801c42d459f6dc7.nq.gz
│   ├── 2ea3205d7102d36cf68baa077c95a86170d8086c.nq.gz
│   ├── 4ce6d985c55f5f04f5a3c3ae825edb5eb7ce4382.nq.gz
│   ├── 5381a8d4ce711078345986f9e7b0373262f436dd.nq.gz
│   ├── 5cee7b57a630b6c370cd9b071af5cb1b5cdcbd28.nq.gz
│   ├── 73fb3ef0a25f322f415559b448575bf9ecf47382.nq.gz
│   ├── 8147f9a175309929105cdd065e982db149ee1149.nq.gz
│   ├── 8181b99aa1204af11523f60a10cbec99f6f3c257.nq.gz
│   ├── 833fe61e63989eea42f2ed1c536b9021a48a792b.nq.gz
│   ├── 875f81d367e1cadbc8fc5e97dd57593923797072.nq.gz
│   ├── 8afbc9b624e20389bbf19ec80ea67729e18693a5.nq.gz
│   ├── 94dbd57b34ac8fa4b7ddb89d9c21380e968024c7.nq.gz
│   ├── 966e3320bb6ed30dfe9149c773f31fcebbeb17f0.nq.gz
│   ├── 9a338fd9c8411610facf2501ef146a1125a817d3.nq.gz
│   ├── 9b126b40c9fd7eafcad62dd3fd8389f3c57c6d44.nq.gz
│   ├── ad12fed27473110d262d075d66b21dcbbf1d339b.nq.gz
│   ├── b5ac43111be085001c107d98f580290089fedd54.nq.gz
│   ├── bace0a79c9142cd3b52ef4c4c4e9b05dab5bafd6.nq.gz
│   ├── bcbd17a0d9aa7fad623fe3d01297a9c24a6e8488.nq.gz
│   ├── c37ddfc0590bcae6c49008f05601fae2178027b9.nq.gz
│   ├── c43d2999a9b6170809e80926da0f51af6fa10d7e.nq.gz
│   ├── c7c933f1dcd6d9e9c70fa03e21b7b4ad412cceb4.nq.gz
│   ├── d1acb0610183bc7158cc4423fbbcef44283af3a3.nq.gz
│   ├── d550b0edd487a02c3fb796c34a87d066fe414a93.nq.gz
│   ├── d908fe93ac5b6769d698481cd7dd247b63fb52e8.nq.gz
│   ├── daf1618c33e7e2bb54a1d293da2918dadeb584f2.nq.gz
│   └── f8a91496e16e2eef4492b6e3fbc016721bcebd2c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 339425f57a35c47a1435b0b3330749f3f1d7f1b8.nq.gz
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

[jupyterhub/autodoc-traits](https://github.com/jupyterhub/autodoc-traits)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
