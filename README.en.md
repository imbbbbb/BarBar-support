<div align="center">

<img src="icon.png" width="128" alt="BarBar">

# BarBar

**Keep your Mac menu bar clean.**

[Download Latest Release](https://github.com/imbbbbb/BarBar-support/releases/latest) ·
[Report an Issue](https://github.com/imbbbbb/BarBar-support/issues/new/choose) ·
[Privacy Policy](PRIVACY.en.md)

[简体中文](README.md) · [繁體中文](README.zh-Hant.md) · **English**

<a href="https://ko-fi.com/P4W31ZZFU0">
  <img src="https://img.shields.io/badge/Support%20me%20on%20Ko--fi-72a4f2?style=for-the-badge&logo=ko-fi&logoColor=white" alt="Support me on Ko-fi" height="36">
</a>

</div>

---

Menu bar icons pile up fast until the one you actually need gets pushed out of sight. **BarBar** is a native menu bar organizer built for macOS 27 — tuck away the icons you rarely touch, and bring them back with a click or a quick hover.

## How It Works

**1. Drag into groups**

Open Settings and drag each app into one of three groups:

- **Always visible** — stays on the menu bar.
- **Hidden** — tucked away until you reveal it.
- **Always hidden** — completely removed from the menu bar (drag it back and restart that app to restore).

**2. Reveal your way**

Click BarBar's icon, turn on **Hover to reveal**, or press the global shortcut (default <kbd>⌥</kbd><kbd>⌘</kbd><kbd>B</kbd>). Choose between two reveal styles:

- **In a panel below** — a native glass panel drops beneath the menu bar with full support for left-click, right-click menus, and direct drag-to-reorder.
- **In the menu bar** — icons expand right along the menu bar itself, with optional auto-collapse once your pointer leaves.

Pick from 4 control icon styles (Chevron, Bar, Dot, Ellipsis). BarBar never captures your screen in the background and collects zero data — see the [Privacy Policy](PRIVACY.en.md).

## Installation

Requires **macOS 27 or later**.

1. Download the latest [DMG](https://github.com/imbbbbb/BarBar-support/releases/latest) and drag **BarBar** into **Applications** (do not launch it straight from the DMG window);
2. On first launch, **right-click BarBar in Applications → Open**. After that, open it normally;
3. Grant **Accessibility** when prompted so BarBar can see which icons are on your menu bar (**Screen Recording** is optional and not required for daily use).

<details>
<summary>Seeing “damaged and should be moved to the Trash”?</summary>

Because BarBar is not notarized with a paid Apple Developer ID yet, macOS Gatekeeper may block downloaded copies. Run this command in Terminal to clear the quarantine flag:

```bash
xattr -dr com.apple.quarantine /Applications/BarBar.app
```

</details>

## FAQ & System Limits

- **Lost BarBar's icon?** Press <kbd>⌥</kbd><kbd>⌘</kbd><kbd>B</kbd> to bring it right back and open Settings. To rearrange visible icons on the menu bar, hold <kbd>⌘</kbd> and drag them directly (avoid dropping outside the menu bar).
- **Notification Center won't open when clicking the clock?** While the **Hidden** group contains icons, the macOS visibility mechanism temporarily disables Notification Center. Using only **Always visible** and **Always hidden** avoids this ([#4](https://github.com/imbbbbb/BarBar-support/issues/4)).
- **An app's icon disappears even though it's set to Always visible?** Make sure that app is installed inside `/Applications`. macOS automatically hides menu bar items belonging to apps launched from other folders while hiding is active.
- **What about system icons?** Input Sources, Spotlight, and Siri can be grouped directly in BarBar. Core items like Clock, Wi-Fi, and Control Center can be toggled in **System Settings → Menu Bar**.
- **Apps with multiple menu bar icons?** macOS controls visibility per app, so multiple icons from the same app hide and show together.

## Feedback & About

Found a bug or have an idea? Open an [Issue](https://github.com/imbbbbb/BarBar-support/issues/new/choose). Including the text from **Settings → About → Export diagnostics** helps track things down much faster.

BarBar is closed-source software written independently from scratch. This repository is used for releases and issue tracking only.
