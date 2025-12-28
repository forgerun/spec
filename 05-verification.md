# Verification

This document defines the **verification model** used in the ForgeRun protocol.

Verification determines whether specific **claims about commitments and receipts** can be independently checked using observable evidence.

Verification does **not** determine correctness, quality, compliance, or intent.

---

## Definition

**Verification** is the process of evaluating whether one or more claims about:

- Commitments
- Receipts
- Their relationships
- Their ordering or inclusion

can be substantiated using publicly observable data.

---

## Verifiable Claims

The ForgeRun protocol supports verification of claims such as:

- A commitment was included in a public ledger
- A commitment existed at or before a specific time
- A receipt references a valid commitment
- Records have not been altered since publication
- Observations were made independently

Claims outside this scope are **non-verifiable by this protocol**.

---

## Verification Properties

All verification MUST be:

1. **Trust-Minimized**  
   Verification does not require trusting the ForgeRun operator or receipt issuer.

2. **Mechanically Reproducible**  
   Independent parties can repeat verification using the same inputs.

3. **Evidence-Bound**  
   Verification relies only on observable commitments and receipts.

4. **Non-Interpretive**  
   Verification does not evaluate meaning, correctness, or desirability.

---

## Verification Inputs

Verification MAY consume:

- Commitment identifiers
- Receipt identifiers
- Ledger inclusion proofs
- Cryptographic hashes
- Timestamp or ordering evidence

This specification does **not** mandate a specific cryptographic primitive.

---

## Verification Outcomes

Verification produces **binary or factual outcomes**, such as:

- Verified / Not Verified
- Included / Not Included
- Match / Mismatch
- Consistent / Inconsistent

Verification outcomes are **not scores, grades, or ratings**.

---

## Failure Conditions

Verification MAY fail if:

- Required evidence is unavailable
- Inputs are malformed
- Records are missing or unresolved
- Integrity checks do not pass

Failed verification MUST remain observable.

---

## Separation from Compliance and Audit

Verification is **not**:

- Compliance determination
- Audit conclusion
- Risk assessment
- Certification
- Enforcement action

These activities MAY consume verification outputs, but occur **outside this protocol**.

---

## Extensibility

Multiple verification models MAY coexist, provided they:

- Respect commitment and receipt semantics
- Do not reinterpret protocol vocabulary
- Do not assert authority or judgment

---

## Status

This document is **normative**.

Any system claiming ForgeRun compatibility MUST NOT represent verification as approval, certification, or endorsement.
