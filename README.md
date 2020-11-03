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

* The heating is only/mainly controled by the temperature of the one room where the room thermostat is installed. This is usually the living or dining room. If this room is warm the central-heating is switched of and the other rooms may stay cold. Vice versa there might be no desire to heat this room. In this case the central-heating keeps running even if the other rooms might be warm enough.
* The heating supply temperature is either controlled manually with a adjustment wheel on the central-heating itself or dependent of the difference of the desired and the actual temperature of the room with the room thermostat. As described above the desired heating might not match that room temperature and thus too high or too low heating supply temeratures might be used.

### Solution
Instead of a room thermostat in one room the heating supply temperature is calculated by the needs of all radiators and the outside temperature.
The central-heating boiler is only running if any radiator requests its need.

## Modus operandi

The workflow is separted in the following parts with the objective to be extended if needed:

10. Getting and updating outside temperature.
20. Calculating and updating heating supply temperature.
30. Controlling the central-heating boiler with hardware module.
