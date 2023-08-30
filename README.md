# RDTech Power Supply Controller via ESPHome

This device allows you to control the RDTech (aka Riden) RD series of power supplies via [Home Assistant](https://www.home-assistant.io/). It uses [ESPHome](https://esphome.io/) to abstract modbus commands and expose them to Home Assistant and makes it super easy to interface with your device over WiFi.

It is a replacement for the (frankly terrible) software running on the Riden WiFi module and intended as a replacement for their mobile apps and Windows software.

## Model support

✅ RD6006:  Supported and tested. Just download the latest release and off you go.

❓ RD6006P: Needs testing: check out the latest release candidate (> 1.4)

❓ RD6012: Needs testing: check out the latest release candidate (> 1.4)

❓ RD6018: Needs testing: check out the latest release candidate (> 1.4)

🛑 RD6024: Not supported. You're welcome to make a pull request :)

## Credits
This repo was based on a Python project by [Baldanos](https://github.com/Baldanos/rd6006).

## What you'll need:
- A [Riden RD](https://rdtech.aliexpress.com/store/923042) power supply with WiFi module
- An [FTDI adapter](https://www.aliexpress.com/item/32273550144.html)
- A [Home Assistant](https://www.home-assistant.io/) installation [with ESPHome](https://esphome.io/guides/getting_started_hassio.html)

## How to:
- Flash your device with the [UniSoft firmware](https://github.com/wildekek/riden-firmware-unisoft)
- Create a new ESPHome device and load this [configuration](/rdtech-powersupply.yaml)
- Update your WiFi credentials in ESPHome
- [Flash the Riden WiFi module with ESPHome](https://esphome.io/guides/physical_device_connection.html)
- Set the right settings in the Riden power supply:
	- UART Interface to "TTL+EN"
	- UART Baudrate to "115200"
	- Address to "1"
	- Skip keys lock to "ON"

## Features
<img width="825" alt="image" src="https://github.com/wildekek/rdtech-esphome/assets/2332647/e5a712ff-85f0-40c0-9eed-f98f387a32b2">

## Dashboard example
<img width="1113" alt="image" src="https://github.com/wildekek/rdtech-esphome/assets/2332647/cef2e02a-3b41-40e4-894a-8eb2d8841829">
