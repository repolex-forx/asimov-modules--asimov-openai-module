# Repolex Knowledge Graph of asimov-modules/asimov-openai-module

RDF knowledge graph data for [asimov-modules/asimov-openai-module](https://github.com/asimov-modules/asimov-openai-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-openai-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5188b23070d9e6093db67fb0b50c8ccde73f1bda
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 5188b23070d9e6093db67fb0b50c8ccde73f1bda.nq.gz
│   └── repolex
│       └── 5188b23070d9e6093db67fb0b50c8ccde73f1bda
│           └── chunk-001.nq.gz
├── blob
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 126f175c1e70c1fa7cec597c290f49ba9e2214b5.nq.gz
│   ├── 5f19796c8c4b5d27dedb3ccda2ee3a57ba2a2680.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 6ef29a4ecd8c78c7a50917ebbca9aa50772a0144.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 81340c7e72d5c852585d0faea06985a720d4c2df.nq.gz
│   ├── 84f4704e85657eed35f5af25d6a8c26b3044ff07.nq.gz
│   ├── 9443c356394c0712ee92473b19668c17b381028f.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── a98ed67cfd71af5de2d9118fcedcca14da175c84.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── dc699cd7e5f96fe7da76498c5f6b99c7d26aa378.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 5188b23070d9e6093db67fb0b50c8ccde73f1bda.nq.gz
├── filetree
│   └── 5188b23070d9e6093db67fb0b50c8ccde73f1bda.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 27 files
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

[asimov-modules/asimov-openai-module](https://github.com/asimov-modules/asimov-openai-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
