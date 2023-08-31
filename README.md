# RDTech Power Supply Controller via ESPHome

This is a configuration for [ESPHome](https://esphome.io/) that allows you to control the RDTech (aka Riden/Riuden) RD series of power supplies via [Home Assistant](https://www.home-assistant.io/).

![image](https://github.com/wildekek/rdtech-esphome/assets/2332647/bd71e5d8-c1b3-44ad-8bbc-08e48c079813)


## Model support
* RD6006: ✅ Supported and tested. Just download the latest release and off you go.
* RD6018: ✅ Supported and tested. Download the latest release candidate.
* RD6006P:❓ Needs testing: check out the latest release candidate and share your results [here](https://github.com/wildekek/rdtech-esphome/issues/5)
* RD6012: ❓ Needs testing: check out the latest release candidate and share your results [here](https://github.com/wildekek/rdtech-esphome/issues/5)
* RD6024: 🛑 Not properly supported, as there is no Unisoft firmware yet.

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
