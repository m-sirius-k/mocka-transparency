# MoCKA Transparency v2

Japanese version: README.ja.md

---

## 3-Minute Transparency Demo (Sample01)

This demo lets you experience tamper detection.

Flow:

1. Verify the sealed state (PASS)
2. Tamper with the file
3. Verification fails (FAIL)
4. Restore and verify again (PASS)

---

### 1. Clone

git clone https://github.com/nsjpkimura-del/mocka-transparency.git
cd mocka-transparency

---

### 2. Verify (should PASS)

powershell -NoProfile -ExecutionPolicy Bypass -File .\scripts\verify_one.ps1

Expected output:
PASS: Sample01 verified

---

### 3. Run tamper demo (should FAIL)

powershell -NoProfile -ExecutionPolicy Bypass -File .\scripts\tamper_demo.ps1

Expected output:
FAIL: decision_log.json sha256 mismatch

---

### 4. Restore (PASS again)

git restore .\sample01\decision_log.json
powershell -NoProfile -ExecutionPolicy Bypass -File .\scripts\verify_one.ps1

---

What this demonstrates:

- Sealed logs cannot be silently modified
- Tampering is immediately detected
- Verification uses only public keys
- Recovery is deterministic via Git
# MoCKA Ecosystem

This repository is part of the **MoCKA Civilization Research Ecosystem**.

MoCKA studies AI civilization systems including governance, consensus and institutional memory.

## Ecosystem Structure

Research Core  
MoCKA

Civilization Theory  
mocka-civilization

Knowledge System  
mocka-knowledge-gate

Transparency Layer  
mocka-transparency

Network Layer  
mocka-outfield

Civilization Core (private)  
mocka-core-private

## 概要

このリポジトリは **MoCKA AI文明研究エコシステム** の一部です。

MoCKAはAI文明の制度、合意形成、知識継承を研究するプロジェクトです。

## 文明構造

研究コア  
MoCKA

文明理論  
mocka-civilization

知識システム  
mocka-knowledge-gate

透明性  
mocka-transparency

ネットワーク  
mocka-outfield

文明コア（非公開）  
mocka-core-private

