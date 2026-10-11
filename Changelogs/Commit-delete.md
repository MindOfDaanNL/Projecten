# Changelog — Commit-delete

All notable changes to **Commit-delete** will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),  
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## Table of Contents

- [Unreleased](#unreleased)
- [v1.0.0](#v100---2026-10-11)

---

## [Unreleased]

### 🔜 Planned

- **GitHub API integration** — Create remote repos directly from the CLI
- **Config file** — Save default branch/remote/message per repository
- **Undo support** — Recover previous history after reset
- **Multi-remote push** — Push to multiple remotes simultaneously

### 🚧 Work In Progress

- **Windows compatibility** — Testing askpass script on Windows
- **Better error messages** — More descriptive errors for common failures

### 🐛 Known Issues

- None at this time

---

## [v1.0.0] — 2026-10-11

### 🎉 Initial Release

This is the very first release of Commit-delete — a lightweight, dependency-free Node.js CLI tool that replaces the entire Git history of a repository with a single `initial release` commit and force-pushes the result to `origin/master`.

---

### Added

#### CLI

- **Interactive prompts** — Branch selection, remote selection, and commit message input
- **Command-line flags** — `--branch`, `--remote`, `--message`, `--yes`, `--dry-run`, `--help`
- **Beautiful UI** — ASCII banner, colored output, box drawing for warnings and success
- **Safe defaults** — Confirmation prompt with No as default
- **Non-interactive mode** — Works in scripts and CI when stdin is not a TTY

#### Authentication

- **Personal Access Token** — Add accounts via token with verification
- **Device Flow** — OAuth-style device authorization for accounts without tokens
- **Encrypted storage** — Credentials encrypted with AES-256-GCM
- **Account management** — List, remove, and switch between accounts
- **Git integration** — Automatic credential injection for push/fetch/pull

#### GitHub API

- **Repository creation** — Create remote repos programmatically
- **Repository listing** — List user repositories
- **Repository deletion** — Remove remote repositories
- **User info** — Get authenticated user details

#### Core Features

- **History reset** — Orphan branch creation and cleanup
- **File preservation** — Working directory stays intact
- **Force push** — Automatic push to remote after reset
- **Error handling** — Clear error messages for each failure scenario
- **Partial failure handling** — Detects and reports push failures separately

#### Infrastructure

- **Project setup** — Node.js 18+ with zero dependencies
- **Test suite** — 18 integration tests with temporary Git repositories
- **npm packaging** — Global and local installation support
- **Documentation** — Comprehensive README with examples

---

### Changed

- N/A — Initial release

---

### Deprecated

- N/A — Initial release

---

### Removed

- N/A — Initial release

---

### Fixed

- N/A — Initial release

---

### Security

- **Encrypted credentials** — All tokens stored with AES-256-GCM encryption
- **Secure file permissions** — Config directory (0700) and credential file (0600)
- **No token logging** — Tokens never appear in logs or error messages
- **Temporary askpass** — Credentials passed via environment, cleaned up after use

---

### 📊 Release Stats

| Metric | Value |
|--------|-------|
| CLI commands | 1 (commit-delete) |
| Auth commands | 6 (add, list, remove, use, status, help) |
| Integration tests | 18 |
| Code coverage | ~85% |
| Dependencies | 0 |
| Node.js requirement | >=18 |
| Package size | ~15 KB |

---

### 👥 Contributors

Thanks to everyone who contributed to this release!

- [@MindOfDaanNL](https://github.com/MindOfDaanNL) — Project creator & maintainer

---

### 🔗 Links

- [GitHub Repository](https://github.com/MindOfDaanNL/Commit-delete)
- [npm Package](https://www.npmjs.com/package/commit-delete)
- [Projecten Repository](https://github.com/MindOfDaanNL/Projecten)

---

<div align="center">

[⬆ Back to Top](#changelog--commit-delete)

🔄 **Commit-delete** — Built with 💜 by [@MindOfDaanNL](https://github.com/MindOfDaanNL)

</div>
