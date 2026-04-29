---
layout: post
title: "Why a Commitments Framework, Not a Specification"
date: 2026-04-27
categories: [standard, governance]
---

Most technical standards are specifications — they describe *what* a product should do. BASICS is something different. It is a commitments framework: a set of obligations that products make to operators, integrators, and each other.

The distinction matters. A specification tells you what to build. A commitments framework tells you what you're promising — and what the other party can hold you to.

## The Problem with Specification-Only Standards

When a standard is purely a specification, there is no clear answer to the question: *what happens if you don't follow it?* The standard describes a behavior; the product either implements it or doesn't; interoperability breaks or doesn't. The feedback loop is indirect and slow.

This is especially painful in constrained deployments. When a product fails in the field — drops a record during a sync conflict, loses data after a power cycle, becomes incompatible after an update — the downstream effects are real and often irreversible. A farmer's stock record doesn't come back. An inventory adjustment that didn't make it through isn't recoverable from a vague specification.

## Testable Obligations

BASICS requires that conformance be verifiable. Every mandatory control has a corresponding evidence artifact:

- A command contract (not just "commands are documented")
- A degraded-mode matrix (not just "offline is supported")
- Test output for constrained deployment (not just "we tested it")

This shifts the question from *did you implement the spec?* to *can you show me the evidence?* That shift is the difference between a claim and a commitment.

## What This Means for Product Teams

Implementing BASICS is not a compliance exercise. It is a forcing function for decisions that most product teams delay until they're expensive: how do we handle schema changes? What happens during a conflict? What is our compatibility horizon?

The 100-day proposal cycle and the deviation registry exist because we know real products have constraints that a standard written in the abstract cannot anticipate. The goal is not perfect adherence — it is transparent, documented, auditable behavior.

A product that registers a deviation and explains its compensating control is more trustworthy, not less. That's the commitments model working as intended.
