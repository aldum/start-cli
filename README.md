<p align="center">
  <img src="https://raw.githubusercontent.com/Start9Labs/start-os/refs/heads/master/web/projects/shared/assets/img/icon.png" alt="Project Logo" width="11%">
</p>

# 📦 Start CLI  

**Start CLI (`start-cli`)** is the official command-line tool for **StartOS** - a sovereignty-first operating system empowering anyone to run and host their own services independently.

The CLI is **essential** for:  
- building and packaging services into the **`.s9pk`** (StartOS Service Package) format,  
- remotely managing a StartOS node (listing services, installing, updating, backups, monitoring),  
- integrating StartOS with CI/CD pipelines and developer tooling.  

This repository provides **prebuilt `start-cli` binaries** for:  
- macOS (Intel x86_64 & Apple Silicon ARM64),  
- Linux (Intel x86_64 & ARM64).  

Official StartOS source code is here: [start9labs/start-os](https://github.com/start9labs/start-os).  

---

## 🔧 Installation

Download the binary archive matching your platform from the [Releases](https://github.com/start9Labs/start-cli/releases) page.  

### macOS (Intel & Apple Silicon)
```
tar -xzf start-cli-x86_64-apple-darwin.tar.gz     # Intel
tar -xzf start-cli-aarch64-apple-darwin.tar.gz    # Apple Silicon
chmod +x start-cli-*
mv start-cli-* /usr/local/bin/start-cli
```

### Linux (x86_64 & ARM64)
```
tar -xzf start-cli-x86_64-unknown-linux-gnu.tar.gz    # Intel/AMD64
tar -xzf start-cli-aarch64-unknown-linux-gnu.tar.gz   # ARM64 (e.g. ARM servers, Raspberry Pi)
chmod +x start-cli-*
sudo mv start-cli-* /usr/local/bin/start-cli
```
---

## 🔄 Release Workflow

Binaries are built and published automatically using **GitHub Actions** workflow:  

- Triggered on each new **tag** pushed (`vX.Y.Z`),  
- Builds for all supported platforms,  
- Generates SHA256 checksums for integrity verification,  
- Publishes a GitHub Release with `.tar.gz` archives ready for download.  
