<p align="center">
<img src="https://raw.githubusercontent.com/ivoronin/TomatoBar/main/TomatoBar/Assets.xcassets/AppIcon.appiconset/icon_128x128%402x.png" width="128" height="128"/>
<p>
 
<h1 align="center">Pomodoro</h1>
<h2 align="center">The missing pomodoro timer for macOS</h2>
<p align="center">
<img src="https://img.shields.io/github/actions/workflow/status/ivoronin/TomatoBar/main.yml?branch=main"/> <img src="https://img.shields.io/github/downloads/ivoronin/TomatoBar/total"/> <img src="https://img.shields.io/github/v/release/ivoronin/TomatoBar?display_name=tag"/> <img src="https://img.shields.io/homebrew/cask/v/tomatobar"/>
</p>

<img
  src="https://github.com/ivoronin/TomatoBar/raw/main/screenshot.png?raw=true"
  alt="Screenshot"
  width="50%"
  align="right"
/>

## Overview
Have you ever heard of Pomodoro? It’s a great technique to help you keep track of time and stay on task during your studies or work. Read more about it on <a href="https://en.wikipedia.org/wiki/Pomodoro_Technique">Wikipedia</a>.

Pomodoro is world's neatest Pomodoro timer for the macOS menu bar. All the essential features are here - configurable
work and rest intervals, optional sounds, discreet actionable notifications, global hotkey.

Pomodoro is fully sandboxed with no entitlements (except for the Apple Events entitlement, used to run the Do Not Disturb toggle shortcut).

---

## Other great open source mac apps:
### Menu Bar
- ICE: Powerful menu bar manager for macOS (https://github.com/jordanbaird/Ice)
- TRex: Captures any text right into your Clipboard with magic of OCR (https://github.com/amebalabs/TRex)
- reminders-menubar: Menu bar application to view and interact with reminders (https://github.com/DamascenoRafael/reminders-menubar)
- Calendr: Menu bar calendar for macOS (https://github.com/pakerwreah/Calendr)
### Apps
- CotEditor: The better Plain-Text Editor for macOS (https://coteditor.com/)
- Lulu: Firewall designed to block unknown outgoing connections (https://objective-see.org/products/lulu.html)

---

## Fork notes
This is a fork and more advanced version of https://github.com/ivoronin/TomatoBar and makes a couple additions/modifications:

1. Allows 0 rest interval instead of the minimum of 1. Closes (https://github.com/ivoronin/TomatoBar/issues/62).
2. Changes start button to blue.
3. Increases the maximum timer duration to 2 hours/120 minutes.
4. Adds an option to toggle Do Not Disturb automatically using a shortcut. The first time you start the timer, you'll be prompted to add the shortcut; it will work fine afterwards (also PRed to https://github.com/ivoronin/TomatoBar/pull/82).
5. Adds sound customization: To use, open the sound folder from settings and place audio files named "windup," "ding," or "ticking" in mp3 or m4a/mp4 (aac/alac) format.
6. Adds a preset selector with 4 presets you can quickly switch between.
7. Adds a pause button, keyboard shortcut, and URL (based on https://github.com/ivoronin/TomatoBar/pull/52).
8. Adds a skip button, keyboard shortcut, and URL which can skip both work and rest (in addition to the existing rest skip notification).
9. Adds an "add a minute" button, keyboard shortcut, and URL.
10. Extends "stop after break" with "work" and "set" options.
11. Adds a "start with break" option.
12. Adds a "start timer on launch" option.
13. Makes numbers in the settings editable (based on https://github.com/ivoronin/TomatoBar/pull/63).
14. Displays the current interval on the start/stop button when "Stop after" is disabled.
15. Turns the volume display into a percentage and adds a long tap gesture on the percentage to mute/unmute (in addition to the existing double tap reset).
16. Adds an option for a full-screen mask (taken from https://github.com/ivoronin/TomatoBar/pull/65).
17. Doesn't play sounds when the volume is set to zero (fixes issues with, e.g., multipoint Bluetooth headphones).
18. Increases the minimum macOS version requirement to Monterey.

## Integration with other tools
### Event log
Pomodoro logs state transitions in JSON format to `~/Library/Containers/com.github.ivoronin.TomatoBar/Data/Library/Caches/TomatoBar.log`. Use this data to analyze your productivity and enrich other data sources.
### Controlling the timer
Pomodoro can be controlled using `tomatobar://` URLs. To start or stop the timer from the command line, use `open tomatobar://startStop`. To pause or resume use `open tomatobar://pauseResume`. To skip use `open tomatobar://skip`. To add a minute use `open tomatobar://addMinute`

## Older versions
Touch bar integration and older macOS versions (earlier than Big Sur) are supported by Pomodoro versions prior to 3.0

## Licenses
 - Timer sounds are licensed from buddhabeats
 - "macos-focus-mode.shortcut" is taken from the <a href="https://github.com/arodik/macos-focus-mode">macos-focus-mode</a> project under the MIT license.
