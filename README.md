# Repolex Knowledge Graph of zopefoundation/zope.globalrequest

RDF knowledge graph data for [zopefoundation/zope.globalrequest](https://github.com/zopefoundation/zope.globalrequest), parsed by [repolex](https://repolex.ai).

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
rlex download zopefoundation/zope.globalrequest
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 200ba7e70df3a9188cdfa2c0b81758216a4ac572
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 200ba7e70df3a9188cdfa2c0b81758216a4ac572
│           └── chunk-001.nq.gz
├── blob
│   ├── 0376d86f322240930573ed041fd49ef618fd8c7a.nq.gz
│   ├── 064a6fe195889fa90a73621206818352aaa69608.nq.gz
│   ├── 0ab12fe1e0c8eb6cb0d68fce1b14a2209cdb0def.nq.gz
│   ├── 1f321f52abb7db6f79c285bab56e2852dc575699.nq.gz
│   ├── 32c47f079c81a579948a4952d1f5ee67126930c2.nq.gz
│   ├── 3a3a5cacd93abc8e9e35e5a2af597c174078a92c.nq.gz
│   ├── 3abf0579e33d4124f728ddd491748787c5ee85bd.nq.gz
│   ├── 564853291998f83dc57aa414210e8919209b46fd.nq.gz
│   ├── 646493af70be34a003f7f80b06627ce23c599ac6.nq.gz
│   ├── 692c41bb1e558152bd3401624d650e95037c35b3.nq.gz
│   ├── 69d0906b13593a1d1ddc9c6638323cb3e323b1a0.nq.gz
│   ├── 6a07bb917814fcce3451ed1dc8d6ee856c18760a.nq.gz
│   ├── 7205453e03568233471f7308b48cb388a9e2c6f6.nq.gz
│   ├── 98cbe6564c87309dfb909df6debc1bcb3c09068d.nq.gz
│   ├── a946ecfe2ef8e79a91f23b849a01515e4b3bfd76.nq.gz
│   ├── a96fb1a798171f0df614dded5a933a841c85e32c.nq.gz
│   ├── b828f41877e58b12d9f21109fa7506dd32bdb387.nq.gz
│   ├── bcc7020fbb5627846d364ba3eeff53bbef95d48d.nq.gz
│   ├── c5508b9f083362a81185d598327e7801d837cb18.nq.gz
│   ├── ccdedc28073a0ba8303c52c91284a4e7e70bb471.nq.gz
│   └── f0ed9d001e553f388470f3a0b5eca7e9269311c7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 200ba7e70df3a9188cdfa2c0b81758216a4ac572.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 29 files
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

[zopefoundation/zope.globalrequest](https://github.com/zopefoundation/zope.globalrequest)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
