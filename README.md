## Firmware Update (UF2 / Drag-and-Drop)

1) Double-click the reset/reboot button to enter bootloader mode.
2) A USB drive will appear on your computer.
3) Copy the `.uf2` file, then drag it onto the device drive.
4) The device will reboot automatically after the copy finishes.

If you like my work, you can support me here:

[![Buy Me a Coffee](https://img.buymeacoffee.com/button-api/?text=Buy%20me%20a%20coffee&emoji=☕&slug=przemeks&button_colour=ff8800&font_colour=000000&font_family=Lato&outline_colour=000000&coffee_colour=FFDD00)](https://buymeacoffee.com/przemeks)


# v1.11.0.1

## UI (WioTrackerL1 companion, ui-new)
- Home carousel tweaks (Messages count, Channels/Contacts/Adverts/System ordering).
- Messages list shows latest conversations; channels open channel history view.
- Channel history header shows current channel name at top.
- Contact conversation header shows who you’re talking to.
- Channel history displays inverted nick without time.
- Contact conversations use RX/TX tags with inverted label block only for contacts.
- Adverts screen merged with recent adverts list, added send options.
- GPS/Bluetooth/Time screens cleaned up for fit and labels.
- RX Log updated for selection-based scrolling.
- Contacts list now opens an action menu (Send message / Delete contact).

## Input / Messaging
- T9 joystick keyboard added for all text inputs.
- Quick replies list added, plus user quick texts (add/remove) on device.
- Custom quick texts appear at top with `*` prefix; base list includes “Hi!” and “Bye”.
- Quick text persistence stored in /quick_texts.
- DM messages show “*” suffix when ACK is received, and “..” while pending.
- WioTrackerL1 on-device sends now register ACKs so delivery status can update.
- Empty conversations return to contacts on cancel; after sending, you return to the conversation.

## System menu
- New System screen: device name edit, battery %, uptime, RAM (placeholder), max contacts, reset defaults.

## Radio settings
- Radio settings menu reworked: presets, custom params, power control.

## Platform config
- WioTrackerL1 platformio config trimmed to GPS-only sensor libs.


