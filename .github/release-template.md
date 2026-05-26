Automated standalone Termux build of the Antigravity CLI v{{VERSION}}.

> [!IMPORTANT]
> **Twin-Binary Requirement:** The release package contains **two** binaries: `bin/agy` and `bin/agy.va39`.
> * `bin/agy.va39` is the core patched engine.
> * `bin/agy` is the native Bionic C bootstrapper.
> **Always execute the `./bin/agy` binary.** It automatically clears conflicts and executes the core engine. You **must** keep both files in the same directory for the bootstrapper to run successfully.

### 🔀 Standalone Fork Changelog
{{FORK_CHANGELOG}}

### ⬆️ Upstream Changelog (v{{VERSION}})

{{UPSTREAM_NOTES}}

### 📦 Installation
To install this release, extract the package to your preferred location (e.g. `~/.local` or a sandbox folder) and execute the C helper directly:
```bash
# 1. Download and extract
curl -fsSLO https://github.com/{{REPO}}/releases/download/v{{VERSION}}/antigravity-termux-standalone.tar.gz
tar -xzf antigravity-termux-standalone.tar.gz

# 2. Run immediately without shell configuration or wrappers!
./bin/agy --help
```

### 🔒 Cryptographic Verification
This release is signed with cryptographic build provenance. Verify it natively using the GitHub CLI:
```bash
gh attestation verify antigravity-termux-standalone.tar.gz -R {{REPO}}
```
