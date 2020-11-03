# 30xx - Hardware Module

The Hardware module is meant to offer a simple interface to control the heating temperature.
It should be connected to the ethernet (i.e. LAN/WLAN) and be controllable via http commands.
Furthermore MQTT or other busses might be of use.

So far the following hardware modules have been designed:

* [3001 - Vaillant 789 interface](3001_vaillant789/README.md)


### API details

The module should offer an API to control the heating supply temperature in a simple way. There is no need to only accept degree values, percentage values or something similar are also fine, but it should be kind of a linear function.

## Contribution

To add support for further heating systems, add a new folder with the next free number.