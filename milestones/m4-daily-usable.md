# M4: Daily usable

**State:** Planned

A complete desktop system that a person can use every day without reaching for
another distribution.

## Definition of done

- KDE Plasma starts to a working desktop with Qinux defaults.
- Sound, networking, Bluetooth, suspend and resume work on a reference machine.
- A full update completes and reboots cleanly, twice in a row.
- An update that breaks the system can be rolled back.
- The first-run welcome application completes.
- `qinux-settings` configures the documented settings.
- Common hardware works: laptop, desktop, external monitors, common GPUs.

## In scope

- KDE, Plasma and KWin integration.
- Icons, theme, cursor, fonts, wallpapers, SDDM and Plymouth themes.
- The Qinux utilities: settings, welcome, update, hardware, system.
- Update rollback via automatic snapshots.
- Default application selection.

## Out of scope

- Every piece of software anyone might want. This is a default set, not a
  full catalogue.
- Enterprise deployment tooling.
- Multi-seat support.

## Blocked by

[M3 Working installer](m3-installer.md)

## Decisions

- Visual assets inherit from upstream (Breeze, Adwaita, Papirus) and are
  recoloured. Drawing an icon set from scratch is a multi-year commitment that
  this project cannot make.
- Fonts are an existing OFL family. A custom typeface is out of scope.

## Risk

The Qinux utilities are five separate applications. They are the largest piece
of original code in the project and the most likely to slip.

## When it closes

When three people use a daily build for two weeks each without falling back to
another distribution.
