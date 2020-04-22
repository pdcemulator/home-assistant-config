# Overview
This is my [Home Assistant Core](https://home-assistant.io) configuration.
My house runs with the KNX bus system. The majority of the automations are implemented inside KNX system. I use HA to connect other systems.

# Contents
* [Hardware](#hardware)
  * [Binary Sensor](#binary_sensor)
  * [Cover](#cover)
  * [Light](#light)
  * [Sensor](#sensor)
  * [Switch](#switch)
  * [Media Player](#media_player)
  * [Network](#network)
  * [Other](#other)
* [Software](#software)
* [References](#references)

# <a name="hardware">Hardware</a>

## <a name="binary_sensor">Binary Sensor</a>
| Device  | Connection | Home Assistant | Notes |
| ------------- | ------------- | ------------- | ------------- |
| [MDT BE-02001](https://www.mdt.de/EN_Universal_Interface.html)| KNX | [KNX Binary Sensor](https://www.home-assistant.io/integrations/binary_sensor.knx/) | Universal Interface |
| [MDT BE-04001](https://www.mdt.de/EN_Universal_Interface.html)| KNX | [KNX Binary Sensor](https://www.home-assistant.io/integrations/binary_sensor.knx/) | Universal Interface |
| [MDT BE-16000](https://www.mdt.de/EN_Binary_Inputs.html)| KNX | [KNX Binary Sensor](https://www.home-assistant.io/integrations/binary_sensor.knx/) | Binary Inputs for potential free contacts |
| [Shelly Flood](https://shelly.cloud/shelly-flood-and-temperature-sensor-wifi-smart-home-automation/)| MQTT | [MQTT Binary Sensor](https://www.home-assistant.io/integrations/binary_sensor.mqtt/) | water leakage sensor |

## <a name="cover">Cover</a>
| Device  | Connection | Home Assistant | Notes |
| ------------- | ------------- | ------------- | ------------- |
| [MDT JAL-0810](https://www.mdt.de/EN_Shutter_Actuators.html)| KNX | [KNX Cover](https://www.home-assistant.io/integrations/cover.knx/) | Shutter Actuator |

## <a name="light">Light</a>
| Device  | Connection | Home Assistant | Notes |
| ------------- | ------------- | ------------- | ------------- |
| [MDT AKD-0401](https://www.mdt.de/EN_Dimming_Actuators.html)| KNX | [KNX Light](https://www.home-assistant.io/integrations/light.knx/) | 230V Dimming Actuator |
| [MDT AKD-0424R](https://www.mdt.de/EN_LED_Controller.html)| KNX | [KNX Light](https://www.home-assistant.io/integrations/light.knx/) | 24V CV LED Dimming Actuator |

## <a name="sensor">Sensor</a>
| Device  | Connection | Home Assistant | Notes |
| ------------- | ------------- | ------------- | ------------- |
| [MDT BE-GT2TW](https://www.mdt.de/EN_Glas_Push_Buttons_Smart.html)| KNX | [KNX Sensor](https://www.home-assistant.io/integrations/sensor.knx/) | Glass Push Button with temperature sensor |
| [MDT BE-GTT4W](https://www.mdt.de/EN_Glas_Push_Buttons.html)| KNX | [KNX Sensor](https://www.home-assistant.io/integrations/sensor.knx/) | Glass Push Button with temperature sensor |
| [BJ 6131/21](https://www.busch-jaeger.de/produktuebersicht?tx_nlbjproducts_catalog%5Baction%5D=show&tx_nlbjproducts_catalog%5BcatBjeProdukt%5D=4113&tx_nlbjproducts_catalog%5BcatStdArtikel%5D=3662&tx_nlbjproducts_catalog%5Bcontroller%5D=CatStdArtikel&cHash=c6f1cfea50e5e80ea9ce72c86ab42c8f)| KNX | [KNX Sensor](https://www.home-assistant.io/integrations/sensor.knx/) | Presence Detector, Light- and temperature sensor |
| [MDT SCN-G360K3](https://www.mdt.de/EN_Presence_Detectors.html)| KNX | [KNX Sensor](https://www.home-assistant.io/integrations/sensor.knx/) | Presence Detector, Light- and temperature sensor |
| [Steinel iHF 3D](https://www.steinel.de/en/trade-professional/sensors/knx/ihf-3d-knx-007607.html)| KNX | [KNX Sensor](https://www.home-assistant.io/integrations/sensor.knx/) | Movement Detector |
| [MDT SCN-WS3HW](https://www.mdt.de/EN_Weather_Station.html)| KNX | [KNX Sensor](https://www.home-assistant.io/integrations/sensor.knx/) | Weather Station |
| Elabnet DS18B20 based sensors | 1-Wire (over KNX)| [KNX Sensor](https://www.home-assistant.io/integrations/sensor.knx/) | Temperature sensor |
| Elabnet DS2438 based sensors | 1-Wire (over KNX) | [KNX Sensor](https://www.home-assistant.io/integrations/sensor.knx/) | Humidity sensor |

## <a name="switch">Switch</a>
| Device  | Connection | Home Assistant | Notes |
| ------------- | ------------- | ------------- | ------------- |
| [MDT AKK-0816](https://www.mdt.de/EN_Switch_Actuators_AKK.html)| KNX | [KNX Switch](https://www.home-assistant.io/integrations/switch.knx/) | Switch Actuator |
| [MDT AKS-1216](https://www.mdt.de/EN_Switch_Actuators_AKS.html)| KNX | [KNX Switch](https://www.home-assistant.io/integrations/switch.knx/) | Switch Actuator |

## <a name="media_player">Media Player</a>
| Device  | Connection | Home Assistant | Notes |
| ------------- | ------------- | ------------- | ------------- |
| [LG 43UM7500PLA](https://www.lg.com/uk/tvs/lg-43UM7500PLA) | Ethernet | [LB webOS](https://www.home-assistant.io/integrations/webostv/) | TV |
| [Sonos Beam](https://www.sonos.com/en-us/shop/beam.html) | Wifi | [Sonos](https://www.home-assistant.io/integrations/sonos/) | Audio Playback and TTS |
| Sonos Play:1 | Wifi | [Sonos](https://www.home-assistant.io/integrations/sonos/) | Audio Playback and TTS |
| Sonos Play:3 | Wifi | [Sonos](https://www.home-assistant.io/integrations/sonos/) | Audio Playback and TTS |

## <a name="network">Network</a>
| Device  | Connection | Notes |
| ------------- | ------------- | ------------- |
| [Ubiquiti USG](https://www.ui.com/unifi-routing/usg/)| Ethernet | Router |
| [Ubiquiti USW](https://www.ui.com/unifi-switching/unifi-switch-poe/)| Ethernet | Switch |
| [Ubiquiti UAP AC Lite](https://www.ui.com/unifi/unifi-ap-ac-lite/)| Ethernet/Wifi | Access Point |

## <a name="other">Other</a>
| Device  | Connection | Notes |
| ------------- | ------------- | ------------- |
| [Elabnet Timberwolf 950Q](https://shop.wiregate.de/aktion/multifunktionsgateway/timberwolf-hutschiene/timberwolf-server-950-art-nr-517.html) | KNX / Ethernet / 1-Wire | KNX IP Interface, 1-Wire Gateway, Logic Server |
| [MDT SCN-LOG1](https://www.mdt.de/EN_Logical_Module.html) | KNX | Logic Module |
| [MDT SCN-LK001](https://www.mdt.de/EN_Interfaces.html) | KNX | Line Coupler |
| [Weinzierl 730](https://www.weinzierl.de/index.php/en/all-knx/knx-devices-en/produktarchiv-en/knx-ip-interface-730-en) | KNX / Ethernet | KNX IP Interface |
| [Samsung Galaxy Tab A](https://www.samsung.com/uk/tablets/galaxy-tab-a-10-1-2016-t580/SM-T580NZKABTU/) | Wifi | Wall mounted display with [Fully Kiosk Browser](https://www.ozerov.de/fully-kiosk-browser/) showing Lovelace UI |
| [Synology Diskstation DS918+](https://www.synology.com/en-global/products/DS918+) | Ethernet | NAS, running Home Assistant Core in [Docker container](https://hub.docker.com/r/homeassistant/home-assistant) |
| [Raspberry Pi 2B](https://www.raspberrypi.org/products/raspberry-pi-2-model-b/) with [PiCAN 2 Board](http://skpang.co.uk/catalog/pican2-canbus-board-for-raspberry-pi-23-p-1475.html) | CAN / MQTT | Connecting Rotex HPSU with [pyHPSU](https://github.com/Spanni26/pyHPSU) over MQTT to HA |
| [Rotex HPSU compact](https://www.rotex-heating.com/products/heat-pump/air-to-water-heat-pump/hpsu-compact.html) | CAN | Heat Pump |


# <a name="software">Software</a>
| Device  | Home Assistant | Notes |
| ------------- | ------------- | ------------- |
| [Mosquitto MQTT Broker](https://mosquitto.org/) | [MQTT](https://www.home-assistant.io/integrations/mqtt/) | running in Docker Container |
| [pyHPSU](https://github.com/Spanni26/pyHPSU) | [MQTT](https://www.home-assistant.io/integrations/mqtt/) | send values (temperature, mode etc) from my Heat Pump to HA |
| [Fully Kiosk Browser](https://www.ozerov.de/fully-kiosk-browser/) | [Rest Command](https://www.home-assistant.io/integrations/rest_command/) | power on / off tablet display when movement is detected |
| [Nextcloud Calendar](https://nextcloud.com/) | [CalDAV](https://www.home-assistant.io/integrations/caldav/)| Calendar |


# <a name="references">References</a>
Thanks to this (any many others) who are sharing their ha config, tipps and other useful information.
* https://github.com/adonno/awesome-home-assistant
* https://github.com/matt8707/hass-config
* https://github.com/adonno/Home-AssistantConfig
* https://github.com/JamesMcCarthy79/Home-Assistant-Config
* https://github.com/geekofweek/homeassistant