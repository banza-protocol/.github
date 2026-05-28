# Banzami

**Open financial infrastructure for programmable payments, operators and settlement systems.**

Banzami is a protocol-first, open-source financial kernel designed for the African financial ecosystem. It defines the rules — wallets, transfers, ledger, settlement, traceability — so that any operator can build certified payment infrastructure without reinventing financial primitives.

---

## Ecosystem

| Repository | Description |
|------------|-------------|
| [banzami/banzami](https://github.com/banzami/banzami) | Open financial kernel — the protocol specification, Rust core, SDKs, and conformance suite |
| [banzami/banzamia](https://github.com/banzami/banzamia) | AI-native interface for building, validating and certifying Banzami operators |
| banzami/banza | First commercial operator — closed source |

---

## What Banzami is

- A **protocol specification** — wallet model, transfer protocol, QR payments, ledger, settlement, traces
- A **Rust financial core** — reference implementation with financial invariant enforcement
- A **conformance suite** — certification levels 0–4 for operators
- An **SDK ecosystem** — TypeScript, Flutter/Dart, PHP, Go
- An **AI orchestration layer** — BanzamIA for certification, onboarding and governance

## What Banzami is not

- A payment processor
- A bank or money transmitter
- A proprietary platform with vendor lock-in

---

## Financial invariants

Banzami is built around six non-negotiable financial properties:

| Invariant | Rule |
|-----------|------|
| INV-LEDGER-001 | Every transfer → equal DEBIT + CREDIT |
| INV-LEDGER-002 | No wallet may reach negative balance |
| INV-LEDGER-003 | Ledger entries are immutable once confirmed |
| INV-STL-001 | `net + fee == gross` (no money creation) |
| INV-STL-002 | Each transfer in exactly one settlement batch |
| INV-TRACE-001 | All entities in a flow share the same `trace_id` |

---

## Operator certification

Operators implement the Banzami protocol and get certified at one of five levels:

| Level | Name |
|-------|------|
| 0 | Reference-compatible |
| 1 | Protocol-compatible |
| 2 | Trace-compatible |
| 3 | Federation-ready |
| 4 | Settlement-compatible |

Run the conformance suite against your operator at any level using the tools in [banzami/banzami](https://github.com/banzami/banzami).

---

## Contributing

Banzami is open source. Contributions are welcome in:

- The protocol specification (RFCs, ADRs)
- The Rust financial core
- The SDK implementations
- The conformance suite
- The documentation

See [CONTRIBUTING.md](https://github.com/banzami/banzami/blob/main/CONTRIBUTING.md) to get started.

---

## Website

[banzami.org](https://banzami.org) — protocol documentation, operator registry, and developer resources.
