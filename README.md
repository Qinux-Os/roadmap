# Roadmap

What Qinux is building, in what order, and why.

## How to read this

Dates are targets, not promises. When a milestone slips it is moved and the
reason is recorded, rather than the date being quietly revised.

| Symbol | Meaning |
| --- | --- |
| Done | Shipped and released |
| In progress | Actively being worked on |
| Planned | Committed, not started |
| Considering | Discussed, not committed |

If something is marked **Considering**, it may never happen. Open an issue
before planning around it.

## Current focus

The critical path runs through the first bootable ISO. Until `iso` produces an
image that installs and boots, every other component is an assumption. Work is
ordered accordingly.

See [`milestones/`](milestones/) for the milestone definitions and
[`quarters/`](quarters/) for the per-quarter plans.

## Milestones

| Milestone | State | Depends on |
| --- | --- | --- |
| [M1 Foundation](milestones/m1-foundation.md) | In progress | Nothing |
| [M2 Bootable ISO](milestones/m2-bootable-iso.md) | Planned | M1 |
| [M3 Working installer](milestones/m3-installer.md) | Planned | M2 |
| [M4 Daily usable](milestones/m4-daily-usable.md) | Planned | M3 |
| [M5 Hardware coverage](milestones/m5-hardware.md) | Considering | M4 |

## Status legend

The full table with owners and dates lives in
[`milestones/`](milestones/).

## Changing the roadmap

Roadmap changes go through the same process as code:

1. Open an issue in [`community`][community] describing the change.
2. Discuss it at a community call.
3. Update the relevant file in a pull request.

Dates are not changed in a pull request that also changes scope. Do one or the
other, so the history shows what actually happened.

[community]: https://github.com/Qinux-Os/community

## Relationship to RFCs

The roadmap says **what** happens and roughly **when**. An
[RFC](https://github.com/Qinux-Os/rfcs) says **how**, and is required before
work starts on anything architectural.

A milestone marked complete should have its design decisions on record as
accepted RFCs.

## Previous quarters

- [`quarters/2026-q1.md`](quarters/2026-q1.md)

## Proposals

Changes that have been suggested but not yet agreed live in
[`proposals/`](proposals/). A proposal becomes a milestone once it is accepted
at a community call.
