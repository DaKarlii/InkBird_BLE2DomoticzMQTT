# iBBQ-Gateway-Fork for Domoticz

an ESP32 Based iBBQ (Inkbird) BLE to MQTT Gateway. This is an fork of runningtoy/InkBird_BLE2MQTT

## Requirements

* Wemos Lolin 32 (or other ESP32 Boards)
* MS Visual Studio Code with PlatformIO
* Domoticz with configured MQTT Client Gateway with LAN interface
* an Inkbird IBT Thermometer

## Usage

* In Domoticz:
Create new virtual Temperature Devices (in ascending IDX order) for each [possible] Probe.
eg. IBT-2x --> 2 virtuel Temp Devices
Create new virtual Percentage Device for the Battery Level

* In VSCode:
Before Flashing create/edit the "src/credentials.h" and "src/domoticz.h". 
You can find the example files in the directory.

After flashing the device should be connected to your WiFi and your MQTT broker.

While boot up, the Gateway is lloking for the BBQ Thermometer and will connect to it Automatically.
After successfully connected per BLE the Gateway starts publishing the Tempdata to MQTT/Domoticz.


## Features

* Automatically connects to iBBQ Bluetooth BBQ thermometers (tested with InkBird IBT-6X and IBT-2X)
* Adapts amount of channels to connected thermometer
* Should work with most ESP32 boards available
* Should work with iBBQ based Bluetooth BBQ thermometers with up to 8 channels
* Publish temperature (Celsius) and battery Level to MQTT/Domoticz
* Battery status according to (https://github.com/sworisbreathing/go-ibbq/issues/2#issuecomment-650725433)

## ToDO

## Protocol description
(https://gist.github.com/uucidl/b9c60b6d36d8080d085a8e3310621d64)
