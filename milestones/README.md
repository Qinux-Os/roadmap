# Milestones

Each milestone is a separate file. A milestone states what must be true for it
to be complete, not a list of tasks.

## The milestones

| Milestone | State | Summary |
| --- | --- | --- |
| [M1 Foundation](m1-foundation.md) | In progress | A minimal system that boots |
| [M2 Bootable ISO](m2-bootable-iso.md) | Planned | An ISO that can be built reproducibly |
| [M3 Working installer](m3-installer.md) | Planned | Calamares installs a working system |
| [M4 Daily usable](m4-daily-usable.md) | Planned | A normal desktop for daily work |
| [M5 Hardware coverage](m5-hardware.md) | Considering | Broad hardware support |

## What a milestone file contains

- **State**: Done, In progress, Planned, or Considering.
- **Definition of done**: The observable condition that closes it.
- **Out of scope**: What is explicitly not included, to stop scope creep.
- **Blocked by**: Which milestone must finish first.
- **Decisions**: Links to the RFCs that settled its design.

## Dependency chain

```text
M1 Foundation
    |
M2 Bootable ISO
    |
M3 Working installer
    |
M4 Daily usable
    |
M5 Hardware coverage
```

This is strictly sequential. That is deliberate: the cost of reworking the base
system after everything else is built on top of it is far higher than the cost
of waiting.

## Moving a milestone

1. Update the state in the milestone file.
2. Update the table in [`../README.md`](../README.md).
3. Record the reason in the quarter file.
4. If scope changed, say what was added or removed.

One pull request per milestone, so the history reads clearly.
