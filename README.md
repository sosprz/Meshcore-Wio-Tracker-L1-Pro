## Download Firmware

Get the latest release files here:
https://github.com/sosprz/Meshcore-Wio-Tracker-L1-Pro/releases


## Firmware Update (UF2 / Drag-and-Drop)

1) Double-click the reset/reboot button to enter bootloader mode.
2) A USB drive will appear on your computer.
3) Copy the `.uf2` file, then drag it onto the device drive.
4) The device will reboot automatically after the copy finishes.

## Firmware Update (Web Flash)

You can also flash using the web flasher. Choose "Custom firmware" at the bottom:

https://flasher.meshcore.co.uk


## Thanks 
If you like my work, you can support me here:

[![Buy Me a Coffee](https://img.buymeacoffee.com/button-api/?text=Buy%20me%20a%20coffee&emoji=☕&slug=przemeks&button_colour=ff8800&font_colour=000000&font_family=Lato&outline_colour=000000&coffee_colour=FFDD00)](https://buymeacoffee.com/przemeks)

# Firmware contains UI changes and base on Meshcore:
 https://github.com/meshcore-dev/MeshCore

# Companion Radio UI (ui-input) Features

## Overview
- Home carousel pages: `Messages`, `Contacts`, `Channels`, `Adverts`, `Radio`, `Bluetooth`, `Sound`, `GPS`, `Time`, `System`, `Tools` (depends on build flags).
- Shortcut visibility can be configured for `Radio/GPS/Time/Bluetooth/Sound` in `System -> UI`.

## Messaging
- Direct messages (DM) with per-contact threads.
- Channel messaging for public and private channels.
- DM and channel compose screens with unified text-input engine.
- Quick text support:
  - send quick text
  - `+Add quick text`
  - `-Remove quick text`
- Input modes:
  - T9 / on-screen keyboard / hardware keyboard (depends on target/build)
  - shared behavior for submit/back/cursor across text-entry screens.
- Message preview screen for recent incoming messages.

## History and Limits
- Persistent history is stored per thread/channel in QSPI.
- Auto-trim is enabled to prevent unbounded history growth.
- Active RAM windows:
  - DM: `20` messages
  - Channels: `100` messages
- Unread/total counters are persisted and restored after reboot.

## Contacts
- Tabs: `favs`, `contacts`, `repeaters`, `rooms`, `sensors`.
- Favorites are grouped in dedicated `favs` tab.
- Contact actions:
  - send/open DM
  - telemetry / repeater login paths
  - favorite toggle
  - clear conversation / delete contact
- Distance-aware sorting in settings (`none / nearest / farthest`) using cached distance.
- Contacts settings:
  - auto-add filters (users/repeaters/rooms/sensors)
  - overwrite oldest toggle
  - cleanup actions (remove non-users / remove all).

## Channels
- Channel list sorted by unread count.
- Join/create flows:
  - `+Join #channel`
  - `+Join priv channel`
  - `+Create priv channel`
- Channel actions:
  - mute/unmute
  - show/share private key (for private channels)
  - clear messages
  - remove channel
- Channel history supports paging and line/message navigation.
- Private key sharing/join flow is integrated from DM.

## Adverts
- Adverts list with detail view.
- Manual send:
  - `Send advert (0-hop)`
  - `Send advert (flood)`
- Adverts settings:
  - `Advert sound` ON/OFF
  - `Share position` ON/OFF
  - `Advert rate` presets.

## Radio and Logs
- Radio menu with:
  - preset selection
  - custom radio setup (`freq/SF/BW/CR`)
  - TX power
  - repeat toggle
  - Local Stats
  - RX Log
- Custom Radio uses staged edits and saves on `OK` (`save [ok]` hint).
- Repeat is blocked on blacklist ranges (`433.x`, `869.x`, `918.x`) and auto-disabled when needed.
- Page up/down (`LEFT/RIGHT`) supported in Local Stats, Repeater Stats, RX Log.

## System
- System menu entries:
  - Change device name
  - Bluetooth
  - UI
  - Display
  - Radio
  - GPS
  - Time
  - Battery
  - Sound
  - Messages
  - Telemetry
  - Stats
  - Reset to default
- Bluetooth card/menu shows connection state and PIN when relevant.
- Sound supports level cycling (`OFF/ON/LOW/MEDIUM/HIGH`).

## UI and Display Settings
- `System -> UI`:
  - joystick rotation (where available)
  - input filter (`OFF`, then `10..500ms` in `10ms` steps)
  - Home shortcut toggles.
- `System -> Display`:
  - screen timeout
  - brightness (if target supports it)
  - wake on message
  - screen lock.
- Screen lock flow:
  - unlock via `HOLD PREV 3s` + `ENTER x2`
  - guided unlock popup with progress.

## Battery
- Battery settings:
  - ADC multiplier calibration
  - top-bar display mode (`Icon/%/Volt`)
  - battery display refresh and rounding
  - shutdown threshold (`OFF/3300/3400/3500/3600 mV`).

## Telemetry and Repeater Operations
- Telemetry policy settings:
  - allow request
  - location access
  - env access.
- Repeater support:
  - admin/guest login flows
  - stats screen
  - remote request orchestration with retry/timeout handling.

## Tools
- Tools menu order:
  1. `Discover Repeaters`
  2. `Ping bot`
  3. `Stopwatch`
  4. `Countdown Timer`
  5. `Sensors`
  6. `Snake`
- `Discover Repeaters`:
  - auto-start scan on enter
  - zero-hop discovery retries in scan window
  - scrollable live results
  - `ENTER` on selected repeater opens `Repeater Stats`
  - `ENTER` with empty list starts a new scan.

## Status Bar
- Battery shown as icon/percent/voltage (configurable).
- GPS indicator when fix is valid.
- Bluetooth/connected state shown in relevant screens/cards.
