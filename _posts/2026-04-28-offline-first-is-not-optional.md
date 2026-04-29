---
layout: post
title: "Offline-First Is Not Optional"
date: 2026-04-28
categories: [standard, conformance]
---

BASICS-SC-010 requires that create and read operations succeed without network access. This is not a feature request — it is a foundational design constraint.

The decision to make offline operation a mandatory Core control came directly from the deployment environments BASICS is designed to serve: rural markets, field operations, areas with intermittent or expensive connectivity. In these environments, a tool that requires a network call to create a record is not a business tool — it is a liability.

## What "Offline-First" Actually Requires

Offline-first is often treated as an architecture preference. In BASICS, it is a verifiable obligation. The degraded-mode matrix (BASICS-SC-032) requires products to publish which operations are available at each network and power state. "Create works offline" must be demonstrable, not claimed.

This has implications beyond the obvious. A record created offline needs a durable local identifier before any sync occurs (BASICS-SC-011). That identifier must be assigned deterministically — not generated from a server response, not dependent on a timestamp that may not be accurate offline.

Conflict resolution then becomes a first-class problem, not an edge case. When two records created offline sync against each other, the conflict comparison contract (BASICS-SC-041, Field tier) defines how the product represents that state to the operator. The operator must be able to see it and act on it.

## The Field Tier Exists for This Reason

The Core tier establishes the offline requirement. The Field tier provides the evidence standard: degraded-mode test output, conflict comparison contracts, constrained deployment validation. This is not belt-and-suspenders redundancy — it is a progressive hardening path.

A product that claims Core conformance has made an architectural commitment. A product that claims Field conformance has produced evidence that the commitment holds under pressure. Both claims are testable. That is the point.

## Why This Is Hard and Why It's Worth It

Offline-first design forces decisions that online-first products postpone. Schema versioning becomes critical the moment a user's device is running a version of your app that hasn't synced in three weeks. Data portability becomes critical the moment the operator needs to move records off a device before it's replaced.

These are not hypothetical problems in the deployment environments BASICS is designed for. They are routine. Building for them from the start is not a burden — it is the cost of operating in the real world.
