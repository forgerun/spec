# Commitments

This document defines the structure, semantics, and invariants of **commitments** in the ForgeRun protocol.

A commitment is a cryptographic record asserting that a specific decision, event, or state transition occurred and was included in a public, append-only ledger at a specific time.

ForgeRun commitments are **descriptive**, not evaluative. They assert *that something happened*, not *whether it was correct, compliant, or desirable*.

---

## Definition

A **commitment** is an immutable record containing:

- A cryptographic hash of a decision or event
- A timestamp or ordering reference
- A reference to the protocol version
- Optional structured metadata
- A signature or proof of inclusion

Once published, a commitment **MUST NOT** be altered or removed.

---

## Commitment Invariants

All valid ForgeRun commitments MUST satisfy the following invariants:

1. **Immutability**  
   Once published, the commitment cannot be modified without detection.

2. **Public Verifiability**  
   Any third party can independently verify the commitment using publicly available data.

3. **Order Preservation**  
   Commitments are totally or partially ordered according to the underlying ledger semantics.

4. **Content Addressability**  
   The commitment identifier is derived from its contents.

5. **Protocol Transparency**  
   The method of commitment generation is publicly specified.

---

## Commitment Structure (Logical)

A commitment logically consists of:

- `commitment_id` — content-derived identifier
- `subject_hash` — hash of the decision, artifact, or event
- `schema_ref` — reference to the applicable signal or decision schema
- `protocol_version` — ForgeRun protocol version
- `timestamp` — logical or physical ordering value
- `metadata` (optional) — structured, non-normative context

This specification does **not** mandate a specific serialization format.

---

## Commitment Creation

A ForgeRun operator MAY generate commitments for:

- Automated system decisions
- AI model outputs
- Policy-relevant events
- State transitions
- External attestations (when explicitly marked)

Commitment generation MUST be deterministic with respect to the committed content.

---

## What Commitments Do Not Assert

A commitment does **not** assert:

- Correctness of the decision
- Compliance with law or policy
- Fairness, safety, or
