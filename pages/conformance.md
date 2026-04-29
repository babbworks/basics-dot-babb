---
layout: page
title: Conformance
eyebrow: BASICS Conformance Model
subtitle: Verifiable state, not narrative. Pass/fail mandatory controls plus a maturity score for optional hardening.
permalink: /conformance
---

Conformance to BASICS is intentional and progressive. The three tiers — **Core**, **Field**, and **Industrial** — inherit cumulatively. A product at the Field tier must satisfy all Core controls; Industrial must satisfy all Field and Core controls.

Tier claims must be backed by published, auditable evidence. Self-attestation is permitted at Core and Field tiers. Industrial tier requires Babb review or a delegated partner review.

---

## Scoring Model

**Mandatory controls** are pass/fail. A single failing mandatory control prevents tier claim at that level.

**Optional controls** use a 0–3 maturity score:
- **0** — Not addressed
- **1** — Partially addressed, no evidence
- **2** — Addressed with internal evidence
- **3** — Addressed with published, externally verifiable evidence

---

## Core Tier Checklist

<div class="checklist-section">

### Command Surface

| ID | Control | Type |
|---|---|---|
| BASICS-SC-001 | Command contract published at stable versioned URI | Mandatory |
| BASICS-SC-002 | Every command declares minimum schema version | Mandatory |
| BASICS-SC-003 | Breaking changes increment major version | Mandatory |
| BASICS-SC-004 | Command contract is machine-parseable | Mandatory |

### Record Operations

| ID | Control | Type |
|---|---|---|
| BASICS-SC-010 | Create and read without network access | Mandatory |
| BASICS-SC-011 | Durable local ID assigned at creation | Mandatory |
| BASICS-SC-012 | Published event schema for record mutations | Mandatory |
| BASICS-SC-013 | Records carry schema version field | Mandatory |

### Interoperability

| ID | Control | Type |
|---|---|---|
| BASICS-SC-020 | Interoperability declaration published | Mandatory |
| BASICS-SC-021 | Declared formats reference versioned spec | Mandatory |
| BASICS-SC-022 | Compatibility policy published | Mandatory |

### Versioning

| ID | Control | Type |
|---|---|---|
| BASICS-SC-030 | All artifacts carry semver version | Mandatory |
| BASICS-SC-031 | ADR history maintained for breaking changes | Mandatory |
| BASICS-SC-032 | Degraded-mode matrix published | Mandatory |

</div>

---

## Field Tier Checklist

All Core controls, plus:

<div class="checklist-section">

| ID | Control | Type |
|---|---|---|
| BASICS-SC-040 | Degraded-mode test evidence published | Mandatory |
| BASICS-SC-041 | Conflict comparison contract published | Mandatory |
| BASICS-SC-042 | Sync and conflict status surface exposed to operator | Mandatory |
| BASICS-SC-043 | Constrained deployment validated (≤ 512 MB RAM or equivalent field target) | Mandatory |
| BASICS-SC-044 | Offline operation validated by automated test output | Mandatory |

</div>

---

## Industrial Tier Checklist

All Field controls, plus:

<div class="checklist-section">

| ID | Control | Type |
|---|---|---|
| BASICS-SC-050 | Security lifecycle evidence published (CVE response process, patch SLA) | Mandatory |
| BASICS-SC-051 | Software Bill of Materials (SBOM) published | Mandatory |
| BASICS-SC-052 | Publishable conformance results (full checklist outputs) | Mandatory |
| BASICS-SC-053 | Babb or delegated partner review completed | Mandatory |

</div>

---

## Registering a Deviation

Products may register formal deviations from mandatory controls using the Deviation Registry. A registered deviation must:

1. Reference the specific rule ID being deviated
2. State the rationale
3. Propose an equivalent or compensating control
4. Carry a durable deviation identifier (format: `DEV-[YYYY]-[NNN]`)

Deviations are not approvals — they are transparent disclosures. Babb may flag deviations as accepted, under review, or rejected in the public registry.

<p style="margin-top:2rem">
  <a href="https://github.com/babbworks/BASICS-standard/blob/master/standards/deviation-registry.md" class="btn btn-primary">View Deviation Registry</a>
  <a href="/participate" class="btn btn-secondary" style="margin-left:0.75rem">Submit a Deviation</a>
</p>
