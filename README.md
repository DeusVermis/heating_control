# Heating Control

## Introduction
This project is meant to control a central-heating system in a private appartment or house.
For now it presumes an installation with the following components:

* OpenHab2
* Homematic CCU and radiator thermostats
* Vaillant central-heating boiler with 789-interface

The project is meant to be extended. Contribution appreciated.

### Problem
Especially older central-heating systems may only have a room thermostat. This provokes two problems:

* The heating is only/mainly controled by the temperature of the one room where the room thermostat is installed. This is usually the living or dining room. If this room is warm the central-heating is switched off although other rooms need heating and they may stay cold. Vice versa there might be no desire to heat this room. In this case the central-heating keeps running even if the other rooms might be warm enough.
* The heating supply temperature is either controlled manually with an adjustment wheel on the central-heating itself or dependent of the difference of the desired and the actual temperature of the room with the room thermostat. As described above the desired heating might not match that room temperature and thus too high or too low heating supply temperatures might be used.

### Solution
Instead of a room thermostat in one room the heating supply temperature is calculated by the needs of all radiators and the outside temperature.
The central-heating boiler is only running if any radiator requests its need.

## Modus operandi

The workflow is separated in the following modules with the objective to be extended if needed:

* [10xx - Weather](10xx_weather/README.md): Getting and updating outside temperature.
* [20xx - Heating Supply Temperature](20xx_heating_supply_temp/README.md): Calculating and updating heating supply temperature.
* [30xx - Hardware Module](30xx_hardware_module/README.md): Controlling the central-heating boiler with a hardware module.

## Disclaimer

Use at your own risk. The contributors of this project cannot be made liable for any harm or damage that is caused by use or reproduction.