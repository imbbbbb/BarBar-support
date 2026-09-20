<div align="center">

<img src="icon.png" width="128" alt="BarBar">

# BarBar

**Tidy up your menu bar.**

[Download the latest release](https://github.com/imbbbbb/BarBar-support/releases/latest) ·
[Report an issue](https://github.com/imbbbbb/BarBar-support/issues/new/choose)

[简体中文](README.md) · [繁體中文](README.zh-Hant.md) · **English**

<a href="https://ko-fi.com/P4W31ZZFU0">
  <img src="https://img.shields.io/badge/Support%20me%20on%20Ko--fi-72a4f2?style=for-the-badge&logo=ko-fi&logoColor=white" alt="Support me on Ko-fi" height="38">
</a>

</div>

---

Menu bar icons pile up, and by the time the bar is full the one you actually want
is the one you can't see. BarBar lets you decide which icons stay out and which
get tucked away; the tucked-away ones come back with one click on the arrow.

Written natively. Hiding icons needs neither Accessibility nor Screen Recording.

## Two things

**One — pick your icons.** In Settings, choose what stays visible and what gets hidden.

**Two — reveal them.** Click the arrow on the menu bar, or press
<kbd>⌥</kbd><kbd>⌘</kbd><kbd>B</kbd>. Two reveal styles, your call:

- **In the menu bar** — hidden icons spread back out along the menu bar itself;
- **In a panel below** — a small panel drops below the menu bar with the icons in it.

## Install

1. Download the dmg from [Releases](https://github.com/imbbbbb/BarBar-support/releases/latest);
2. Open it and drag BarBar into **Applications**;
3. **Close the dmg window and launch BarBar from Applications**;
4. The first time, right-click the app → **Open**, then click **Open** again in the
   dialog. After that a normal double-click works.

> [!IMPORTANT]
> **Do not run BarBar straight from the dmg window.**
>
> Apps downloaded through a browser carry the quarantine flag, and macOS runs them
> from a temporary read-only location instead (App Translocation). From there the
> system doesn't recognise BarBar's identity and hiding silently breaks — version
> 0.1 would hide its own arrow along with everything else, leaving an empty menu bar.
>
> Since 0.1.1 BarBar detects this, refuses to hide anything and asks you to install
> it properly, but **the right move is always to drag it into Applications first**.

Requires **macOS 27 or later**. Hiding menu bar icons relies on a system mechanism
introduced in macOS 27; it cannot be done on earlier versions.

<details>
<summary>Why the right-click?</summary>

BarBar is not yet signed with an Apple Developer ID or notarised, so macOS stops it
on first launch. Right-click → Open is the official route Apple leaves open for
un-notarised software — it isn't a security bypass; you are still explicitly
authorising this one app.

If a double-click gets you "damaged and should be moved to the Trash", that's the
quarantine attribute. One line in Terminal clears it:

```
xattr -dr com.apple.quarantine /Applications/BarBar.app
```

</details>

On first launch BarBar asks for **Accessibility** — that's how it reads which icons
are on the menu bar. Hiding itself needs no permission at all. The "panel below"
style additionally wants **Screen Recording** to draw the icons as they really look;
without it BarBar still works, the panel just shows names instead.

BarBar collects nothing and has no server. Exactly what those two permissions are
for, and what the once-a-day update check actually sends, is spelled out in the
[Privacy Policy](PRIVACY.en.md).

## If the arrow disappears

Press <kbd>⌥</kbd><kbd>⌘</kbd><kbd>B</kbd>. When the arrow isn't on the menu bar,
that shortcut brings it back and opens Settings.

The usual cause: while <kbd>⌘</kbd>-dragging, you let go outside the menu bar —
macOS reads that as "the user doesn't want this item" and remembers the decision
indefinitely. Since 0.1.1 BarBar restores it on every launch.

## What it can't do yet

Stated plainly, so you don't spend an afternoon trying:

- **BarBar can't control where the arrow sits or how visible icons are ordered.**
  The system offers no ordering API. To rearrange, hold <kbd>⌘</kbd> and drag
  directly on the menu bar — that's a macOS feature. Just don't let go outside the
  menu bar, or the icon vanishes.
- **Hiding works per app, not per icon.** If one app puts several icons up there,
  they hide and show together.
- A few icons the system refuses to hide at all; BarBar marks those in Settings.

## Feedback

That's what this repository is for. Problems, feature requests — open an
[Issue](https://github.com/imbbbbb/BarBar-support/issues/new/choose).

For bug reports, please include your macOS version, your BarBar version, and which
app's icon misbehaved.

## Support development

BarBar is free today, with no promise that it stays free forever. If it made your
menu bar liveable, you can buy me a coffee.

<a href="https://ko-fi.com/P4W31ZZFU0">
  <img src="https://img.shields.io/badge/Support%20me%20on%20Ko--fi-72a4f2?style=for-the-badge&logo=ko-fi&logoColor=white" alt="Support me on Ko-fi" height="38">
</a>

Not supporting is completely fine too — an issue telling me what's awkward to use
is worth just as much.

## About the source

BarBar is closed source. This repository only handles distribution and feedback; it
contains no source code.

It was written from scratch and reuses no code from any existing project.
