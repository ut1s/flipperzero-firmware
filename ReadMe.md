# ut1s's Flipper Zero firmware

<img src="https://user-images.githubusercontent.com/110339660/187163324-7ad7edc7-107e-424d-9450-58408a90e4ee.png" width="200" />

*This is a very cute image, isnt't it?* Generated with [__DALL·E 2__](https://openai.com/dall-e-2/)


Welcome to my fork of the official FlipperZero repo!
It's a flipperzero-firmware repository by me but with some changes like plugins, with own graphics and more! (I hope :sweat_smile:)

This repo will be merged from the official and from the non official firmwares to make an ultimate firmware including games and plugins.
So in the most of the time I'll not really write codes but I'll **always** mention the creator of that part of the code. Soo if there is an issue then -I hope- most of the time it'll not be due to my code :sweat_smile:

I hope it will be a weekly ~~(or sometimes montly)~~ updated firmware and I will the include those cool changes which made on that week ~~(/in that month)~~

In the next days (or weeks) I'll update this ReadMe file to make it more ut1sish but til that I'll not change it very and just delete the for this non nessecary things.

# Fork changes
*An always updating part of the ReadMe*

The parts from firmwares:

~~under construction as I add the things I'll update it~~

## BadUSB thing

A great user [dummy-decoy](https://github.com/dummy-decoy) made a program for PC and for Flipper so you can easily add any kind of keyboard layouts by copying the dummy-decoy's program created .kl files to the SD card and then just simply select it. Due to this `DUCKY_LANG` is not aviable for the scripts. (Just simply delete it form the first line :sweat_smile:) His repo for this is there (download it to make your keyboard layout file): [the best way for this](https://github.com/dummy-decoy/flipperzero_badusb_kl)
This part is from the [__UNLEASHED__ firmware](https://github.com/DarkFlippers/unleashed-firmware/tree/dev/applications/main/bad_usb)


## Infrared

Form the [Unleashed firmware](https://github.com/DarkFlippers/flipperzero-firmware/tree/dev/applications/main/infrared) too as it seems like this application has more things about the universal remotes in it


## SubGHz

This part is from the [Unleashed firmware](https://github.com/DarkFlippers/flipperzero-firmware/tree/dev/applications/main/subghz) too. It means there is support for many rolling code protocols but the region restrictions are still there (btw I'm not sure :sweat_smile:)


## Plugins

- Clock/Stopwatch ([By CompaqDisc, Stopwatch & Sound Alert By RogueMaster](https://gist.github.com/CompaqDisc/4e329c501bd03c1e801849b81f48ea61)) /w 12/24HR ([By non-bin](https://github.com/RogueMaster/flipperzero-firmware-wPlugins/pull/254)) & Refactoring ([By GMMan](https://github.com/RogueMaster/flipperzero-firmware-wPlugins/pull/256))
- DAP Link [(by DrZlo13)[OFW]](https://github.com/flipperdevices/flipperzero-firmware/pull/1897)
- Flipper Authenticator (Totp) [(by akopachov)](https://github.com/akopachov/flipper-zero_authenticator)
- MultiConverter plugin [(by theisolinearchip)](https://github.com/theisolinearchip/flipperzero_stuff)
- Metronome [(by panki27)](https://github.com/panki27/Metronome)
- Mouse Jiggler ([By Jacob-Tate](https://github.com/Jacob-Tate/flipperzero-firmware/blob/dev/applications/mouse_jiggler/mouse_jiggler.c))
- Paint ([By n-o-T-I-n-s-a-n-e](https://github.com/n-o-T-I-n-s-a-n-e/flipperzero-firmware/tree/420/applications/paint))
- Pomodoro Timer ([by sbrin](https://github.com/sbrin/flipperzero_pomodoro))
- Spectrum Analyzer (with changes) [(by jolcese)](https://github.com/jolcese/flipperzero-firmware/tree/spectrum/applications/spectrum_analyzer)
- Sub-GHz Playlist [(by darmiel)](https://github.com/darmiel/flipper-playlist)
- UPC-A Barcode generator plugin [(by McAzzaMan)](https://github.com/McAzzaMan/flipperzero-firmware/tree/UPC-A_Barcode_Generator/applications/barcode_generator)
- USB Keyboard ([by huuck](https://github.com/huuck/FlipperZeroUSBKeyboard))
- WAV player plugin (fixed) [(OFW: DrZlo13)](https://github.com/flipperdevices/flipperzero-firmware/tree/zlo/wav-player)

## Games

- Arkanoid (with fixes) [(by gotnull)](https://github.com/gotnull/flipperzero-firmware-wPlugins)
- Tetris (with fixes) [(by jeffplang)](https://github.com/jeffplang/flipperzero-firmware/tree/tetris_game/applications/tetris_game)
- Heap Defece [(By xMasterX)](https://github.com/RogueMaster/flipperzero-firmware-wPlugins/commit/fc776446de9fdd553b221c02668b925b689378d8) [(original by wquinoa & Vedmein)](https://github.com/Vedmein/flipperzero-firmware/tree/hd/svisto-perdelki)
- T-Rex Runner (yeah, like the Chrome game!) [(By gelin)](https://github.com/gelin/t-rex-runner) WIP

## Another little changes to make your day :)

- __Added my own animation!!__ It's a little DJ animation with a cute dolphin of course!
- Hold Center to change Flipper idle animation. [Thanks to Zycenios](https://github.com/flipperdevices/flipperzero-firmware/commit/111786ef40e50a40d2e510595672b569d9b97bba) With changes by RogueMaster and pasted from [RogueMaster's firmware](https://github.com/RogueMaster/flipperzero-firmware-wPlugins) of course

<!--
This is a comment. It won't seen on the page. I hope. You can prewrite the text here and after just get out of this comment.
--->

# Clone the Repository

You should clone with 
```shell
$ git clone --recursive https://github.com/flipperdevices/flipperzero-firmware.git
```

# Read the Docs

Check out details on [how to build firmware](documentation/fbt.md), [write applications](documentation/AppsOnSDCard.md), [un-brick your device](documentation/KeyCombo.md) and more in `documentation` folder. 

# Update firmware

[Get Latest Firmware from Update Server](https://update.flipperzero.one/)

Flipper Zero's firmware consists of two components:

- Core2 firmware set - proprietary components by ST: FUS + radio stack. FUS is flashed at factory, and you should never update it.
- Core1 Firmware - HAL + OS + Drivers + Applications.

They both must be flashed in the order described.

## With offline update package

With Flipper attached over USB:

`./fbt flash_usb`

Just building the package:

`./fbt updater_package`

To update, copy the resulting directory to Flipper's SD card and navigate to `update.fuf` file in Archive app. 

## With STLink

### Core1 Firmware

Prerequisites:

- Linux / macOS
- Terminal
- [arm-gcc-none-eabi](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads)
- openocd

One-liner: `./fbt firmware_flash`

## With USB DFU 

1. Download latest [Firmware](https://update.flipperzero.one)

2. Reboot Flipper to Bootloader
 - Press and hold `← Left` + `↩ Back` for reset 
 - Release `↩ Back` and keep holding `← Left` until blue LED lights up
 - Release `← Left`

3. Run `dfu-util -D full.dfu -a 0`

# Build on Linux/macOS

Check out `documentation/fbt.md` for details on building and flashing firmware. 

## macOS Prerequisites

Make sure you have [brew](https://brew.sh) and install all the dependencies:
```sh
brew bundle --verbose
```

## Linux Prerequisites

The FBT tool handles everything, only `git` is required.

### Optional dependencies

- openocd (debugging/flashing over SWD)
- heatshrink (compiling image assets)
- clang-format (code formatting)
- dfu-util (flashing over USB DFU)
- protobuf (compiling proto sources)

For example, to install them on Debian, use:
```sh
apt update
apt install openocd clang-format-13 dfu-util protobuf-compiler
```

heatshrink has to be compiled [from sources](https://github.com/atomicobject/heatshrink).

## Compile everything

```sh
./fbt
```

Check `dist/` for build outputs.

Use **`flipper-z-{target}-full-{suffix}.dfu`** to flash your device.

## Flash everything

Connect your device via ST-Link and run:
```sh
./fbt firmware_flash
```

# Links

~~under construction~~

# Project structure
*(I kept this part lol)*

- `applications`    - Applications and services used in firmware
- `assets`          - Assets used by applications and services
- `furi`            - Furi Core: os level primitives and helpers
- `debug`           - Debug tool: GDB-plugins, SVD-file and etc
- `documentation`   - Documentation generation system configs and input files
- `firmware`        - Firmware source code
- `lib`             - Our and 3rd party libraries, drivers and etc...
- `scripts`         - Supplementary scripts and python libraries home

Also pay attention to `ReadMe.md` files inside of those directories.
