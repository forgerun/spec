# ForgeRun Protocol Overview

This document provides a high-level overview of the ForgeRun protocol.

ForgeRun is a transparency protocol for recording governance-relevant decisions made by automated systems into public, append-only ledgers. Its purpose is to make specific claims mechanically falsifiable by third parties without requiring trust in the operator.

## Core Claims

The ForgeRun protocol exists to make the following claims verifiable:

- That a specific commitment was included in a public ledger at a specific time
- That historical records have not been altered without detection
- That inclusion and consistency can be verified independently by third parties

## Separation of Concerns

ForgeRun intentionally separates:

- Evidence production  
from  
- Interpretation, enforcement, or judgment

The protocol produces cryptographic evidence. Interpretation of that evidence occurs outside this specification.

## Protocol Scope

Within scope:

- Commitment inclusion
- Ledger append-only properties
- Receipt and proof semantics
- Verification procedures

Out of scope:

- Policy enforcement
- Decision correctness or fairness
- Risk assessment
- Compliance determinations
- Operational dashboards or scoring systems

## Audience

This specification is written for:

- Protocol implementers
- Independent verifiers
- Auditors and researchers
- Tooling authors

It is not intended to provide guidance, recommendations, or assurances.

## Status

This document describes the protocol currently operated at:

https://forgerun.ai
