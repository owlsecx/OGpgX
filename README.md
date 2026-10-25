# 🦉 OGpgX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCipher-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OGpgX** — Offline GnuPG / OpenPGP Keyring Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OGpgX — Offline GnuPG / OpenPGP Keyring Auditor. It provides tolerant parser for gpg.conf, gpg-agent.conf and dirmngr.conf (comments, quoting, no-* negations); Crypto preference auditor — SHA1/MD5/RIPEMD160, 3DES/CAST5/IDEA/Blowfish, weak S2K, MDC overrides. Built-in demo/self-test paths and severity gates help validate detections without touching production when those flags are used.

---

## ✨ Features

- Tolerant parser for gpg.conf, gpg-agent.conf and dirmngr.conf (comments, quoting, no-* negations)
- Crypto preference auditor — SHA1/MD5/RIPEMD160, 3DES/CAST5/IDEA/Blowfish, weak S2K, MDC overrides
- Key-generation policy — default-new-key-algo check (ed25519/cv25519, nistp256+, rsa3072+)
- Privacy checks — auto-key-retrieve, cleartext hkp://, honor-keyserver-url, emitted version strings
- gpg-agent cache TTL, loopback / preset passphrase, passphrase-constraint policy review
- Colon-listing parser (gpg --with-colons) — weak key sizes, DSA/Elgamal, expired/revoked-yet-trusted keys, misplaced ultimate trust, v3 keys, SHA1 self-sigs

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OGpgX                                     # interactive menu
./OGpgX --scan
./OGpgX --demo
./OGpgX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
