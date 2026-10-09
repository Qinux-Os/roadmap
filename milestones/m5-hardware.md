# M5: Hardware coverage

**State:** Considering

Broad hardware support, so Qinux works on the machine people actually own.

**This milestone is not committed.** It is listed because it is the most
requested category of work, and because postponing it indefinitely would make
Qinux unusable for most people.

## Definition of done

- Automatic detection of common hardware.
- Correct driver selection for common GPUs, network cards and audio devices.
- Documented manual overrides for hardware that is detected wrongly.
- A bug report template that produces enough information to act on.

## In scope

- Hardware detection and per-device defaults.
- A driver and device database.
- The `qinux-hardware` utility.
- Per-form-factor configuration (laptop, desktop, server).

## Out of scope

- Certification for hardware we do not own.
- Enterprise fleet management.

## Blocked by

[M4 Daily usable](m4-daily-usable.md)

## Open questions

- Maintain a driver database ourselves, or rely on `pci.ids` and the kernel's
  own module aliases?
- How much upstream do we contribute hardware fixes back to?

## When it closes

Not scheduled. Open an issue if you have hardware that does not work, even if
you cannot contribute a fix. Those reports set the priority order.
