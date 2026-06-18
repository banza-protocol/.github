# BANZA

**Open financial protocol for programmable payments, operators, wallets, settlement, and certification.**

BANZA is a protocol-first, open financial infrastructure layer for wallet-native payments, transfers, settlement, traceability, and certified operators. It defines the rules — financial invariants, open contracts, certification criteria, and a federation/trust model — that any operator can implement to build certified payment infrastructure without reinventing financial primitives.

BANZA is a **specification, not a product**: it does not process payments, hold funds, or belong to any operator.

---

## Ecosystem

| Repository | Role |
|---|---|
| [`banza-protocol/banza`](https://github.com/banza-protocol/banza) | Open financial protocol — specifications, schemas, contracts, certification framework, and conformance suite |
| [`banza-protocol/banzami`](https://github.com/banza-protocol/banzami) | First commercial operator / payment network built on BANZA (reference Rust core and client SDKs) |
| [`banza-protocol/banzai`](https://github.com/banza-protocol/banzai) | AI-native knowledge, validation, certification, and governance layer for BANZA |
| [`banza-protocol/.github`](https://github.com/banza-protocol/.github) | Organization profile and public metadata |

> **BANZA is the protocol. Banzami is one operator built on it. BanzAI is the AI knowledge/certification layer.**
> Operators implement BANZA — Banzami operates on top of BANZA.

---

## What BANZA is

- A **protocol specification** — wallet model, transfer protocol, QR payments, ledger, settlement, traceability, and operator rules.
- **Open contracts and schemas** — OpenAPI, webhook schemas, QR payload, and event/federation contracts.
- A **conformance suite** — deterministic certification, levels L0–L4, for operators.
- A **trust and federation model** — a PKI hierarchy, operator certificates, and inter-operator routing.
- An **AI-assisted knowledge layer** — through BanzAI, for validation, onboarding, certification guidance, and documentation navigation.

Reference implementations — a Rust financial core and client SDKs (TypeScript, Flutter/Dart, and others) — live in the reference operator (`banzami`), demonstrating conformance. BANZA itself is **contract-first**: any language or stack that satisfies the contracts and passes the conformance suite is a valid implementation. There is no mandated SDK, language, or infrastructure.

## What BANZA is not

- A commercial payment app.
- A bank.
- A money transmitter.
- A closed, proprietary platform.
- A single operator.
- Banzami itself.

Banzami is only one operator built on BANZA. If every operator stopped tomorrow, BANZA — its rules, contracts, invariants, certification criteria, and federation model — would remain fully valid and available to any new operator.

---

## Financial invariants

BANZA is built around six non-negotiable financial properties — enforced by the protocol, verified by the conformance suite, regardless of implementation technology:

| Family | Guarantee |
|---|---|
| `INV-LEDGER-*` | Double-entry, immutability, integer precision, atomic postings |
| `INV-WALLET-*` | No negative balance; balances are always ledger-derived |
| `INV-SETTLE-*` | `gross = net + fee` — no money creation; settlement amount identity |
| `INV-IDEM-*` | The same idempotency key always produces the same result |
| `INV-RECON-*` | Posting linkage; externally reconcilable |
| `INV-QR-*` | Unique resolution; single-use dynamic QR; expiry enforcement |

---

## Operator certification

Operators implement the BANZA protocol and get certified at one of five levels — verified by a deterministic conformance suite, never by self-declaration:

| Level | Name |
|---|---|
| L0 | Protocol Sandbox |
| L1 | Core Payment Capability |
| L2 | Payment Initiation Capability |
| L3 | Inter-Operator Interoperability |
| L4 | External Interoperability |

L3 opens federation: certified operators route payments to one another without bilateral agreements. The **BANZA CA** issues certificates; **BanzAI** explains the criteria but never certifies.

Run the conformance suite against your operator using the tools in [`banza-protocol/banza`](https://github.com/banza-protocol/banza).

---

## Contributing

BANZA is open source. Contributions are welcome in:

- The protocol specification (RFCs, ADRs)
- The open contracts and schemas
- The conformance suite
- The documentation
- BanzAI protocol knowledge and validation workflows

See the contributing guides in each repository to get started.

---

## Website

[banzami.org](https://banzami.org) — public documentation for the BANZA ecosystem, including protocol documentation, operator registry, developer resources, and Banzami operator information.

Contact: [contact@banzami.org](mailto:contact@banzami.org)
