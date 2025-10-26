## 1.0.1

### 🔧 What's Fixed

- Custom EEP mapping file was not taken into account (https://github.com/ChristopheHD/HA_enoceanmqtt-addon/issues/74)
- Remove wrong error logs when using external MQTT server (https://github.com/ChristopheHD/HA_enoceanmqtt-addon/issues/73)

### 🛑 What's Removed

- Entity `cover` have been removed from EEP D2-05-xx to avoid confusion for new-comers. Only entity `cover2` is remaining. `cover2` is not a good entity name but changing it would force current users to review all their automations.

## 1.0.0

### 🚨 Breaking change !

If you are using debug option, mapping file or MQTT configuration, you will need to reset those configurations after the update

### 🎉 Version 1

Since more than 1 year that I made this fork and tried to improve the life of HA Enocean device owners (50+ users when I write those lines), I decided that this addon is stable enough to have a version 1.x release. Next releases will follow the versioning rules described in [VERSION.md](https://github.com/ChristopheHD/HA_enoceanmqtt-addon/blob/master/VERSION.md)

### ✨ What's New

- Device Eltako TF100L
- Device Eltako FLD61
- Device Eltako FBH55ESB
- French translation of configuration tab

### 🚀 What's Improved

- Configuration tab have been reorganized with categories of options
- Better error handling at startup (https://github.com/ChristopheHD/HA_enoceanmqtt-addon/issues/68 and https://github.com/ChristopheHD/HA_enoceanmqtt-addon/issues/69)

### 🔧 What's Fixed

- Fixes for EEP D2-14-41 thanks to @frankrml including
  - Removing of raw data
  - Rounding illumination value
  - Accelaration status is now type enum
  - Rounding acceleration values
  - Contact sensor is now type door
  - Contact sensor have now a door icon
 
### 🛑 What's Removed

- Option to use device name in entity name have been removed

### 👏 New Contributors

- @frankrml made their first contribution
  
## 0.1.42

### 🚀 What's Improved

- Better serial port handling and logging to prevent or have more information on issue https://github.com/ChristopheHD/HA_enoceanmqtt-addon/issues/61

### 🔧 What's Fixed

- EEP D2-01-11 state fixed for DALI controllers (and other controllers based on dimming) (https://github.com/ChristopheHD/HA_enoceanmqtt/pull/19)
- Eltako FJ62 current position fixed on reboot thanks to @jdr85 (https://github.com/ChristopheHD/HA_enoceanmqtt/pull/20)

### 👏 New Contributors

- @jdr85 made their first contribution

## 0.1.41

### ✨ What's New

- Device Eltako FR62-230V thanks to @jansorg
- Device Afriso FT thanks to @jansorg
- EEP D2-01-11

### 🚀 What's Improved

- Documentation tab of the addon have been improved (quick setup guide and correct links to wiki)
- Use of Python XML library for EEP.xml file (https://github.com/ChristopheHD/HA_enoceanmqtt-addon/issues/43)

## 0.1.40

### 🔧 What's Fixed

- CPU architecture amd64 compatibility restored (https://github.com/ChristopheHD/HA_enoceanmqtt-addon/issues/51)

## 0.1.38

### ✨ What's New

- Device Eltako FTTB/Piotec Tracker thanks to @Stev-G
- Device Eltako TF61D tested by @Luxmaster

### 🔧 What's Fixed

- Update mechanism is now fixed, no need to rebuild the addon after update (https://github.com/ChristopheHD/HA_enoceanmqtt-addon/issues/29)
- Flood detector and buttons were triggered in automation at HA startup (https://github.com/ChristopheHD/HA_enoceanmqtt-addon/issues/38)

### 🚀 What's Improved

- Addon is now downloaded instead of build locally making it faster to install and version reliable

### 🛑 What's Removed

- Architectures armhf, armv7 and i386 have been removed. If still needed, please open an issue on GitHub

### 👏 New Contributors

- @Stev-G made their first contribution
- @Luxmaster helped testing new device

## 0.1.37

### What's New

- EEP D2-14-41 thanks to @wronny
- Blind central command for EEP A5-38-08 thanks to @bakkerv

## 0.1.36

### What's Changed

- EEP D2-06-01 : rounding temperature sensor

### What's Fixed

- Virtual rocker switch was broken since 0.1.35 in https://github.com/ChristopheHD/HA_enoceanmqtt-addon/issues/24

## 0.1.35

### What's Fixed

- A5-07-01 : presence detection was not working

## 0.1.34

### What's New

- EEP A5-09-0C
- EEP A5-30-02 thanks to @madejackson
- EEP D2-06-01 (following sensors have not been tested : diagnostic, configuration, temperature, humidity, illumination, motion, protection plus alarm)
- EEP F6-05-01 (known bugs : HA automation is triggered at each restart)

### What's Changed

- D2-50-00 : adding air quality and filter maintenance sensors thanks to @Alaric84
- A5-10-03 : Rounding for temperature and humidity with raw values available thanks to @jansorg
- Set-point devices : correction of HA properties for setpoint values thanks to @jansorg

### What's Fixed

- A5 devices not working ("message not interpretable") in https://github.com/ChristopheHD/HA_enoceanmqtt-addon/issues/20

### New Contributors

- @Alaric84 made their first contribution
- @jansorg made their first contribution

## 0.1.33

### What's New

- TCP configuration by @ChristopheHD as requested in https://github.com/ChristopheHD/HA_enoceanmqtt-addon/issues/7

**Full Changelog**: https://github.com/ChristopheHD/HA_enoceanmqtt-addon/compare/v0.1.32...v0.1.33

## 0.1.32

### What's Changed

- Continuous integration by @ChristopheHD in https://github.com/ChristopheHD/HA_enoceanmqtt-addon/pull/4
- Bump pyyaml from 6.0.1 to 6.0.2 in /addon by @dependabot in https://github.com/ChristopheHD/HA_enoceanmqtt-addon/pull/5
- Bump tinydb from 4.7.1 to 4.8.2 in /addon by @dependabot in https://github.com/ChristopheHD/HA_enoceanmqtt-addon/pull/6

### New Contributors

- @ChristopheHD made their first contribution in https://github.com/ChristopheHD/HA_enoceanmqtt-addon/pull/4
- @dependabot made their first contribution in https://github.com/ChristopheHD/HA_enoceanmqtt-addon/pull/5

**Full Changelog**: https://github.com/ChristopheHD/HA_enoceanmqtt-addon/compare/v0.1.30...v0.1.32

## 0.1.30

/!\ Fork aseracorp/HA_enoceanMQTT

### Added

- support TCP-linked transceivers (mak-gitdev/HA_enoceanmqtt#130)
- GH-Actions to build new docker image on every commit (mak-gitdev/HA_enoceanmqtt#155)
- timezone support in Dockerfile, fixes _last seen_ datapoint in HA (mak-gitdev/HA_enoceanmqtt#156)
- include default configfile in container (enoceanmqtt.conf) for easier container-deployment (mak-gitdev/HA_enoceanmqtt#157)
- Add Support for A5-10-01 Temperature Sensor, Set Point, Fan Stage and Occupancy Control

### Fixes

- Fix for the new version of enocean-mqtt (mak-gitdev/HA_enoceanmqtt#136)
- fix EEP A5-12-00 (mak-gitdev/HA_enoceanmqtt#144)
- latest commits not in relase 0.1.28
  - Change off to closed for A5-14-09 and A5-14-0A
  - Fix small issues in mapping file + Add support for D2-05-02
  - Fix battery mapping for A5-20-06
  - Add state_class to entities + start using anchors and alias + update standalone script
  - Fix issue mak-gitdev/HA_enoceanmqtt#121
  - Minor fixes in mapping file
  - Remove EEP.xml from repository
  - D2-01-08 + Fix issue mak-gitdev/HA_enoceanmqtt#122 for Docker and standalone

## 0.1.28

Important: Add a new cover entity (cover2) for D2-05-00. This should fix inverted position issue (thanks to @didi31).

### Fixed

- Add a new cover entity (cover2) for D2-05-00. This should fix inverted position issue (thanks to @didi31).
  See #94 for more details.

### Added

- Add support for:
  - D2-14-30 (Netsecur smoke detector with temperature and humidity sensors)
  - F6-04-01. All NodOn devices to date are now supported.
  - D2-50-00 (thanks to @billeranton for testing and initial mapping)
  - D2-50-01
  - D2-50-10
  - D2-50-11
  - A5-20-01 (control+status)
  - A5-20-04 (control+status)
  - A5-20-06 (control+status, thanks to @stefanhofmann2)
  - A5-14-09 (thanks to @juame in #101)
  - A5-13-04
  - A5-13-05
  - A5-13-06
- Add switches for F6-02-01/02 virtual entities in addition to the existing select entities.

### Changed

- Add A5-13-04, A5-13-05 and A5-13-06 entities to A5-13-01 as requested by the EEP specification.

## 0.1.27

### Changed

None

### Added

- Add support for:
  - D2-01-01
  - D2-01-09
  - A5-09-04
  - A5-30-03
  - A5-30-04
  - A5-38-08 (Command 2)
- Added new configuration entry use_dev_name_in_entity to select whether to use device name in the name of entities.
  This is for users of HA versions from 2023.8.1 to the one before 2024.2.0.
  For users of version before 2023.8.1, this entry is internally forced to true.
  For users of version starting from 2024.2.0, this will be internally forced to false.

### Fixed

- Fixes device selection error (see mak-gitdev/HA_enoceanmqtt#73 and embyt/enocean-mqtt#43 for more details)
- Fix issue mak-gitdev/HA_enoceanmqtt#77 related to MQTT entity naming
- Fix issue mak-gitdev/HA_enoceanmqtt#72

## 0.1.26

### Changed

None

### Added

- Add virtual A5-10-06 (mak-gitdev/HA_enoceanmqtt#46)
- Add '%' as unit of measurement for A5-20-01 current value field (mak-gitdev/HA_enoceanmqtt#53)
- Update F6-02-[01-02] to send status bits

### Fixed

- Use latest enocean-mqtt version which fixes status bits setting (see mak-gitdev/HA_enoceanmqtt#65 and embyt/enocean-mqtt#41 for more details)
- From now, use mak-gitdev/enocean as Python EnOcean Library which fixes "list index out of range error" thanks to @kridgo patch (see kipe/enocean#134 and kipe/enocean#138 for more details).

### Removed

None

## 0.1.25

### Fixed

- Fix issue mak-gitdev/HA_enoceanmqtt#41

## 0.1.24

### Changed

- **Change devices and entities unique ids. This may lead to some devices loosing some configurations such as zones, etc.**
- Add better support for A5-13-01. ID1, ID2 and ID3 are now supported. ID4 to ID6 will follow in another release.
- Use device triggers for D2-03-0A instead of binary sensors.

## Added

- Add support for virtual devices. We can now declare more than one device sending broadcast data. Only F6-02-01 and F6-02-02 are available at the moment.
- Add packet receipt date to all devices so that it is possible to know the last time the device has been seen.
- Add support for:
  - D2-01-0A
  - D2-01-0D
  - D2-01-0E
  - A5-13-[01-06]
  - A5-10-03
  - A5-10-05
  - A5-10-06
  - A5-10-10
  - A5-10-12
  - A5-08-[01-03]
  - A5-14-01
  - A5-14-0A
  - A5-20-01 (no control yet, only status)
  - A5-20-04 (no control yet, only status)
  - Initial support for A5-38-08 command 1
- Add measurement control entities for D2-01-0B, D2-01-0C and D2-01-0E.

### Removed

- Remove some unused entities from D2-01-xx devices to comply with the EEP documentation.

### Fixed

- Fixed issue mak-gitdev/HA_enoceanmqtt#37

## 0.1.23

**Note**: Rename versions in changelog

### Changed

- Rename not rounded entities `xx_temperature` and `xx_humidity` from A5-04-XX devices to `t_raw` and
  `h_raw`. These new entities are also disable by default.

### Added

- Add support for:
  - A5-02-[01-0B]
  - A5-02-[10-1B]
  - A5-02-20
  - A5-02-30
  - A5-06-[01-02]
  - A5-07-[01-03]
  - A5-13-01
  - D2-03-0A

### Removed

- Remove °F entities from A5-04-XX devices as HA seems to convert automatically °C to °F and vice-versa

### Fixed

- Fix status entity for A5-04-XX devices.
