# 🦉 OReg

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-2.0-cyan?style=flat-square"/>
</p>

> **OReg** — Persistence Forensic Tool

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OReg is a Linux persistence forensic tool. It audits common persistence mechanisms — cron, systemd, init.d, rc.local, SSH, shell profiles, kernel modules, SUID/SGID, at jobs, XDG autostart, LD_PRELOAD, passwd, sudoers, capabilities and writable PATH entries — and reports findings. It is intended for authorised security testing and typically requires root.

---

## ✨ Features

- Audits cron, systemd, init.d and rc.local persistence
- Reviews SSH, shell profiles, XDG autostart and LD_PRELOAD
- Inspects kernel modules, SUID/SGID binaries, capabilities and writable PATH entries
- Checks passwd, sudoers and at jobs
- Saves TXT/JSON/CSV reports and an optional HTML report
- Baseline capture and syslog forwarding for monitoring

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OReg --full
./OReg --audit cron
./OReg --full --save-baseline --html
./OReg --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OReg --help   # watch every network call
firejail --net=none ./OReg --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
