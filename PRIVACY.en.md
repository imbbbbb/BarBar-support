# BarBar Privacy Policy

Last updated: 2026-09-20

[简体中文](PRIVACY.md) · [繁體中文](PRIVACY.zh-Hant.md) · **English**

The one-line version: **BarBar collects nothing about you, and there is no server
that could collect it.**

The details are below, because BarBar asks the system for two permissions that
sound alarming.

## What BarBar does not do

- No collecting, no uploading, no storing of personal information
- No account, no login, no analytics, no crash reporting, no ads, no third-party SDKs
- Doesn't read your files, clipboard, browsing history or keystrokes
- Doesn't log which apps you use or when

BarBar has no backend. The developer cannot obtain any data about you, because no
data flows anywhere at all.

## What those two permissions are for

### Accessibility

Used to **know what's on the menu bar**.

macOS offers no public API that answers "which icons are on the menu bar right now,
and whose are they". The only way is to enumerate the status items on the system
menu bar through the accessibility interface, reading each icon's owning app bundle
identifier and its position on screen.

Those two things are all BarBar reads. It does not read window contents, does not
read text, does not watch the keyboard, does not synthesise input.

Without this permission, BarBar's icon list is empty.

### Screen Recording

Used to **draw the icons**.

In the "panel below" reveal style, hidden icons have to be redrawn in BarBar's own
panel. Only the system knows what a menu bar icon looks like — many are live
(battery percentage, network speed) and there is no original artwork to fetch — so
the only option is to capture that small rectangle of the menu bar once.

BarBar captures exactly those few dozen by few dozen points of the menu bar. It does
not capture windows, does not record the screen, does not save anything. Captured
bitmaps live in memory only and vanish when the process quits; nothing is written to
disk.

Without this permission, the panel shows each app's own application icon instead —
less faithful, but fully functional.

### Hiding icons needs no permission at all

Worth saying separately: BarBar's core function — hiding icons — goes through the
system's own menu bar visibility mechanism and requires neither permission above.
Both permissions serve only "seeing and recognising" the icons.

You can revoke them at any time in System Settings → Privacy & Security.

## The only outbound connection

BarBar checks once a day for a new version. That request goes to:

- `https://imbbbbb.github.io/BarBar-support/appcast.xml` (update information)
- `https://github.com/imbbbbb/BarBar-support/releases/...` (only downloaded when
  there really is a new version)

The request carries BarBar's version number and your macOS version, used to decide
whether a given release suits you. No identifiers, nothing that could pick you out.

GitHub, as the server, sees your IP address the way it would for any web request.
BarBar has no say in that, and it is no different from any other download.

You can turn the automatic check off under Settings → General → Updates. Once off,
BarBar does not reach out to any network address on its own.

## Where your settings live

Groupings, order and the shortcut are stored in the standard local preferences
(`~/Library/Preferences/com.barbar.app.plist`). They are not synced and not
uploaded. To clean up completely after deleting BarBar, run in Terminal:

```
defaults delete com.barbar.app
```

## Diagnostics export

Settings → About → Export diagnostics writes a text file you can paste into a report.

It is **generated only when you ask for it, shown to you first, and pasted only if
you decide to**. It contains version numbers, hardware model, permission states and
the bundle identifiers of the apps on your menu bar — no window titles, no
screenshots, no file paths containing your username. BarBar never sends it
automatically.

## Changes

If this policy changes, it changes along with a new version and is noted in the
release notes.

## Contact

Questions: open an issue at <https://github.com/imbbbbb/BarBar-support/issues>
