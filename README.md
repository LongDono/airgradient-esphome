# AirGradient-ESPHome
An ESPHome configuration for the AirGradient DIY Air Quality Sensor to send air quality data directly to Home Assistant.

## Configuration
If all original sensors (PMS5003, Senseair S8, SHT3x) are connected, airgradient.yml should be fully ready
If some sensors are not installed, comment or remove the associated sections in sensor: and display: and http_request.post:
Commented code supports TVOC readings from SGP30 sensor, but in testing, it required being connected to 3.3v instead of 5v as wired on the AirGradient board.  Also does not appear to work if the OLED display is connected, but works if display is physically removed.

To add your wifi SSID and password, either remove the "!secret" section and type in your information, or edit the secrets.yaml file with
your information so it is not hard coded into the device's file.

## Prometheus option (non-ESPHome)
This fork will be similar in appearance to my other repository that uses Prometheus instead of ESPHome:
https://github.com/LongDono/airgradient-esphome
