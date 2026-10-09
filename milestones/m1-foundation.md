# M1: Foundation

**State:** In progress

A minimal Qinux system that boots on real hardware and reaches a login prompt.

## Definition of done

- A configured kernel boots to an initramfs and mounts root.
- The system reaches a text login prompt on both UEFI and BIOS systems.
- The base package set installs from the local repository.
- `base`, `filesystem`, `system` and `initramfs` configurations are in place.
- A snapshot can be taken and restored.

## In scope

- Kernel configuration and any patches required to boot.
- `mkinitcpio` profiles for the supported layouts.
- GRUB and systemd-boot configuration, plus the EFI stub.
- Base filesystem layout and `fstab`.
- Core systemd units, sysctl and journald settings.
- A package repository containing only the base set.

## Out of scope

- Any desktop environment.
- The graphical installer.
- Hardware enablement beyond the machine used for testing.
- The Qinux utilities.

## Blocked by

Nothing. This is where the work starts.

## Decisions

- Package format follows pacman. See the accepted RFC on packaging.

## Risk

If the kernel does not boot on real hardware, everything after this milestone
is guesswork. Budget for testing on several machines, not just the build host.

## When it closes

When a fresh machine boots the built system and reaches a login prompt without
manual intervention.
