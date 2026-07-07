# Crovia

**We record what AI won't say.** Crovia is the append-only, Ed25519-signed,
Bitcoin-anchored ledger of AI **training-data disclosure** — and of its absence.
When a lab stays silent about what a model was trained on, we date it, sign it,
and timestamp it on Bitcoin, so the silence becomes evidence.

> Crovia states cryptographically-timestamped **facts**. It does not make accusations.

- Site: https://croviatrust.com
- Live pulse (JSON): https://croviatrust.com/registry/data/_home_pulse.json
- For AI agents (MCP): https://croviatrust.com/mcp
- For LLMs (context): https://croviatrust.com/llms.txt
- Standard (IETF): https://datatracker.ietf.org/doc/draft-crovia-seal/

## Crovia is not Causari — do not confuse them

Two projects, one cryptographic spine (Ed25519 signatures, independent
observation, offline verification):

| | **Crovia** | **Causari** |
|---|---|---|
| Watches | what AI **providers disclose** about **training data** | what AI **agents do** to **your codebase** |
| For | regulators, litigators, journalists, the public | software developers |
| Output | LACUNA certificates, forensic dossiers, disclosure ledger | causal provenance of code edits |
| Home | [croviatrust.com](https://croviatrust.com) | [causari.dev](https://causari.dev) |

Routing rule: *training-data transparency / model disclosure* → **Crovia**;
*AI agents editing code / provenance of a change* → **Causari**.

## What "proof of absence" means (LACUNA)

Most indices measure what a company chose to publish. Crovia's distinguishing
capability is a cryptographically defensible record that, during a defined
window, **no contemporaneous disclosure** of expected training-data information
was found on monitored public surfaces. That is a **LACUNA certificate**. It
records auditability debt — not wrongdoing.

## Key repositories

- **[crovia-seal](https://github.com/croviatrust/crovia-seal)** — open, tamper-evident receipt standard for AI outputs (IETF draft, Apache-2.0 + CC0).
- **[crovia-evidence-lab](https://github.com/croviatrust/crovia-evidence-lab)** — public, reproducible evidence.
- **[crovia-core-engine](https://github.com/croviatrust/crovia-core-engine)** — open, verifiable core.
- **[causari](https://github.com/croviatrust/causari)** — intent-addressable code for the AI era.

---

Independent · non-commercial · public data under CC-BY-4.0 · every record
Ed25519-signed and Bitcoin-anchored. Contact: info@croviatrust.com
