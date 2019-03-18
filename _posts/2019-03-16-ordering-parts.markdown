---
layout: post
title:  "Ordering parts: esp32 + batteries?"
date:   2019-03-16 20:30:00 +0200
categories: blinds
---
# Ordering parts

It is time to order the parts. Our team have been increasingly  leaning more towards an external end product rather than an internal design. The internal design lacks the great and highly desired portability that comes along with the external design - the whole battery powered product could be moved to another window without the effort of disassembling the reassembling the whole thing.

However, we have been struggling to find a solid solution to battery power this prototype. We really would like to enable high level of portability by powering the whole thing via some sort of portable power supply. This in practice would mean that there is no permanent cabling going to the prototype to operate the device. To enable wireless operation, we also need to be able to recharge the device.

However, this is unfortunately not as simple as we thought and some critical decisions have to made before deciding on and ordering the parts for the prototype.

## Making decisions & engineering requirements

As we've posted recently, we need to be able to power the whole esp32 development board (controller) and the servo motor (actuator). Considering the initial internal blinds prototype, we came into conclusion that the sg90 servo motor is not sufficient for the task and we need something that is able to deliver more torque. Because of this, we need to go for another more power hungry servo which introduced new challenges.

Basically going higher up in torque from sg90 means that the servo is more hungry for power. Unfortunately this means that we are not able to power the servo directly from the development board since drawing too much current over the board fries it up. Based on these thoughts, we came up with some written requirements.

### Requirements

- Prototype design should be *noninvasive* and *require no permanent or irreversible modifications* to the blinds
- Prototype must consist of *three main parts*, as required by the Principles of Digital Fabrications course
  - Controller (esp32)
  - Actuator (servo motor)
  - Sensor (photoresistor)
- Prototype should have following additional features
  - Button (hold to tilt UP)
  - Button (hold to tilt DOWN)
  - Switch (enable or disable "automatic photoresistor mode")
    - Maintain certain level of luminosity (photoresistor input is read and tilt up/down is controlled)
  - LED ("automatic photoresistor mode" status indicator, is on or off)
- Prototype should be battery powered
  - Prototype should be rechargeable by either
    - Sticking a cable to it (eg. micro-usb) OR
    - Manually switching standard lithium AA batteries (that are ofcourse preferably rechargeable)

## The part list

The following parts ended up being ordered. Some common parts for the build and the development such as jumper wires is assumed to be available to us.

![parts ordered from adafruit](/assets/ordered-parts.png)

# Links & some thoughts

Esp32 featured Feather HUZZAH32 development board have amazing battery power capabilities. According to [adafruit's power management guide], Feather HUZZAH32 is able to power the chip when the USB power is powered. In addition to this, it also will automatically switch over to USB for power, as well as start charging the battery (if attached) at 200mA.

[This guy over here have made a simple example project setup][orionrobots] where two devices (controller) and servo (actuator) are powered simultaneously from the same 6V battery pack. The trick used here is to divide the 6V in to two "lanes" and use diodes or some sort of regulators to drop the voltage on the another lane. With this setup, the one battery pack results in two lanes running in 6V that is for servo and 4.7V for the controller.

---

##### <a href="{{ site.github.repository_url }}/tree/master/{{ page.relative_path }}">Edit this page</a>

[orionrobots]: http://orionrobots.co.uk/2015/04/04/powering-arduino-uno-from-4xaa-batteries/
[adafruit's power management guide]: https://learn.adafruit.com/adafruit-huzzah32-esp32-feather/power-management
