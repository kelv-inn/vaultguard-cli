# VaultGuard CLI

🔐 **Scan. Store. Secure.**

A minimal developer tool to scan your code for secrets and store them locally. No cloud. No complexity. Just security.

## Installation

### Global Installation
```bash
npm install -g vaultguard-cli
```

## Quick Start

```bash
# Scan a file for secrets
vaultguard scan myfile.js

# Protect your .env file
vaultguard protect

# Store a secret safely
vaultguard safeadd API_KEY=sk_123456789

# Add custom secret pattern
vaultguard addpattern "myapi_[0-9A-F]{16}"
```

## Commands

### Basic Commands
- `vaultguard scan <file>` - Scan a file for secrets
- `vaultguard vault add <key>=<value>` - Store a key-value pair
- `vaultguard vault show` - Show all stored secrets (masked)
- `vaultguard vault export` - Export secrets as .env file

### Protection Commands
- `vaultguard protect` - Protect .env file with encoding and decoys
- `vaultguard decode [--file <file>]` - Decode .vg files back to .env
- `vaultguard safeadd <key>=<value>` - Create secure folder structure
- `vaultguard safeadd --protect <key>=<value>` - Combine safeadd with protection

### Configuration
- `vaultguard addpattern <pattern>` - Add custom secret detection pattern
- `vaultguard version` - Show CLI version
- `vaultguard help` - Show help message

## Features

- 🔍 **Secret Detection**: Automatically detects API keys, tokens, and passwords
- 🔒 **Local Protection**: Encodes and creates decoy files for your .env
- 📁 **Safe Storage**: Creates secure folder structures for sensitive data
- 🎯 **Custom Patterns**: Add your own regex patterns for secret detection
- 🚫 **No Cloud**: Everything stays on your machine

## License

MIT
