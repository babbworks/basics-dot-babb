---
layout: post
title: "Workpads Is the First BASICS-Conformant Product"
date: 2026-04-29
categories: [community, conformance]
---

[Workpads](https://workpads.org) has achieved Core tier conformance under BASICS v0.1.1. It is the first product to do so, and it is the proof-of-concept that drove the shape of the standard.

This is worth naming directly: BASICS was not written in the abstract. It was extracted from the design decisions, failure modes, and hard constraints encountered while building Workpads for deployment on KaiOS feature phones in emerging markets. The standard is a distillation of what turned out to matter.

## What Workpads Conformance Looks Like

The Workpads conformance evidence package includes:

- A published command contract covering all record operations, sync commands, and export paths
- An event schema for all record mutation events (create, update, delete, conflict, resolution)
- Degraded-mode test output showing create and read operations under offline conditions
- A compatibility policy covering a 24-month backward-compatibility horizon for schema versions
- A degraded-mode matrix covering offline, low-battery, and partial-sync states

This evidence is published alongside the standard at [standard.workpads.org](https://standard.workpads.org).

## Why a Proof Product Matters

A standard without a conformant implementation is a hypothesis. The 100-day governance cycle, the deviation registry, the tier structure — all of these were tested against the reality of building Workpads, not just theorized.

Several rules changed during development. BASICS-SC-011 (durable local ID at creation) was originally scoped to sync-enabled products only; the Workpads implementation revealed that the constraint applies from the moment a record is created, regardless of whether sync is configured. The rule was updated to reflect that.

This is the feedback loop the standard is designed to have. A product builds against it, hits friction, and the friction becomes a proposal. The proposal moves through community review. The standard improves.

## An Invitation

If you are building a tool for constrained or emerging-market deployment, we would like to hear from you. The [Adoption Playbook](https://github.com/babbworks/BASICS-standard/blob/master/ADOPTION.md) is a 30-day track designed to take you from zero to Core tier conformance. The standard is open. The governance process is public. The deviation registry exists precisely so that your constraints can be disclosed without invalidating your conformance claim.

[Start with the Adoption Playbook →](https://github.com/babbworks/BASICS-standard/blob/master/ADOPTION.md)
