# Source
https://www.96boards.org/documentation/iot/stinger96/hardware-docs/

# GPIO_control.sh
The steps are based on this page:
https://elinux.org/CI20_GPIO_LED_Blink_Tutorial

This script turns on and off the 34th pin on the Expansion Connector with a period of 2 seconds.

Explanation of GPIO=91:
We want to control the 34th pin, based on the connector schematic this means we want to control GPIO PF11 - GPIO-L 96B.
PF11 means 11th GPIO of block "F", controller "/sys/class/gpio/gpiochip80" is labeled as "GPIO F", its base is 80, thus: 80 (first GPIO in block F) + 11 (our GPIO of interest in block F) = 91 (GPIO number to be used in sysfs).
