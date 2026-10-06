# The Mid Click

**Middle click for your Mac trackpad.** The Mid Click is a small macOS utility that turns a three-finger (or four-finger) trackpad tap or click into a standard middle mouse click, in every app.

- Website and guides: https://davletovalmir.github.io/the-mid-click/
- Download (notarized, macOS 26 or later): see [Releases](https://github.com/davletovalmir/the-mid-click/releases/latest)
- Privacy policy: https://davletovalmir.github.io/the-mid-click/privacy.html

## What it does

| | |
|---|---|
| Works with | Built-in MacBook trackpads and Magic Trackpad |
| Gesture | Three-finger tap, three-finger click, or four fingers of either |
| Output | A standard middle mouse button event (button 2 in Core Graphics, "button 3" in X11 terms), including middle-drag in Click mode |
| Useful for | Opening links in background tabs, closing tabs, orbiting in Blender and CAD, panning in Figma, anything mapped to the middle button |
| Permission | Accessibility, used only to read trackpad touches and send the click ([why](https://davletovalmir.github.io/the-mid-click/accessibility-permission/)) |
| Footprint | Menu bar only, no Dock icon, two settings |
| Price | 7-day free trial, then $1/year or $10 lifetime |

## How it works

It reads the trackpad's gesture events through a public `CGEvent` tap and `NSEvent.allTouches()`, rather than Apple's private MultitouchSupport framework, and sends a middle-button `CGEvent`. The full event path is written up at [How middle click actually works on macOS](https://davletovalmir.github.io/the-mid-click/how-middle-click-works-on-macos/).

## Why it isn't on the Mac App Store

App Review restricts Accessibility to assistive purposes, and there is no App Store-approved way to synthesize a mouse button. The app is signed with an Apple Developer ID and notarized. Details: [Why The Mid Click needs Accessibility permission](https://davletovalmir.github.io/the-mid-click/accessibility-permission/).

## This repository

Hosts the website (GitHub Pages) and the release downloads. The app's source is not public.

Made by Almir Davletov. Support: davletovalmir@gmail.com
