# M3: Working installer

**State:** Planned

Calamares installs Qinux to disk from the ISO, and the result boots.

## Definition of done

- The installer runs from the live ISO.
- Manual partitioning, alongside guided partitioning, works.
- A user account, locale and keyboard layout are created.
- The installed system boots on its own, without the ISO.
- Encryption, when selected, works and the system prompts at boot.
- The installer can be themed with Qinux branding.

## In scope

- `calamares-config`: module selection and ordering.
- `installer-modules`: partitioning, locale and user modules.
- Branding: logos, colours and the slideshow.
- Post-install scripts that enable the display manager and configure the
  bootloader.

## Out of scope

- Automated partitioning on non-standard layouts.
- Network installers.
- Upgrading an existing installation from the installer.

## Blocked by

[M2 Bootable ISO](m2-bootable-iso.md)

## Decisions

- Calamares rather than a custom installer. Writing an installer is not the
  problem worth solving here.
- Custom modules only where Calamares cannot be configured to fit.

## Risk

Calamares is C++ with its own build system. Custom modules add packaging work
and are the most likely source of schedule slip in this milestone.

## When it closes

When a user boots the ISO on a machine with no operating system, installs
Qinux, reboots, and logs in to a working desktop.
