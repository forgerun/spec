# ForgeRun Specification

This repository contains the **canonical protocol specification** for ForgeRun.

ForgeRun is a neutral transparency protocol for recording governance-relevant decisions made by automated systems into **public, append-only ledgers**, enabling independent verification of *inclusion*, *integrity*, and *consistency* without trusting the operator.

This repository defines:

- The protocol surface and invariants
- Commitment and receipt semantics
- Verification and consistency guarantees
- Vocabulary and interpretation boundaries

It does **not** define:

- Policy, compliance, or enforcement logic
- Decision correctness, fairness, or safety
- Operational dashboards or scoring systems
- Commercial services or opinions

---

## Status

This specification is **active** and reflects the protocol currently operated at:

➡ https://forgerun.ai

The ForgeRun operator publishes commitments and proofs according to this specification, but **no trust in the operator is required** for verification.

---

## Scope and Intent

This repository exists to make the following claims *mechanically falsifiable*:

- That a commitment was included in a public ledger at a specific time
- That historical records have not been altered without detection
- That verification can be performed independently by third parties

The protocol intentionally separates:

> **Evidence production** from **interpretation**

Interpretation, enforcement, audit preparation, and compliance analysis occur *outside* this specification.

---

## Normative Language

The key words **MUST**, **MUST NOT**, **SHOULD**, and **MAY** are to be interpreted as described in RFC 2119.

All language in this repository is intended to describe **observable properties**, not judgments or assurances.

---

## Related Resources

- Protocol overview and documentation: https://forgerun.ai/protocol
- Verification model: https://forgerun.ai/verification-model
- Decision signal schema: https://forgerun.ai/signal-schema
- Deployment patterns: https://forgerun.ai/deployment-patterns

---

## License

License terms for this specification will be published explicitly.  
Until then, this repository is provided for **reference and review only**.

---

## Governance

Changes to this specification are made deliberately and transparently.  
No change to this repository implies endorsement, certification, or approval of any system.

