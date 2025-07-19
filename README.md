# [Infinity] -  The Raspberry Pi Pico 1 RP2040's FreeRTOS Firmware written in C/C++ !!!

[19.07.2025] 

[0.0.0.1a] - The Begin.






Goals:

```md
Using :
        Latest Pico C/C++ SDK
        Latest FreeRTOS-Kernel for RP2040


Devices:
        LCD 1602 LiquidCrystal Display 
        Oled SSD1306 Display
        SPI TFCard Reader
        1x Green LED
        1x Potentiometer
        2x Antennen / Spulen (Für EMF-Messungen etc.)
        




Submodules:

```sh

git submodule add -b main   https://github.com/FreeRTOS/FreeRTOS-Kernel.git external/FreeRTOS
git submodule add -b v0.17.0 https://github.com/hathach/tinyusb.git      external/tinyusb
git submodule add -b master https://git.savannah.nongnu.org/git/lwip.git  external/lwip
git submodule update --init --recursive

```