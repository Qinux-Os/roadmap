# M2: Bootable ISO

**State:** Planned

A Qinux ISO that can be built from source and booted, containing the live
environment.

## Definition of done

- `iso` produces a bootable ISO from a clean checkout.
- The build is reproducible: two builds from the same tag produce identical
  checksums.
- The ISO boots on UEFI and BIOS.
- The live session reaches a KDE Plasma desktop.
- The ISO boots in a virtual machine without hardware-specific work.

## In scope

- Build profiles: at minimum `kde` and `minimal`.
- The live overlay and autologin configuration.
- Automated ISO builds in CI.
- Checksum generation and release signing.

## Out of scope

- The graphical installer. That is M3.
- Multiple desktop profiles beyond the two above.
- Fancy bootloader theming. A working boot comes first.

## Blocked by

[M1 Foundation](m1-foundation.md)

## Decisions

- Live session uses an overlay rather than a copy, so the ISO stays small.
- Reproducibility is a requirement, not a goal. A non-reproducible ISO cannot
  be signed meaningfully.

## Risk

Reproducible ISO builds conflict with some tooling that embeds timestamps.
Those tools need replacing or patching early, not at the end.

## When it closes

When `qinux-cli iso build` produces a bootable image on two different machines
with identical checksums.
