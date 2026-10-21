# Repolex Knowledge Graph of scrapy/scrapy-mcp-official

RDF knowledge graph data for [scrapy/scrapy-mcp-official](https://github.com/scrapy/scrapy-mcp-official), parsed by [repolex](https://repolex.ai).

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
rlex download scrapy/scrapy-mcp-official
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5530c671a7078f4f06479422c623d10b846d3db9
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5530c671a7078f4f06479422c623d10b846d3db9
│           └── chunk-001.nq.gz
├── blob
│   ├── 037539fb280518065546db32143b9c0df5ad8521.nq.gz
│   ├── 1492abd809eb5541a128e5f7ba619dacd3087466.nq.gz
│   ├── 1897ec7c01808a2c5334921b09fa23ae99724287.nq.gz
│   ├── 263c405676a2b3a2e63e49b81a85bc55df823fe1.nq.gz
│   ├── 35e22d662746394f798f2e8abd2a79be1e5174b0.nq.gz
│   ├── 3aee72cb13065249b562091c6f7ed8c47baeab89.nq.gz
│   ├── 4155a0c2c8bf150e76eeae936bbe2e75e3ee026f.nq.gz
│   ├── 4cc2a45d98dbbaa003715643fe482cd8a910a6fd.nq.gz
│   ├── 5cf2c1c9762814eaf68539ea97ac7d806c7420ff.nq.gz
│   ├── 623d48cfa6b6f2ba551dde2435254ed5a1b63862.nq.gz
│   ├── 6b2697371d666edab5941c570d3fd475f771e6e2.nq.gz
│   ├── 7a8e2117a374777d7af2c2df23521100ffa18688.nq.gz
│   ├── 8391663f08df67ddc93eec3f457bb0881e7f6612.nq.gz
│   ├── 922b59a950c5dc4638d9e19c68e6241fdc5728ab.nq.gz
│   ├── 933ae0db35e2674f95f9e0f80d3537984bfd2268.nq.gz
│   ├── 9445341fc901d0c97eb43a505cd119d49cb9e8ff.nq.gz
│   ├── a10566a1a2590f381f8589fedb4623dacf81ba11.nq.gz
│   ├── a52e3fbab7896d0fe5ea57b91b841faba6cdc214.nq.gz
│   ├── a7510d0c23646f93368bee5edcc0e5e30e34d992.nq.gz
│   ├── b5433e5621a1550460318525fd2825e64fd7ae53.nq.gz
│   ├── c38685c951ad3c00f93d0d3a302ca78fbadfa424.nq.gz
│   ├── c8ea83e84cfa0d2173e7f716946774a5a63d0c81.nq.gz
│   ├── cf3181f0069c35b544330851f026797e21d291ee.nq.gz
│   ├── d59d8e65c83c5f9b6fc6cfd9de46e0c4251cff0d.nq.gz
│   ├── d5c112835596d0798c6dac50fce0e399a3150b0f.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── d7606a9bd133aa0672b9761684aa670f0345e8a2.nq.gz
│   ├── e0a147509e7b63aaf2d41caa4096c95c735cc71c.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── e75ea308324d0a2c010f036b2371c557340f6cdc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5530c671a7078f4f06479422c623d10b846d3db9.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 38 files
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

[scrapy/scrapy-mcp-official](https://github.com/scrapy/scrapy-mcp-official)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
