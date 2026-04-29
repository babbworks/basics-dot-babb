---
layout: page
title: The Standard
eyebrow: BASICS v0.1.1
subtitle: A layered architecture for building business tools that operate under real constraints.
permalink: /standard
wide: true
---

<div class="standard-intro">
  <p>
    BASICS is organized into a <strong>Shared Core</strong> that applies to all conformant products, and three
    <strong>Deployment Profiles</strong> for products that cross software, hardware, or firmware boundaries.
    Conformance is cumulative — profiles inherit and may not weaken Core controls.
  </p>
</div>

## Shared Core

The Shared Core defines obligations that every BASICS-conformant product must satisfy, regardless of deployment tier or hardware target. It establishes the minimum verifiable guarantees that make interoperability and operator confidence possible.

<div class="rule-section">

### Command Surface

Products must publish a machine-readable and human-readable command contract. The contract defines every command the product exposes, its required and optional parameters, its side effects, and its version history.

<ul class="rule-list">
  <li><code class="rule-id">BASICS-SC-001</code> A command contract MUST be published at a stable, versioned URI.</li>
  <li><code class="rule-id">BASICS-SC-002</code> Every command MUST declare its minimum required schema version.</li>
  <li><code class="rule-id">BASICS-SC-003</code> Breaking changes to the command surface MUST increment the major version.</li>
  <li><code class="rule-id">BASICS-SC-004</code> The command contract MUST be machine-parseable (JSON Schema or equivalent).</li>
</ul>

### Record Operations

Core record operations — create, read, update, delete — must function without network connectivity. This is the foundational offline-first guarantee.

<ul class="rule-list">
  <li><code class="rule-id">BASICS-SC-010</code> Create and read operations MUST succeed without network access.</li>
  <li><code class="rule-id">BASICS-SC-011</code> Records MUST be assigned a durable local identifier at creation time, before any sync.</li>
  <li><code class="rule-id">BASICS-SC-012</code> A published event schema MUST describe all record mutation events.</li>
  <li><code class="rule-id">BASICS-SC-013</code> Records MUST carry a schema version field.</li>
</ul>

### Interoperability

Products must declare their interoperability surface — what they can import, export, and exchange — so that integration is predictable and testable.

<ul class="rule-list">
  <li><code class="rule-id">BASICS-SC-020</code> Products MUST publish an interoperability declaration listing supported import/export formats.</li>
  <li><code class="rule-id">BASICS-SC-021</code> Declared formats MUST reference a versioned schema or public specification.</li>
  <li><code class="rule-id">BASICS-SC-022</code> Products MUST publish a compatibility policy stating how long prior versions remain supported.</li>
</ul>

### Versioning and Governance

Artifacts must be versioned, and changes must be traceable.

<ul class="rule-list">
  <li><code class="rule-id">BASICS-SC-030</code> All published artifacts (schemas, contracts, declarations) MUST carry a semver version string.</li>
  <li><code class="rule-id">BASICS-SC-031</code> An ADR (Architecture Decision Record) history MUST be maintained for all breaking changes.</li>
  <li><code class="rule-id">BASICS-SC-032</code> A degraded-mode matrix MUST be published, listing which operations are available at each network/power state.</li>
</ul>

</div>

---

## Software Profile

Applies to products delivered as software (web, mobile, desktop, CLI). Builds on the Shared Core and adds requirements for installation, update paths, and data portability.

<div class="rule-section">

<ul class="rule-list">
  <li><code class="rule-id">BASICS-SW-001</code> The product MUST support installation on devices with ≤ 512 MB RAM without degraded core functionality.</li>
  <li><code class="rule-id">BASICS-SW-002</code> Updates MUST not break existing records without a published migration path.</li>
  <li><code class="rule-id">BASICS-SW-003</code> A full data export in an open format MUST be available without operator intervention.</li>
  <li><code class="rule-id">BASICS-SW-004</code> Minimum supported OS/runtime versions MUST be published and maintained.</li>
</ul>

</div>

---

## Hardware Profile

Applies to products that include or require dedicated hardware (readers, terminals, kiosks, purpose-built devices).

<div class="rule-section">

<ul class="rule-list">
  <li><code class="rule-id">BASICS-HW-001</code> Hardware MUST operate in environments with ambient temperatures of 0–50°C without data loss.</li>
  <li><code class="rule-id">BASICS-HW-002</code> Local record storage MUST persist across power cycles without external sync.</li>
  <li><code class="rule-id">BASICS-HW-003</code> A published bill of materials (BOM) MUST identify all primary components.</li>
  <li><code class="rule-id">BASICS-HW-004</code> Hardware products MUST publish a repair and replacement policy.</li>
</ul>

</div>

---

## Firmware Profile

Applies to products that include programmable embedded firmware.

<div class="rule-section">

<ul class="rule-list">
  <li><code class="rule-id">BASICS-FW-001</code> Firmware MUST support field update without specialized tooling beyond a USB connection or equivalent.</li>
  <li><code class="rule-id">BASICS-FW-002</code> Firmware versions MUST be readable from the device without disassembly.</li>
  <li><code class="rule-id">BASICS-FW-003</code> A signed firmware manifest MUST be published with each release.</li>
  <li><code class="rule-id">BASICS-FW-004</code> Rollback to the prior firmware version MUST be supported.</li>
</ul>

</div>

---

<p style="font-size:0.85rem;color:var(--text-muted)">
  All rule IDs are canonical and referenced in the <a href="https://github.com/babbworks/BASICS-standard/blob/master/standards/rule-index.md">Rule Index</a>.
  Registered deviations use the same IDs via the <a href="https://github.com/babbworks/BASICS-standard/blob/master/standards/deviation-registry.md">Deviation Registry</a>.
  The full normative text lives in the <a href="https://github.com/babbworks/BASICS-standard">BASICS-standard GitHub repository</a>.
</p>
