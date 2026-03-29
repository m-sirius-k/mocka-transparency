# MoCKA Transparency — Tamper Detection Layer

<p align="center">
  <img src="https://raw.githubusercontent.com/m-sirius-k/MoCKA/main/docs/images/mocka_overview.svg" width="800">
</p>

> **This is not a security scanner. Not a firewall. Not an access control system.**
> It is the layer that proves nothing has been altered —
> cryptographically, independently, and publicly.
>
> Not "trust us."
> "Verify yourself."

---

## Position in mocka_Movement

<p align="center">
  <img src="https://raw.githubusercontent.com/m-sirius-k/MoCKA/main/docs/images/mocka_architecture_v2.svg" width="720">
</p>
```
MoCKA (core · heart)
      ↓
mocka-knowledge-gate       ② Record
      ↓
[ mocka-transparency ]     ← ③ Incident · ④ Recurrence — YOU ARE HERE
      ↓
mocka-external-brain       ⑥ Decision
      ↓
mocka-civilization         ⑧ Institutionalize
```

**Loop step: ③ Incident · ④ Recurrence**
Upstream: mocka-knowledge-gate → sends sealed records
Downstream: mocka-external-brain → receives verified findings

---

## What this repository does

<p align="center">
  <img src="https://raw.githubusercontent.com/m-sirius-k/MoCKA/main/docs/images/mocka_loop_v2.svg" width="720">
</p>

mocka-transparency provides cryptographic proof that every record is authentic.

- **Ed25519 digital signatures** — every governance event is signed
- **SHA256 hash chain** — append-only, tamper-evident history
- **Public verification** — anyone can verify, no trust required
- **Tamper detection** — even one byte changed is detected

If anything was altered — the system detects it.
If the chain is intact — the system proves it.

---

## shadow_Movement and transparency
```
Primary path fails
      ↓
shadow_Movement activates
      ↓
mocka-transparency preserves the evidence
      ↓
Failure is recorded · analyzed · institutionalized
      ↓
The civilization loop continues
```

shadow_Movement is not a backup.
mocka-transparency ensures the evidence survives
even when the primary path fails.

---

## Quick Start
```powershell
# Verify the hash chain
python verify_chain.py
# → CHAIN OK

# Run all governance checks
python verify_all.py
# → ALL CHECKS PASSED

# Demonstrate tamper detection
.\tamper_demo.ps1
```

---

## Status

**Active Development**
Part of the MoCKA deterministic governance architecture.
Loop position: ③ Incident · ④ Recurrence

---

## 日本語

### MoCKA Transparencyとは何か

セキュリティスキャナーではありません。ファイアウォールでもありません。
何も改ざんされていないことを暗号的に・独立して・公開可能な形で証明する層です。

「信頼してください」ではなく「自分で検証してください」。

### mocka_Movementにおける位置づけ
```
MoCKA（コア・心臓部）
      ↓
mocka-knowledge-gate       ② Record
      ↓
[ mocka-transparency ]     ← ③ Incident · ④ Recurrence — ここです
      ↓
mocka-external-brain       ⑥ Decision
      ↓
mocka-civilization         ⑧ 制度化
```

**ループステップ：③ Incident · ④ Recurrence**
上流：mocka-knowledge-gate → 封印済み記録を送信
下流：mocka-external-brain → 検証済み知見を受信

### このリポジトリの役割

すべての記録が本物であることを暗号的に証明します。

- **Ed25519デジタル署名** — 全ガバナンスイベントが署名済み
- **SHA256ハッシュチェーン** — 追記専用・改ざん検知可能な履歴
- **公開検証** — 誰でも検証可能・信頼不要
- **改ざん検知** — 1バイトでも変更があれば検出

### shadow_Movementとの関係

shadow_Movementはバックアップではありません。
mocka-transparencyは主系が停止しても証拠を保全し、
文明ループが継続することを保証します。

---

Part of the [MoCKA Deterministic Governance Architecture](https://github.com/m-sirius-k/MoCKA).
