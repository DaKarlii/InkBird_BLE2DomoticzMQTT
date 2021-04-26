# iBBQ-Gateway-Fork for Domoticz

an ESP32 Based iBBQ (Inkbird) BLE to MQTT Gateway. This is an fork of runningtoy/InkBird_BLE2MQTT

## Requirements

## Usage

Before Flashing create/edit the "src/credentials.h" and "src/domoticz.h". 
You can find the example files in the directory.

After flashing the device you should connect to your WiFi.

Tt should connect to your iBBQ Device and starts to publish data.

## Features

* Automatically connects to iBBQ Bluetooth BBQ thermometers (tested with InkBird IBT-6X and IBT-2X)
* Adapts amount of channels to connected thermometer
* Should work with most ESP32 boards available
* Should work with iBBQ based Bluetooth BBQ thermometers with up to 8 channels
* Publish temperature (Celsius) and battery Level to MQTT/Domoticz
* Battery status according to (https://github.com/sworisbreathing/go-ibbq/issues/2#issuecomment-650725433)[https://github.com/sworisbreathing/go-ibbq/issues/2#issuecomment-650725433]

## ToDO

## Protocol description
(https://gist.github.com/uucidl/b9c60b6d36d8080d085a8e3310621d64)
