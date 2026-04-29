---
layout: page
title: Governance
eyebrow: BASICS Governance Process
subtitle: The standard evolves through a 100-day proposal-to-ratification cycle with community input at every stage.
permalink: /governance
---

BASICS is governed by Babb as the founding steward, with the explicit goal of transitioning to a multi-steward model as the conformant product ecosystem grows. All governance activity is conducted publicly via the BASICS-standard GitHub repository.

---

## The 100-Day Cycle

Proposals move through four stages. The timeline is a target, not a hard cutoff — a proposal moves forward when its stage criteria are met, not when a clock expires.

<div class="gov-timeline">

  <div class="gov-stage">
    <div class="stage-marker">Days 1–20</div>
    <div class="stage-body">
      <h3>Draft</h3>
      <p>
        The proposer submits a GitHub Issue using the proposal template. The draft must include:
        the rule IDs affected (or new IDs requested), the rationale, a proposed normative statement,
        and any known implementation implications.
      </p>
      <p>
        During the Draft stage, anyone may comment. Babb triages within 10 business days and
        assigns a proposal ID (<code>PROP-[YYYY]-[NNN]</code>).
      </p>
    </div>
  </div>

  <div class="gov-stage">
    <div class="stage-marker">Days 21–60</div>
    <div class="stage-body">
      <h3>Trial Implementation</h3>
      <p>
        One or more products implement the proposed change on a trial basis and publish results.
        Trial implementations must document: what was implemented, what evidence was produced,
        and any friction encountered.
      </p>
      <p>
        Babb or a designated reviewer may request clarifications. The proposal author is responsible
        for incorporating feedback into a revised draft by the end of this period.
      </p>
    </div>
  </div>

  <div class="gov-stage">
    <div class="stage-marker">Days 61–90</div>
    <div class="stage-body">
      <h3>Community Review</h3>
      <p>
        The revised draft and trial results are posted for community review. A 30-day comment
        period opens. All comments are logged and must receive a disposition (accepted, rejected,
        or deferred with rationale).
      </p>
      <p>
        At the close of the comment period, Babb produces a disposition report summarizing
        all feedback and the proposed final text.
      </p>
    </div>
  </div>

  <div class="gov-stage">
    <div class="stage-marker">Days 91–100</div>
    <div class="stage-body">
      <h3>Ratification Decision</h3>
      <p>
        Babb issues a ratification decision: <strong>Accepted</strong>, <strong>Accepted with modifications</strong>,
        <strong>Deferred</strong> (returned to draft with specific conditions), or <strong>Rejected</strong>.
      </p>
      <p>
        Accepted proposals are merged into the standard with a new version increment.
        The proposal ID is recorded in the ADR history alongside the affected rule IDs.
      </p>
    </div>
  </div>

</div>

---

## Stewardship

**Current steward:** Babb (basics@babb.tel)

Babb holds binding ratification authority until a formal stewardship transition is completed. A transition requires:

- At least three independent conformant products at Field tier or above
- A stewardship council with published operating rules
- A 180-day overlap period during which Babb retains veto authority

The stewardship model is itself subject to the proposal process — any party may propose changes to governance via the standard GitHub repository.

---

## Accelerated Track

Proposals that address critical security vulnerabilities or interoperability-breaking behaviors may be escalated to an accelerated track. The accelerated track compresses the cycle to 30 days and bypasses the Trial Implementation stage, with the understanding that implementations will follow ratification rather than precede it.

Accelerated track use requires Babb approval at the time of proposal triage.

---

<p style="font-size:0.85rem;color:var(--text-muted)">
  All proposals and their dispositions are tracked in the
  <a href="https://github.com/babbworks/BASICS-standard/issues">BASICS-standard GitHub Issues</a>.
  Ratified changes are recorded in the
  <a href="https://github.com/babbworks/BASICS-standard">standard repository</a>.
</p>
