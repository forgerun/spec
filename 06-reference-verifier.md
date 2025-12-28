# 06 — Reference Verifier (Read-Only)

The reference verifier exists so third parties can independently validate **mechanical, falsifiable** properties of ForgeRun evidence (structure, cryptography, inclusion, timestamps) **without trusting the operator**.

---

## Reference Verifier Boundary (Normative)

This document defines a *reference verification interface* only.

The reference verifier:

- MUST be read-only
- MUST NOT generate, modify, or submit commitments
- MUST NOT publish to any ledger
- MUST NOT interpret semantic meaning, intent, policy compliance, fairness, safety, or correctness
- MUST NOT issue certifications, approvals, endorsements, ratings, or recommendations
- MUST NOT provide dispute resolution

The verifier performs only mechanical checks of:

- Structural validity (schema / required fields)
- Cryptographic integrity (hashes / signatures)
- Inclusion proofs (membership in an append-only ledger)
- Timestamp consistency (e.g., RFC3339 parsing; optional external time proofs)

Any interpretation of verification results occurs outside this specification.

---

## Non-Normative CLI Interface (Illustrative)

The command-line interface described below is illustrative and non-normative. It is an example of how an implementation **MAY** expose the verification checks defined by this specification.

### Commands

```bash
forgerun-verify <command> [options]

# Verify a commitment’s structure + cryptographic integrity (no publishing)
forgerun-verify verify commitment \
  --commitment <path|stdin> \
  [--schema <path>] \
  [--output json|text]

# Verify a receipt against a commitment (structure + cryptographic binding)
forgerun-verify verify receipt \
  --receipt <path|stdin> \
  --commitment <path|stdin> \
  [--output json|text]

# Verify inclusion proof of a commitment hash in an append-only ledger
forgerun-verify verify inclusion \
  --commitment-hash <hex> \
  --ledger <url|path> \
  --proof <path|stdin> \
  [--time <rfc3339>] \
  [--output json|text]

# Perform a full mechanical verification bundle (still read-only)
forgerun-verify verify full \
  --commitment <path|stdin> \
  --receipt <path|stdin> \
  --ledger <url|path> \
  --proof <path|stdin> \
  [--schema <path>] \
  [--output json|text]
