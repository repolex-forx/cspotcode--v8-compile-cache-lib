# Repolex Knowledge Graph of cspotcode/v8-compile-cache-lib

RDF knowledge graph data for [cspotcode/v8-compile-cache-lib](https://github.com/cspotcode/v8-compile-cache-lib), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download cspotcode/v8-compile-cache-lib
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 35dfbc6db9fb006f8a39dd16430d11f254cc2b1d
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 35dfbc6db9fb006f8a39dd16430d11f254cc2b1d.nq.gz
│   └── repolex
│       └── 35dfbc6db9fb006f8a39dd16430d11f254cc2b1d
│           └── chunk-001.nq.gz
├── blob
│   ├── 03e05e4c07174bdbd4a86a6206af4fa88b03f743.nq.gz
│   ├── 0593febf50ed0adb4cfd31a143b13c29b51f4897.nq.gz
│   ├── 08201ac62569d8c8ffbf8fa23866d08c7cdfaca8.nq.gz
│   ├── 11056fb56746b05b977bbb6890ca7e4440116895.nq.gz
│   ├── 1b8fd4e1545b269f14147206dc034c0211fa1c13.nq.gz
│   ├── 230ee9419f81dc770b396b64cf5bca1dab4b2692.nq.gz
│   ├── 2ac14b695ff239fe675c7ba991e06baa20474cc0.nq.gz
│   ├── 35037757e291796f9e69cde4dd101f84daf45b96.nq.gz
│   ├── 36ca6e14a0364bf6c6a8925877fea9b07262ca19.nq.gz
│   ├── 444765314e3f4de66421cfa3c5405152ebfe1b7a.nq.gz
│   ├── 46a24029ef1cff2fa36510640b3318d27ba7131f.nq.gz
│   ├── 536e4f2f3cfb36b12fb1e0ae4a5b1854e8ea5261.nq.gz
│   ├── 75fa9f9dac9b41548f4f86aada9b5db10837d059.nq.gz
│   ├── 80699a25f70a419dd47058c3c0dd7ba50587c9b8.nq.gz
│   ├── 88a36c31385db1d9f519e8c24ab40a1baf6d82f2.nq.gz
│   ├── 89b65633541dbe49003f7b0ea8996756ea777c09.nq.gz
│   ├── 9afc2dde4ee812dce44259a289cede6efd49913f.nq.gz
│   ├── a843dc44a1976c152e2574507ed2e47b201a2488.nq.gz
│   ├── b72b6701877c7fe12d5a1ada87676616fcf03b42.nq.gz
│   ├── baedb360c0e40e1472b3316d12f6220b96f03ecf.nq.gz
│   ├── bbb5fcef0d51d3a3622469db91fc1983e581f36a.nq.gz
│   ├── ce195a18e0ec9800214fcf3db5b844743900430d.nq.gz
│   ├── d4da256947c37da6d37ab24d75e2e89ba20d35e1.nq.gz
│   ├── d57f54f037785120ffc58b50933498b1592015b2.nq.gz
│   ├── d8103a3c785806782b4c4453a972953b0ecf0745.nq.gz
│   ├── e0cdf14855f50e6b9a4c47621106f0f4126a8dc5.nq.gz
│   ├── e7b1d1706a5af541a04f851649ff76f4b352dbef.nq.gz
│   ├── e905b105a50d15c8768dc4d90744c03d428b396d.nq.gz
│   ├── eca7a46cb3873cb3719ba8d0cea33da7ce570ed9.nq.gz
│   ├── ecbfb708a00c3b88261fc19d5b18208a645a3fc2.nq.gz
│   ├── ee76c741a6a73f002de1f8a0b1c3632eb0b2d9ec.nq.gz
│   └── fb80c2c9e62d85d08f8a9ac57647de7f77368844.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 35dfbc6db9fb006f8a39dd16430d11f254cc2b1d.nq.gz
├── filetree
│   └── 35dfbc6db9fb006f8a39dd16430d11f254cc2b1d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 42 files
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

## Source repository

[cspotcode/v8-compile-cache-lib](https://github.com/cspotcode/v8-compile-cache-lib)

---
*Parsed on 2026-04-25 by [repolex](https://repolex.ai)*
