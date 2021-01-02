# Bitcoin price ticker with ESP32 (realtime websockets)

* 7-segment 8-bit - or - Dot Matrix LED Display support with 32x8px
* bitstamp & bitfinex websocket interfacing for lightning fast, real time updates!
* solderless build possible (if you order the display with pre-soldered pin headers)
* low power (<0.5W), cheap to build (around 5 EUR)

## components
* Tile ESP32-DevKitC-32D tile with a built-in module ESP-WROOM-32D ([link](https://www.aliexpress.com/item/1005001621012182.html))
* 7 segment display with MAX7219 ([link](http://s.click.aliexpress.com/e/7uottDW)) or Dot Matrix display ([link](http://s.click.aliexpress.com/e/Jckdk7Q))
* dupont cables (female-to-male) and maybe a cheap antenna ;)

## wiring 7-segment (software SPI, ESP32-DevKitC-32D)

ESP32-DevKitC-32D | Display
--- | ---
GND | GND
5V/VIN | VCC
25  | DIN
26  | CLK
27  | CS

## wiring dot-matrix-display using hardware SPI

ESP32-DevKitC-32D | Display
---     | ---
GND     | GND
5V/VIN  | VCC
25      | CS
14      | CLK
13      | DIN

## how to install
- flash the board by uploading source sketch with arduino IDE
- connect board to power 
- connect your smartphone/computer to ESPxxxxxx wifi
- enter your home wifi settings at the captive portal

## known issues

- compilation error in LedControl.h:  
solution: comment out or delete pgmspace.h include

## more information
This repository is a fork of the [btc-ticker-esp8266 by nebman](https://github.com/nebman/btc-ticker-esp8266). Please see the original repository for more information.