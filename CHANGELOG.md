# homebridge-hm-homeseer

## 1.0.26
- Documented `controlValues` override syntax and allowed keys per device type in README
- Added changelog

## 1.0.25
- Added support for Add 8 new HomeKit accessory types: windowcovering, door, window, outlet, programmableswitch, irrigation, occupancy sensor, CO2 sensor, air quality sensor

## 1.0.24
- Save and load manually defined control values
- Allow overriding of control values in switches

## 1.0.23
- Prevent accessory removal when homeseer is unreachable

## 1.0.22
- Automatically fetch control pairs for newly created devices
- Fan speed fixes for dimmable fans

## 1.0.21
- Added non dimmable fan
- UI can now search by device ID

## 1.0.20
- fan/thermostat companion ref parent check

## 1.0.19
- Fix: real time sync of accessory state between homeseer and homebridge

## 1.0.18
- Plugin will now report failure to correctly process control values
- Display name improvements

## 1.0.17
- Added support for alarm panels

## 1.0.16
- Better support for bond fans

## 1.0.15
- Fan accessory supports multiple speed or fixed speed (on/off only)

## 1.0.14
- Supports water valve accessory

## 1.0.13
- Garage door uses value_string for state detection (Open, Closed, Opening, Closing, Stopped)
- Open/close/stop ControlPairs detection always runs (not blocked by on/off detection)
- Supports HomeKit transitional door states

## 1.0.12
- Fan and garage door now read on/off/open/close values from ControlPairs (no more hardcoded 255/0)
- Better device naming: prepends HS4 room name when no voice command is set
- Added open/close/stop value detection to ControlPairs scanning

## 1.0.11
- Expanded thermostat companion ref search to +/-20 refs in both directions
- Added last-resort exact name match for setpoints in same HS4 location
- Changed temperature minStep from 0.5 to 0.1 for better Fahrenheit precision

## 1.0.10
- Full thermostat rewrite: heat/cool/auto modes, separate heat and cool setpoints
- Companion device discovery for Ecobee, Honeywell, and Z-Wave thermostats
- Humidity sensor support as linked service
- Operating state detection from value_string

## 1.0.9
- Ecobee and Honeywell auto-detection from device_type_string and location field
- Exclude thermostat sub-devices (sensors, setpoints, modes) from being detected as standalone thermostats

## 1.0.8
- ControlPairs auto-detection for switches, dimmers, locks
- Label-based fallback when ControlUse enum is not set (common for plugin-created devices)
- Type change detection: re-creates HomeKit accessory when device type changes

## 1.0.7
- Fixed Multilevel Sensor incorrectly detected as lightbulb
- Temperature sensors now convert Fahrenheit to Celsius for HomeKit
- Web UI cache flush after saving device selections

## 1.0.6
- Initial public release
- Auto-discovery, ASCII event stream, web UI device picker
- Support for switches, dimmers, fans, locks, garage doors, sensors
