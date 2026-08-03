# AI Plugins Sandbox Marketplace

A lightweight marketplace repository for AI plugins, designed as a small sandbox for experimenting with plugin manifests, skill definitions, and curated plugin listings.

This workspace demonstrates how a compact catalog of AI plugins can be organized, documented, and shared in a repo-friendly structure for marketplace discovery and experimentation.

## Overview

The repository currently includes one educational plugin:

- Animal in Latin — an educational skill that provides the scientific (Latin) name of animals, along with brief contextual descriptions and classification details.

## Marketplace Structure

```text
.
├── README.md
├── plugins/
│   └── animal/
│       ├── README.md
│       └── skills/
│           └── in-latin/
│               ├── SKILL.md
│               └── .claude-plugin/
│                   └── plugin.json
├── .claude-plugin/
│   └── marketplace.json
└── .github/
    └── plugin/
        └── marketplace.json
```

## Getting Started

This project is a small marketplace example that can be used from the Claude Code CLI.

### 1) Register the marketplace repo

```bash
claude plugin marketplace add github:sp-acc/ai-plugins-sandbox
```

### 2) Browse the marketplace

```bash
claude plugin marketplace browse sp-marketplace
```

### 3) Install the plugin

```bash
claude plugin install in-latin@sp-marketplace
```

### 4) Use the plugin

After installation, invoke the plugin through the slash command:

```text
/in-latin tiger
```

The skill will return:

- common name
- scientific name
- family information
- status (extant or extinct)
- brief educational description

## Notes

This repository is intentionally compact and easy to extend. New plugins can be added by creating a new folder under `plugins/`, adding a `plugin.json`, and linking the corresponding skill files.

---

This sample marketplace is meant to showcase a clean pattern for delivering educational AI plugins in a reproducible repository layout.
