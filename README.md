# miThermoHygro
[![Python](https://img.shields.io/badge/python-2-brightgreen.svg)]() [![Donate](https://img.shields.io/badge/donate-PayPal-brightgreen.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=5654A67GA3GHA)

**Important information: This library was developed for working with FW version 00.00.66. Xiaomi might change interface in future FW updates!**

*This python script allows you interfacing Xiaomi BLE temperature and humidity sensors with Domoticz. To be able to use it your device needs a bluetooth hardware that supports BLE, Python (2) as well as external libraries as defined in imports. Tested on Raspberry Pi 3.*

## Setup
First you need to know the MAC addresses of your sensor devices (can be easily found using hcitool on PC/Mac or smarthone BLE scan apps).
Next create a new hardware device in Domoticz using type "dummy" and add the according amount of your sensors as devices of type "Temp + Humidity" to it. Afterwards open the script and edit the Domoticz configuration to match your setup. Next add your sensors (with the MAC addresses you got above) and assign them to the according device Idx of domoticz. You can add as many sensors as you want (of course also only one is possible).

That´s it! Now whenever you run the Python script the sensor data in Domoticz gets updated. For continuous polling just create a cronjob for example on your device calling the Python script.

## Supported values
* temperature
* humidity
* battery level

## Thanks
A big thanks to [Dirk (distel) of the FHEM forum](https://forum.fhem.de/index.php/topic,82249.0.html) for reverse engineering the sensor!

