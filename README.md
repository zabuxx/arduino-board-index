# Unofficial Adafruit Package Lists for the Arduino v1.6.4+ Board Manager [![Build Status](https://github.com/adafruit/arduino-board-index/workflows/Build/badge.svg)](https://github.com/adafruit/arduino-board-index/actions)

This repo contains a custom `package_adafruit_index.json` file that can be used in Arduino IDE to use an recent compiler toolchain for e.g nRF52.

## Usage

Just add https://raw.githubusercontent.com/zabuxx/arduino-board-index/gh-pages/package_adafruit_index.json as url in Arduino IDE Settings for the 'Additional Boards Manager URLs'.


## How

I've downloaded the latest version of the [GNU Arm Embedded Toolchain Downloads](https://developer.arm.com/downloads/-/gnu-rm), recompressed the `.xd` files as `.bz2` and moified `package_adafruit_index.json` to use the latest compiler toolchain.

Apart from some linker warnings seem to be working fine, but use at your own risk...



