# Pustaka Terbuka — BNM (Bank Negara Malaysia Knowledge Management Centre)

> **Pustaka Terbuka: Katalog Induk Terbuka untuk Perpustakaan dan Sekolah Malaysia.**  
> *Official Bank Negara Malaysia Knowledge Management Centre (BNM) Bibliographic Dataset & Standalone Harvester.*

This repository contains the harvested open MARCXML collection and harvester pipeline for **Bank Negara Malaysia Knowledge Management Centre** (`BNM`), contributing to the national Malaysian union catalog at [pustaka-terbuka/opac](https://github.com/pustaka-terbuka/opac).

---

## Institutional Metadata

| Attribute | Value |
| :--- | :--- |
| **Institution Code** | `bnm` |
| **Agency Code** | `BNM` |
| **Official Name** | Bank Negara Malaysia Knowledge Management Centre |
| **Institution Type** | `special` |
| **State / Territory** | Kuala Lumpur |
| **Target End Bib** | 150,000 |
| **OPAC Base URL** | [https://library.bnm.gov.my/](https://library.bnm.gov.my/) |
| **Subject Focus** | Central banking, monetary policy, Islamic finance, economics, and banking supervision |

---

## Directory Structure

```text
bnm/
├── README.md                      # Institutional repository documentation
├── package.json                   # Node.js project specification & scripts
├── harvest/
│   └── inbox/bnm/             # Sealed MARCXML batch chunks and manifests
│       └── <run-id>-chunk-001/
│           ├── manifest.json      # Chunk SHA-256 manifest & metadata
│           ├── provenance.jsonl   # Record-level attribution and fetch logs
│           └── records/           # Batched MARC21 slim XML files
├── tools/
│   ├── harvesters/bnm/        # Automated OPAC crawler & XML converter
│   └── lib/                       # Supporting MARCXML and validation utilities
└── tests/
    └── harvester-bnm.test.js  # Autonomous test suite
```

---

## Usage

```bash
# Install dependencies
npm install

# Test run harvester (10 sample records)
npm run harvest:sample

# Run full collection sweep
npm run harvest:full

# Validate dataset integrity
npm run validate-inbox harvest/inbox/bnm/<chunk-directory>
```

---

## Attribution & License

Dataset harvested and preserved under open library metadata standards for educational, civic, and cooperative indexing. Attribution: **Bank Negara Malaysia Knowledge Management Centre (BNM)** & **Pustaka Terbuka**.
