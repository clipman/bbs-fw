# BBSHD Open Source Firmware

This firmware is inteded to replace the original Bafang firmware on the BBSHD motor controller.  
Almost all functionallity of original firmware has been implemented and more special features  
has been added.

This firmware is compatible with all displays that works with the original firmware.
A custom configuration tool is provided since BafangConfigTool is not compatible  
due to a different set of supported parameters.

**Install**  
See https://github.com/danielnilsson9/bbshd-fw/wiki/Flashing-the-Firmware

**Configure**  
See https://github.com/danielnilsson9/bbshd-fw/wiki/Configuration-Tool

**The firmware can be flashed using a standard bafang programming cable (TTL level usb to serial converter).**

## Highlights
* More power without hardware modifications! (max 32A).
* No upper voltage limit in software, can by default run up to 63V (maximum rating of components).
* Support lower voltage cutoff for use with e.g. 36V battery.
* No issue with PAS/Throttle override.
* Optional separate set of street legal & offroad assist levels.
* Possible to set road speed limit per assist level.
* Possible to limit cadence per assist level.
* Support cruise assist levels (i.e. motor power without pedal or throttle input).
* Display motor/controller temperature (shown in range field on display).
* Use of speed sensor is optional.
* Use of display is optional.

![Config Tool](https://raw.githubusercontent.com/wiki/danielnilsson9/bbshd-fw/img/config_tool/config_tool3.png)

## Limitations
* No battery SOC calculation, set display to show battery voltage instead.
* No range estimation, the range field on the display will show motor temperature instead.
* Voltage cutoff is a bit crude, it does not limit power when approaching limit.  
When limit has been hit controller is disabled and needs to be restarted by power cycle.

## Supported Hardware Revisions

Revision | MCU          | Released    | Comment
-------- | ------------ | ----------- | --------------------
V1.4     | STC15W4K56S4 | ~2017       | V1.3 printed on PCB, sticker with 1.4.
V1.5     | IAP15W4K61S4 | ~2019       | V1.4 printed on PCB, sticker with 1.5.

## Legal
* Installing this firmware will void your warranty.
* I cannot be held responsible for any injuries caused by the use of this firmware, use at your own risk.
