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

**Overview**
- Home carousel with quick pages for Messages, Contacts, Channels, Adverts, Radio, Bluetooth, Sound, Ping, GPS, Time, Sensors, System, and Tools (availability depends on build flags).

**Messaging**
- Direct messages with per-contact conversation history.
- Channel messages with joinable public channels and private channels.
- Message preview screen for recent messages.
- Message detail view for long messages.
- T9/joystick text input with caps, symbols, and quick text support.
- Quick text add/remove screens.

**Contacts**
- Contacts list with contact actions (message, delete).
- Contact list paging with LEFT/RIGHT.
- Contact list sort option (none/nearest/farthest) using cached distances.
- Contact settings screen for auto-add filters and cleanup.
- GPS distance/coordinates shown in contact details when available.

**Channels**
- Channel list with unread counts (sorted by unread first).
- Channel history view with paging and line-by-line scroll.
- Channel compose screen.
- Channel actions screen.

**Radio and Logs**
- Radio settings screens (frequency, SF, BW, CR, power).
- RX log screen with per-packet stats.

**Adverts**
- Adverts menu and recent adverts list.
- GPS distance/coordinates for adverts when available.

**System and Battery**
- System menu with device name, battery info, uptime, GPS units, screen lock, max contacts, and reset.
- Battery submenu with ADC multiplier calibration and status-percent toggle.
- ADC calibration screen with live voltage/percent display.

**Tools**
- Stopwatch.
- Countdown timer.
- Discover nodes tool.
- Signal meter (RSSI/SNR stats with ping sampling).
- Ping tool and ping status page (toggle + status).

**Status Bar**
- Battery indicator or percentage (configurable).
- GPS fix indicator text when fix is valid.
