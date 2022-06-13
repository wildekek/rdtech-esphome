# Riden RD6006 controller via ESPHome

This device allows you to control a Riden RD6006 Power Supply via [Home Assistant](https://www.home-assistant.io/). It uses [ESPHome](https://esphome.io/) to abstract modbus commands and expose them to Home Assistant and makes it super easy to interface with your device over WiFi.

It is a replacement for the (frankly terrible) software running on the Riden WiFi module and intended as a replacement for their mobile apps and Windows software.

The functionality is currently *very* limited, but can easily be extended by borrowing ideas from https://github.com/Baldanos/rd6006, which was a huge inspiration for this project.

## Requirements:
- An FTDI adapter
- The chip-enable pin on the RD6006 should be physically disconnected or enabled trough [alternative RD6006 firmware](https://www.eevblog.com/forum/testgear/ruideng-riden-rd6006-dc-power-supply/950/)
- The RD6006 should have the TTL setting enabled

<img width="1028" alt="image" src="https://user-images.githubusercontent.com/2332647/171522772-cb27c1a2-5ebc-4385-a022-043dd3dfc149.png">
