# Repolex Knowledge Graph of allenai/duplodocus

RDF knowledge graph data for [allenai/duplodocus](https://github.com/allenai/duplodocus), parsed by [repolex](https://repolex.ai).

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
rlex download allenai/duplodocus
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 02cf2f74334d4d87cdec8bec24238cc8fdbc3d95
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 02cf2f74334d4d87cdec8bec24238cc8fdbc3d95
│           └── chunk-001.nq.gz
├── blob
│   ├── 0392eaf59fed2e253615e287371991edee071385.nq.gz
│   ├── 05a7c17c562ad2af1646ad45ce144f61ef20c179.nq.gz
│   ├── 09f288ec9005d98ea46e7d99a6c70fc797d2fea4.nq.gz
│   ├── 0d817649eeef64ef04275ec0c77bf7b9dd601219.nq.gz
│   ├── 0ed21bd3461c39a237f0ece097ef98aa71941209.nq.gz
│   ├── 1576ae4cd7cea78266f2a01aadd7bbfc235d2146.nq.gz
│   ├── 19ff723e27715dca4b40366d9e507cbce332acd5.nq.gz
│   ├── 230d1e401a7caf29703765bc88256a1ad9cbbbda.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 2a7e2fc941861f4ec9bb95083cac58bf7eddfdef.nq.gz
│   ├── 352e282305d2d42fb84d4a84c52699844544509b.nq.gz
│   ├── 43d26c6007cef56048002aea36e20644712d10c4.nq.gz
│   ├── 4f556c94010393a71dfdb51ccea2fc7aef023666.nq.gz
│   ├── 5008ddfcf53c02e82d7eee2e57c38e5672ef89f6.nq.gz
│   ├── 57ed3398fa5df5ab78327d4e4f02d9bb6e0c52d6.nq.gz
│   ├── 5af17713b64d015c8cb42a970078413cd98432af.nq.gz
│   ├── 5e133a7b7b2231b5336f92a2390f279b44c1803b.nq.gz
│   ├── 765fa25018a2065b061e4be8870ba6332769f461.nq.gz
│   ├── 7f990f4e4ca886b5c745bf8ca21fe380082a04ff.nq.gz
│   ├── 91f088d02753e031061cb634bf0495c63b5de3da.nq.gz
│   ├── a7b49d0c73bc38a3e35bc7eeca68378d06a8bab8.nq.gz
│   ├── acd5e17afcd9407bb7c918b6e6fd1c714e769111.nq.gz
│   ├── bc6d9029ee507025ea2b1dbff01df852d1250012.nq.gz
│   ├── c7a18a74ae56dc35e49690ea206d4e08513114ba.nq.gz
│   ├── c7a7a9f1c83070ec0feadcd4d31515e29e3aa420.nq.gz
│   ├── c89ed9e996aa049c2514286219970fff1128086c.nq.gz
│   ├── cfd32beab749772c607ed04415464cfda7a15130.nq.gz
│   ├── d3a2601bfa715d7387c97c6f48ed2c58ba7137e0.nq.gz
│   ├── d8c7c7004ef341cdc3ecad9db5854e8e5288e1e0.nq.gz
│   ├── db25d67edbd818b23db7bc2085c08c903b1071bf.nq.gz
│   ├── dc5ffcc90c621fa43f7f288b7e08a0b5748e0407.nq.gz
│   ├── df5e4a1522fc7c7285cc3342acd1180d881cb2c6.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ec52b2d4cd0d758e13c1f9d9260c2d1eb6ab716a.nq.gz
│   ├── ed995a13879e467810ae0f6e179c6e24b1513c68.nq.gz
│   ├── f08ac8575847fb8cb3e13df901a699f2848d6366.nq.gz
│   ├── f3d22b94ab13c29988fd5a9d597fe9c74e36caed.nq.gz
│   ├── f85097ae63a0792f88aa49148e6dd713e0e7ffd4.nq.gz
│   ├── fa609229da44be28d86e5982163addb4f5cfab89.nq.gz
│   ├── ff02b9874b109857800357c68b7fd5121de5e843.nq.gz
│   └── ffc25f23cfbc0e89ccc068f5d34c8d1d7505a81a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 02cf2f74334d4d87cdec8bec24238cc8fdbc3d95.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 49 files
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

[allenai/duplodocus](https://github.com/allenai/duplodocus)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
