# Unofficial Adafruit Package Lists for the Arduino v1.6.4+ Board Manager [![Build Status](https://github.com/adafruit/arduino-board-index/workflows/Build/badge.svg)](https://github.com/adafruit/arduino-board-index/actions)

This repo contains a custom `package_adafruit_index.json` file that can be used in Arduino IDE to use an recent compiler toolchain for nRF52.

After succesful installation you'll be able to use the [Arm GNU Toolchain](https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads) v13.2R1 (Okt 2023) based on [GCC 13.2](https://gcc.gnu.org/), instead of GCC v9 (2019) shipped with the default installation.

## Usage

Just add https://raw.githubusercontent.com/zabuxx/arduino-board-index/gh-pages/package_adafruit_index.json as URL in Arduino IDE Settings for the 'Additional Boards Manager URLs'.

![image](https://github.com/zabuxx/arduino-board-index/assets/18469570/a24babde-8657-44c0-8ed6-f25d75f80ea0)

and add the "Adafruit nRF52" using board manager (uninstall it before if needed).

![image](https://github.com/zabuxx/arduino-board-index/assets/18469570/d8e22370-1abd-43b4-8339-e2a749126d9b)


## How

I've downloaded the latest version of the [GNU Arm Embedded Toolchain Downloads](https://developer.arm.com/downloads/-/gnu-rm), recompressed the `.xd` files as `.bz2` and modified `package_adafruit_index.json` to use the latest compiler toolchain.

Only tested on **x86_64-pc-linux-gnu**, but should work on for Win/MacOS as well (open an issue if not). The binaries turn out 7~10% smaller in size with the new compiler, benchmarking is on todo list...

Apart from some [(fixable)](https://stackoverflow.com/a/76388278) linker warnings seem to be working fine, but as always on this part of the show, **no guarantees and use at your own risk**...

![image](https://github.com/zabuxx/arduino-board-index/assets/18469570/ecbfcff3-e4f1-4dc8-b197-e27846a6fead)

![image](https://github.com/zabuxx/arduino-board-index/assets/18469570/d887b917-dbde-4311-88b8-78983e1241ed)

