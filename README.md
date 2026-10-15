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

Offline GnuPG / OpenPGP keyring & configuration auditor

---

## ✨ Features

- Tolerant parser for gpg.conf, gpg-agent.conf and dirmngr.conf (comments, quoting, no-* negations)
- Crypto preference auditor — SHA1/MD5/RIPEMD160, 3DES/CAST5/IDEA/Blowfish, weak S2K, MDC overrides
- Key-generation policy — default-new-key-algo check (ed25519/cv25519, nistp256+, rsa3072+)
- Privacy checks — auto-key-retrieve, cleartext hkp://, honor-keyserver-url, emitted version strings
- gpg-agent cache TTL, loopback / preset passphrase, passphrase-constraint policy review
- Colon-listing parser (gpg --with-colons) — weak key sizes, DSA/Elgamal, expired/revoked-yet-trusted keys, misplaced ultimate trust, v3 keys, SHA1 self-sigs
- ASCII-armor reader with CRC24 verification and a read-only OpenPGP packet walker (version, algo, creation, key-id, fingerprint, signature subpackets) — never decrypts anything
- --homedir tree scan — permissions on homedir, private-keys-v1.d, secring.gpg, unprotected key files, revocation certificates, ownership
- Optional read-only live listing (gpg --list-keys)
- CWE + MITRE ATT&CK mapping, severity, remediation
- Hardened configuration template generator
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Built-in --demo self-test with temp homedir
- Full CLI mode (--homedir, --conf, --listing, ...)

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OGpgX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
