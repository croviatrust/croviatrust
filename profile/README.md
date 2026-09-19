<p align="center"><img src="https://croviatrust.com/logo.png" width="64" alt=""></p>

<h2 align="center">Crovia — silence you can verify</h2>

<p align="center">
  <a href="https://croviatrust.com/registry/tacet/">Live log</a> ·
  <a href="https://github.com/croviatrust/countersign/blob/main/tacet/SPEC.md">TACET spec</a> ·
  <a href="https://croviatrust.com/whitepaper.html">Whitepaper</a> ·
  <a href="https://croviatrust.com/llms.txt">For LLMs</a> ·
  <a href="https://github.com/croviatrust/countersign/blob/main/CANON.md">Canon</a>
</p>

<p align="center">
  <a href="https://croviatrust.com/registry/tacet/"><img alt="TACET epochs (live)" src="https://img.shields.io/endpoint?url=https%3A%2F%2Fcroviatrust.com%2Fregistry%2Fdata%2Ftacet%2Fbadges%2Fepochs.json"></a>
  <a href="https://croviatrust.com/registry/data/tacet/targets.json"><img alt="models observed (live)" src="https://img.shields.io/endpoint?url=https%3A%2F%2Fcroviatrust.com%2Fregistry%2Fdata%2Ftacet%2Fbadges%2Fmodels.json"></a>
  <a href="https://croviatrust.com/registry/data/tacet/latest.json"><img alt="signed observations of absence (live)" src="https://img.shields.io/endpoint?url=https%3A%2F%2Fcroviatrust.com%2Fregistry%2Fdata%2Ftacet%2Fbadges%2Fnegative.json"></a>
</p>

Every hour, a public randomness beacon opens an epoch. **TACET** fetches the model
cards of the AI systems under watch, runs a published predicate over the bytes —
*does this card name its training data?* — signs each answer, commits them all to a
sparse Merkle map, and anchors the hour in Bitcoin. When a lab stays silent about
training data, the silence becomes a **proof anyone can verify offline**.

> Crovia states observation facts, bounded by two public clocks. It never asserts intent.

**Verify a proof in your browser** — nothing to install:
[croviatrust.com/registry/seal/verify/?url=…](https://croviatrust.com/registry/seal/verify/?url=https%3A%2F%2Fcroviatrust.com%2Fregistry%2Fdata%2Ftacet%2Fproofs%2Fmistralai__Mistral-7B-v0.1.seal.json)

```bash
pip install -e countersign/tacet/reference/python -e crovia-seal/reference/python -e countersign/tacet/operator
curl -sO https://croviatrust.com/registry/data/tacet/proofs/mistralai__Mistral-7B-v0.1.seal.json
tacet-operator verify mistralai__Mistral-7B-v0.1.seal.json      # recomputes roots, drand, Bitcoin anchors, signatures
```

### Repositories

| | |
|---|---|
| **[countersign](https://github.com/croviatrust/countersign)** | **TACET**: specification, reference implementation, conformance vectors, the live operator, the canon and the site sources. Start here. |
| **[crovia-seal](https://github.com/croviatrust/crovia-seal)** | The **Crovia Seal** (`crovia.seal.v1`): tamper-evident, offline-verifiable receipts for AI outputs. IETF Internet-Draft. Every TACET proof is a Seal. |
| [crovia-core-engine](https://github.com/croviatrust/crovia-core-engine) | The 2026 archive substrate (collectors, signed envelopes, batch seals, anchors). Observation paused 2026-06-01; data stays public. |
| [crovia-evidence-lab](https://github.com/croviatrust/crovia-evidence-lab) | Public data exports of the archive, CC-BY-4.0. |
| [causari](https://github.com/croviatrust/causari) | Sibling product: causal provenance of what AI **agents** do to a codebase. Same Seal, different subject. |

### Crovia is not Causari

| | **Crovia** | **Causari** |
|---|---|---|
| Watches | what AI **providers disclose** about **training data** | what AI **agents do** to **your codebase** |
| For | regulators, litigators, journalists, the public | software developers |
| Output | TACET silence proofs, LACUNA certificates | causal provenance of code edits |
| Home | [croviatrust.com](https://croviatrust.com) | [causari.dev](https://causari.dev) |

### Conduct

This account does not open issues, pull requests or discussions on repositories outside
`croviatrust/*`. An automated outreach experiment in early 2026 was stopped and will not
resume. If you received an unsolicited issue from us, we apologise — write to
info@croviatrust.com.

---

Independent · no vendor money · code Apache-2.0 · specs CC0 · data CC-BY-4.0 · info@croviatrust.com
