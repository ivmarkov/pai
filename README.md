# PAI - Paradox Alarm Interface

[![Join the chat at https://gitter.im/paradox-alarm-interface/community](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/paradox-alarm-interface/community)


Middleware that aims to connect to a Paradox Alarm panel, exposing the interface for monitoring and control via several technologies.
With this interface it is possible to integrate Paradox panels with HomeAssistant, OpenHAB, Homebridge or other domotics system that supports MQTT, as well as several IM methods.

It supports MG/SP/EVO panels connected through a serial port, which is present in all panels (TTL 5V), or through a USB 307 module. It also has __beta__ support to connections using the IP150 module, both directly (firmware version <4.0), and through the SITE ID (firmware versions >4.0).

Support for Magellan and Spectra panels is very stable. Support for EVO panels is being added, so YMMV. If you find a bug, please report it.


For further information and detailed usage refer to the [Wiki](https://github.com/jpbarraca/pai/wiki).

If you are having issues, or wish to discuss new features, join us at our [Gitter community](https://gitter.im/paradox-alarm-interface)

On Android, if you install [MQTT Dash](https://play.google.com/store/apps/details?id=net.routix.mqttdash), and [follow the instructions](https://github.com/jpbarraca/pai/wiki#mqtt-dash) you will automatically get a panel like this:
![mqtt_dash](https://user-images.githubusercontent.com/497717/52603920-d4984d80-2e60-11e9-9772-578b10576b3c.jpg)

## Branch build statuses
- [master](https://github.com/ParadoxAlarmInterface/pai/tree/master) [![Build Status Master](https://travis-ci.org/ParadoxAlarmInterface/pai.svg?branch=master)](https://travis-ci.org/ParadoxAlarmInterface/pai)
- [dev](https://github.com/ParadoxAlarmInterface/pai/tree/dev) [![Build Status Dev](https://travis-ci.org/ParadoxAlarmInterface/pai.svg?branch=dev)](https://travis-ci.org/ParadoxAlarmInterface/pai)

## Things you need to have to be able to connect
We support two connection options: via Serial and via IP150 Module

#### For all connection methods
- **PC Password:** 4 digit `[0-9a-f]` password.
Can be looked up in Babyware (_Right click on a panel ⇾ Properties ⇾ PC Communication (BabyWare) ⇾ PC Communication (BabyWare) ⇾ PC Password_)
#### In case of IP150 you need additionally:
- **IP Module password**: Default is `paradox`
##### For IP150 firmware > 4.0 if you connect via Paradox Cloud (SWAN)
- **SITE ID**
- **Email registered in the site**

## How to use
See [wiki](https://github.com/ParadoxAlarmInterface/pai/wiki/Installation)

## Tested Environment

Tested in the following environment:
* Python > 3.5.2
* Mosquitto MQTT Broker >v 1.4.8
* OrangePi 2G-IOT, NanoPi NEO, and Raspberry Pi 3 through their built in Serial Port (with a level shifter!), or a USB RS232 TTL adapter (CP2102, PL2303, CH340, etc..)
* Ubuntu Server 16.04.3 LTS
* Paradox MG5050, SP7000 and EVO panels
* [Signal Cli](https://github.com/AsamK/signal-cli) through a DBUS interface
* Pushbullet.py
* SIM900 module through a serial port

## Authors

* João Paulo Barraca - [@jpbarraca](https://github.com/jpbarraca) - Main code and MG/SP devices
* Ion Darie - [@iondarie](https://github.com/iondarie) - Homebridge integration
* Jevgeni Kiski - [@yozik04](https://github.com/yozik04) - EVO devices


## Acknowledgments

This work is inspired or uses parts from the following projects:

* Tertiush at https://github.com/Tertiush/ParadoxIP150v2
* Spinza at https://github.com/spinza/paradox_mqtt


## Disclaimer

Paradox, MG5050 and IP150 are registered marks of PARADOX. Other brands are owned by their respective owners.

The code was developed as a way of integrating personally owned Paradox systems, and it cannot be used for other purposes.
It is not affiliated with any company and it doesn't have have commercial intent.

The code is provided AS IS and the developers will not be held responsible for failures in the alarm systems, or any other malfunction.
