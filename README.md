# gerbil-lsp-plugin

Claude Code marketplace plugin for [gerbil-lsp](https://github.com/ober/gerbil-lsp), a language server for Gerbil Scheme.

## Features

- Diagnostics (compilation errors and parse failures)
- Code completion
- Hover information
- Go-to-definition
- Find references
- Document symbols / workspace symbol search
- Rename
- Code formatting

## Prerequisites

Install gerbil-lsp:

```bash
git clone https://github.com/ober/gerbil-lsp
cd gerbil-lsp
make build
make install
```

Verify it's available:

```bash
gerbil-lsp --version
```

## Setup

### 1. Add the marketplace plugin

```
/plugin marketplace add ober/gerbil-lsp-plugin
```

### 2. Enable in `~/.claude/settings.json`

Add the following to your `~/.claude/settings.json`:

```json
{
  "env": {
    "ENABLE_LSP_TOOL": "1"
  },
  "enabledPlugins": {
    "gerbil-lsp-plugin@claude-plugins-official": true
  }
}
```

### 3. Restart Claude Code

The LSP server will start automatically when you open `.ss` files.
