# AirGradient-ESPHome: First commit
An ESPHome configuration for the AirGradient DIY Air Quality Sensor to send air quality data directly to Home Assistant. While I have another AirGradient repository that I used initially, [LongDono/airgradient-prometheus](https://github.com/LongDono/airgradient-prometheus), this fork only supports Home Assistant and features a significantly changed display to try to make better use of that 0.96" OLED. Another change is that the Home Assistant entity names now indicate the location in case you have more than one AirGradient unit deployed. Finally, I was getting HTTP errors from the AirGradient Server code (stores data on AirGradient's Servers) and decided to remove support for it.

Currently, you will have to edit the code to enable/disable features while I learn more about ESPHome. :)

## Pre-Fork Configuration Notes
If all original sensors (PMS5003, Senseair S8, SHT3x) are connected, airgradient.yml should be fully ready
If some sensors are not installed, comment or remove the associated sections in sensor: and display: and http_request.post:
Commented code supports TVOC readings from SGP30 sensor, but in testing, it required being connected to 3.3v instead of 5v as wired on the AirGradient board.  Also does not appear to work if the OLED display is connected, but works if display is physically removed.

To add your wifi SSID and password, either remove the "!secret" section and type in your information, or edit the secrets.yaml file with
your information so it is not hard coded into the device's file.
