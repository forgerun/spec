# ForgeRun Definitions

This document defines the **normative vocabulary** used throughout the ForgeRun specification.

The purpose of these definitions is to ensure that all terms have **stable, unambiguous meaning** across implementations, audits, and third-party analysis.

Unless otherwise stated, all definitions apply globally to the ForgeRun protocol.

---

## Operator

An **Operator** is an entity that runs a system which emits commitments and receipts according to the ForgeRun specification.

An Operator:
- MAY be a company, individual, or automated system
- MAY publish commitments to one or more public ledgers
- MUST NOT be trusted for verification correctness

Verification of ForgeRun records MUST NOT depend on trust in the Operator.

---

## Commitment

A **Commitment** is a cryptographic statement asserting that a specific input or decision artifact existed at or before a particular point in time.

A Commitment:
- MUST be immutable once published
- MUST be addressable by a stable identifier
- MUST be verifiable independently of the Operator
- MUST NOT be altered, revoked, or overwritten

A Commitment does not assert correctness, quality, or compliance — only inclusion.

---

## Receipt

A **Receipt** is a verifiable proof that a Commitment was included in a specific public ledger.

A Receipt:
- MUST bind a Commitment to a ledger and time reference
- MUST be independently verifiable
- MAY be generated synchronously or asynchronously
- MUST remain valid even if the Operator ceases operation

---

## Ledger

A **Ledger** is an append-only data structure used to record Commitments.

A Ledger:
- MUST provide tamper-evident history
- MUST allow third-party verification
- MAY be blockchain-based or non-blockchain-based
- MUST NOT allow deletion or mutation of prior entries

ForgeRun does not mandate a specific ledger technology.

---

## Verification

**Verification** is the process by which a third party independently confirms that a Commitment was included in a Ledger as claimed.

Verification:
- MUST be possible without Operator cooperation
- MUST rely only on public data
- MUST be reproducible by independent parties
- MUST NOT require trust assumptions

Verification determines *whether something happened*, not *whether it was correct*.

---

## Evidence

**Evidence** refers to artifacts produced by the ForgeRun protocol that demonstrate historical inclusion.

Evidence:
- Includes Commitments and Receipts
- Is factual and observable
- Does not imply interpretation or judgment

Evidence is intentionally separated from analysis, compliance, and enforcement.

---

## Interpretation

**Interpretation** is any semantic, legal, ethical, or operational analysis applied to Evidence.

Interpretation:
- Occurs outside the ForgeRun protocol
- MAY vary across jurisdictions or institutions
- MUST NOT be embedded into protocol semantics

ForgeRun produces Evidence, not conclusions.

---

## Specification

The **Specification** is the canonical definition of ForgeRun protocol behavior as published in this repository.

The Specification:
- Defines observable properties only
- Uses normative language (MUST, MUST NOT, SHOULD, MAY)
- Does not encode policy, enforcement, or opinion

---

## Trust

**Trust** refers to reliance on an actor’s honesty, intent, or correctness.

The ForgeRun protocol is explicitly designed to:
- Minimize trust assumptions
- Enable verification without trust
- Avoid trust-based guarantees

Trust is neither required nor provided by the protocol.

---

## Out of Scope

The following are explicitly **out of scope** for ForgeRun:

- Policy enforcement
- Compliance determinations
- Correctness or fairness judgments
- Safety assessments
- Certification or endorsement
- Dispute resolution

These activities may consume ForgeRun Evidence, but are not part of the protocol.

---
