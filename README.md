# Repolex Knowledge Graph of tiangolo/meinheld-gunicorn-docker

RDF knowledge graph data for [tiangolo/meinheld-gunicorn-docker](https://github.com/tiangolo/meinheld-gunicorn-docker), parsed by [repolex](https://repolex.ai).

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
rlex download tiangolo/meinheld-gunicorn-docker
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 70cb7974f40ee6719e429bc4485d4f92c6f65ed4
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 70cb7974f40ee6719e429bc4485d4f92c6f65ed4
│           └── chunk-001.nq.gz
├── blob
│   ├── 0045fb8182cf94a55db192aa3bc8c4c7e033da47.nq.gz
│   ├── 0ffc101a3f23548392499fe5104f3f8cf4d4e91b.nq.gz
│   ├── 252e25eab0580218af219612e01b805f1d9df032.nq.gz
│   ├── 36588ee4003be844eba792f0a31ff9a19757c9ff.nq.gz
│   ├── 44bb880652b8b654769933fa8fc2997d46421f5a.nq.gz
│   ├── 45951c5782fdac49e128c4aafc806e166e0cc9ee.nq.gz
│   ├── 4613b22c0005228ac22fdb640858e579ac64e9a0.nq.gz
│   ├── 463566dd085915237069c231779fc0d46dc98300.nq.gz
│   ├── 4f59d025a98c990997f39606b888dedc9e7f4dcc.nq.gz
│   ├── 4f8174b20971969872947e41469fa9a5d7a644a3.nq.gz
│   ├── 4fc70af2e28837604c3861d2ddcda8ff466be01e.nq.gz
│   ├── 516f76fa05cb7981adc2229a847e639b816b66fb.nq.gz
│   ├── 52b221999c9a477686bbce90c5f5e2542cdb0c79.nq.gz
│   ├── 52c89067d30e0e9f306bfd578f3668e3f7e646c0.nq.gz
│   ├── 55eec6eb458d17b0a36c90625488d8fafbda90d5.nq.gz
│   ├── 695fdeb2bd72ba32ec9882588f9798181f881af0.nq.gz
│   ├── 6acdc987b2cec000d457c146392f4108e2689ee7.nq.gz
│   ├── 6d57d20dee6a1ef716b1c26ab4023d3a2263f43a.nq.gz
│   ├── 70a3289a8e27d16ce6a7275bbf079d2c2fce79c2.nq.gz
│   ├── 7a9bbce4c6565fd7558784d98d7c0166f92a142b.nq.gz
│   ├── 7cceeeac5f3432cbe09e7193d6664584e0528382.nq.gz
│   ├── 8143a2363e47576a52ab8a34e2e20acf80f695b1.nq.gz
│   ├── 8d9ad92d90926089d5e92da0af59a23854fdec67.nq.gz
│   ├── 92e4a19c0b6a6053b58997c850cd6be43836c7ec.nq.gz
│   ├── 94143827ed065ca0d7d5be1b765d255c5c32cd9a.nq.gz
│   ├── 96edf219890d21b6c076b1c23cbb77d698bf3120.nq.gz
│   ├── 9ccb1dabcbaf7082ebc12fdefdb7c061d05983e2.nq.gz
│   ├── a0ff6523ede705c5c4f7fa81e6914263f7931274.nq.gz
│   ├── af6abf466199d728b7d86a70aa2c9c94686ada74.nq.gz
│   ├── bcf66db271f562c0a0109c812faf7d21475f878e.nq.gz
│   ├── c27d231a76f21d09a3b2e5d5ddbf03d27f05b9ac.nq.gz
│   ├── cd972a0ba47221bf96acedfaed8f3b5cba819849.nq.gz
│   ├── d0a3ca3d7dafa779568bba43952512887bdb02a4.nq.gz
│   ├── d2b94552b6b4b5cbfe732ee1c4436a1243f532b3.nq.gz
│   ├── da9491031271961a7477401c0635cd3c6cb23a16.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f456e7265408920b8adcbd573c39865fe1d0eb96.nq.gz
│   └── feec529f1e6a2c68172ce4c39dca6419764cdbfa.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 70cb7974f40ee6719e429bc4485d4f92c6f65ed4.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 46 files
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

[tiangolo/meinheld-gunicorn-docker](https://github.com/tiangolo/meinheld-gunicorn-docker)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
